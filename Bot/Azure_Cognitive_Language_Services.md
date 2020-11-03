# Azure Cognitive Language Services

## Content Moderator

### Wstęp

Content Moderator to usługa, która pozwala na  sprawdzanie tekstów, obrazów oraz wideo w celu wykrycia niepożądanych treści. W tym celu serwis wykorzystuje mechanizmy sztucznej inteligencji (SI). Wynik działania przesyłany jest w formacie JSON, w którym zawarte są szczegółowe informacje dotyczące konkretnego tekstu/obrazu/wideo. W odpowiedzi zawarta może być informacja, czy wiadomość powinna zostać sprawdzona przez człowieka. Warto zaznaczyć, że usługa przystosowana jest do pracy z wieloma językami, które są rozpoznawane automatycznie.

### Sposoby wykorzystania

Poniżej przedstawiono kilka przykładowych możliwości wykorzystania serwisu Content Moderator:

- Filtrowanie ogłoszeń na serwisie aukcyjnym - usuwanie pozycji zawierających wulgaryzmy lub niecenzuralne zdjęcia. 
- Blokowanie publikowania dodatkowych danych kontaktowych na portalach randkowych. W ten sposób można wymusić korzystanie wyłącznie z czatu danego serwisu.
- Moderacja komentarzy na portalach społecznościowych. Usuwanie treści niestosownych.

### Użytkowanie serwisu

**Jak korzystać z serwisu?**

Korzystanie z serwisu polega na wykorzystywaniu przeznaczonych do tego API. Najpierw należy stworzyć zasób przypisany do konta wraz z wybranym modelem płatności. Na wejście wysyłamy tekst, obraz lub wideo. Każde z nich posiada pewną ograniczoną wielkość. Na wyjściu otrzymujemy dokument w formacie JSON, który zawiera stosowne informacje. Warto zaznaczyć, że usługa ma możliwość pobierania najważniejszych informacji personalnych z zadanego tekstu. Dodatkowo, podczas analizy tekstu możliwa jest klasyfikacja, która pozwala określić jakiego typu był znaleziony niestosowny fragment. 

**Płatności**

Podczas korzystania z serwisu Content Moderator, możemy zdecydować się na jeden z dwóch modeli płatności.

* Model darmowy pozwala na wykonywanie 5000 transakcji miesięcznie, z częstotliwością jednej transakcji na sekundę. Dodatkowym ograniczeniem nakładanym na plan darmowy jest posiadanie wyłącznie jednego serwisu opierającego się na modelu darmowym.

* Model standardowy pozwala na wykonywanie 10 zapytań na sekundę. Koszty z tym związane zostały przedstawione w poniższej tabeli.

  | Liczba zapytań w miesiącu | Cena za 1000 zapytań |
  | :-----------------------: | :------------------: |
  |          0 -1 M           |          $1          |
  |          1M - 5M          |        $0.75         |
  |         5M - 10M          |        $0.60         |
  |           10M+            |        $0.40         |



# Language Understanding Intelligent Service (LUIS)

## Wstęp

Language Understanding Intelligent Service jest usługą, która pozwala na analizę języka naturalnego. W szczególności umożliwia wyznaczenie ogólnego znaczenia wypowiedzi oraz wyciągnięcia najważniejszych szczegółów. W ogólności LUIS odpowiada za zrozumienie języka naturalnego (ang. Natural Language Understanding). 

## Sposoby wykorzystania

Poniżej przedstawiono kilka przykładowych możliwości wykorzystania serwisu LUIS:

- Chatbot, przeznaczony do przyjmowania zamówień w kebabowni poprzez wiadomości na portalu społecznościwym

- Autonomiczna suszarka do włosów, która reguluje temperaturę oraz ciśnienie. Sterowanie suszarką opiera się na komendach głosowych.

- Proponowanie podstawowych rozwiązań problemów w dziale obsługi klienta. Zarówno w formie tekstowej jak i rozmowy telefonicznej.

## Użytkowanie serwisu

**Jak korzystać z serwisu?**

Korzystanie z usługi bazuje na komunikacji z API poprzez protokół HTTP. Po stworzeniu zasobów w chmurze, można rozpocząć pracę z serwisem. Podczas konfiguracji usługi należy zdefiniować listę intencji wraz ze słowami kluczowymi, które je opisują. Na wejście przekazywany jest tekst, który ma zostać poddany interpretacji. Wynikiem jest dokument w formacie JSON, który zawiera listę intencji wraz z wyznaczoną jakością dopasowania. Dodatkowo wyznaczane są pewne dane szczególne zawarte w tekście. Wszystkie uzyskane w ten sposób informacje można dalej przetwarzać w celu klasyfikacji, tworzenia zamówień itd.

**Płatności**

Podczas korzystania z serwisu Language Understanding Intelligent Service mamy do wyboru dwa modele finansowania:

- Model darmowy pozwala na wykonywanie 5 zapytań na sekundę. Liczba zapytań miesięcznych została w tym modelu ograniczona do 10000. Warto dodać, że zapytania głosowe nie są obługiwane.

- Model standardowy pozwala na wykonywanie 50 zapytań na sekundę. Cena za 1000 transakcji wynosi €1,265 w przypadku zapytań tekstowych oraz €4,639 w przypadku zapytań głosowych.

  

# Text Analytics

## Wstęp

Text Analytics jest usługą chmurową, która dostarcza szereg funkcji przetwarzania języka naturalnego. Pozwala między innymi na wyznaczenie ogólnej tonacji wyrażenia (pozytywne czy negatywne), wyznaczanie kluczowych fraz, określanie języka oraz rozpoznawanie encji. 

Ocena tonacji wyrażenia pozwoli między innymi na określenie nastroju piszącego. Pozwala to na klasyfikację komentarzy na pozytywne oraz negatywne. Funkcja ta zwraca ocenę opinii od 0 do 1, przy czym 1 jest najbardziej pozytywna. 

Ekstrakcja kluczowych fraz pozwoli na bardzo szybką identyfikację głównego wątku w tekście i na wyodrębnienie słów kluczowych.

Detekcja języka pozwala na określenie, w jakim języku napisany został przedstawiony tekst.

## Sposoby wykorzystania

Poniżej przedstawiono kilka przykładowych możliwości wykorzystania serwisu Text Analytics:

- Ukrywanie negatywnych komentarzy dotyczących produktów w sklepie internetowym
- Dobór odpowiednich reklam na portalu społecznościowym, bazując na nastroju użytkownika podczas jego konwersacji
- Wybór odpowiedniego konsultanta w biurze obsługi klienta międzynarodowej firmy, bazując na nastroju oraz języku klienta

## Użytkowanie serwisu

**Jak korzystać z serwisu?**

Komunikacja z serwisem przebiega za pomocą HTTP. Po stworzeniu odpowiedniego zasobu, korzystanie z usługi staje się niezwykle proste. Korzystanie z serwisu polega głównie na analizie wyników wygenerowanych przez program. Danymi wejściowymi powinien by nieprzetworzony tekst, otrzymany od użytkownika. Na wyjściu otrzymujemy dokument w formacie JSON. Następnie mamy możliwość analizowania, wizualizowania lub kategoryzowania otrzymanych wyników. 

**Płatności**

Podczas korzystania z serwisu Language Understanding Intelligent Service mamy do wyboru kilka modeli finansowania:

- Model darmowy pozwala na wykonywanie 5000 zapytań miesięcznie i daje nam dostęp do następujących funkcji:
  - Sentiment Analysis
  - Key Phrase Extraction
  - Language Detection
  - Named Entity Recognition (not available in Container)
- Model standardowy daje nam dostęp do tych samych funkcji co model darmowy, jednak ceny za 1000 transakcji wahają się pomiędzy $2 oraz $0.25 w zależności od miesięcznej liczby zapytań
- Modele S0-S4 pozwalają na wykupienie określonej liczby zapytań w danym miesiącu. Wraz ze wzrostem ceny, wzrasta liczba dostępnych zapytań oraz spada cena za transakcje nadwyżkowe. Modele te dają dostęp do tych samych funkcji co model darmowy, jednak funkcja Named Entity Recognition może być wykonywana również w kontenerze.



