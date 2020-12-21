# Wyznaczanie liczby osób na obrazie

## Cel projektu

Celem projektu jest przygotowanie programu, którego celem będzie zliczanie osób zawartych na obrazie. W tym celu wykorzystany został serwis Custom Vision dostępny na portalu Microsoft Azure.

## Dane

Podczas przygotowywania modelu, wykorzystano dane ze zbioru "CrowdHuman". Zbiór tne dostępny jest [tutaj](https://www.crowdhuman.org/). Warto zaznaczyć, że wykorzystane zostały wyłącznie obrazy, bez opisów i dodatkowych danych.

## Podejście do problemu

Zliczanie osób widocznych na obrazie należy do stosunkowo trudnych zadań. W moim podejściu zdecydowano na przygotowanie modelu, którego zadaniem będzie detekcja głów widocznych na obrazie. Liczba osób wyznaczana będzie poprzez sumowanie liczby detekcji.

## Przygotowanie modelu

**Inicjalizacja projektu**

Pierwszym krokiem było stworzenie nowego projektu na stonie customvision.ai. Utworzono również nowy zasób oraz grupę zasobów.

**Wczytywanie danych**

Pierwszym krokiem w nowo stworzonym projekcie było dodanie zestawu danych treningowych. Następnie na każdym obrazie zaznaczono wszystkie występujące na nim głowy. Zarówno widoczne z przodu jak i z tyłu.

**1 iteracja treningu **

Podczas pierwszej iteracji treningu wykorzystano 51 ręcznie oznaczonych zdjęć. Wyniki tego treningu wyglądają następująco:

Precission - 100%

Recall - 29.6%

mAP - 62.4 %

Dodatkowo przeprowadzono testy na kilku obrazach nie należących do zbioru treningowego. Poniżej przedstawiono wyniki detekcji testowych.



Jak widać na powyższych obrazkach, jakość predykcji nie jest idealna. Zdecydowano zatem na dodanie kolejnych obrazów, tym razem wykorzystując wcześniejszy model do zaznaczania obiektów. W tym wypadku usuwam błędne predykcje i zaznaczam dodatkowe niewykryte głowy.

**2 iteracja treningu**

Druga iteracja treningu przeprowadzona została dla 100 obrazów treningowych. Wyniki tego treningu wyglądają następująco:

Precission - 94.3 %

Recall - 59.9 %

mAP - 78%

Poniżej przedstawiono testy dla kilku obrazów nie należących do zbioru treningowego:



Zauważyłem, że predykcje z drugiej iteracji są podobne do tych z 1, jednak prawdopodobieństwa są znacznie wyższe. Dodatkowo znaczny wzrost wartości recall oraz mAP, zwiastuje, że model działa lepiej niż po 1 iteracji.

**3 iteracja**

Ze względu na to, że dodanie dodatkowych 50 obrazów do obrazów z 1 iteracji przyniosło pozytywne skutki, zdecydowano na przeprowadzenie jeszcze jednej, ostatniej iteracji. W tym przypadku podczas treningu wykorzystane zostały

## Zliczanie predykcji

W celu zliczenia predykcji zdecydowano na przygotowanie skryptu w Pythonie. Skrypt ten został przygotowany w środowisku jupyter notebook. Jest dostępny [tutaj](https://github.com/zgorzynb/AI-on-Microsoft-Azure/blob/main/Computer_Vision/People_counter.ipynb). 

Zdecydowano na komunikację z serwisem przy pomocy API. Wykorzystano zatem bibliotekę requests. 

Dodatkowo, przygotowano funkcję, której zadaniem jest nie tylko zliczenie predykcji ale też naszkicowanie obrazu, wraz z zaznaczonymi ramkami.

## Napotkane problemy

Podczas wykonywania projektu nie natknięto się na żadne duże problemy. Warto jednak zaznaczyć, że oznaczanie zdjęć okazało się niezwykle czasochłonne, ponieważ na niektórych trzeba było zaznaczyć nawet około 20 głów. Dodatkowo bardzo długo zastanawiałem się, dlaczego moje zapytanie nic nie zwraca. Wystarczyła zmiana GET na POST :).

## Możliwości rozwoju projektu



## Wnioski

Dzięki wykorzystaniu serwisu Custom Vision udało się

