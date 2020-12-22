# Computer Vision Theory Part

## Computer Vision API

### Wstęp

**Face API**

Pozwala na detekcję oraz analizę twarzy na obrazach. W ogólności narzędzie jest w stanie wykonywać 5 równych zadań: weryfikację, detekcję, identyfikację, podobieństwo oraz grupowanie. Na wyjściu otrzymujemy lokalizację twarzy, markery pewnych elementów twarzy oraz dodatkowe atrybuty takie jak: wiek, płeć, kolor włosów.

**Emotion API**

Emotion API jest w stanie wykrywać emocje, ukazywane na ludzkiej twarzy. Możemy wyróżnić na przykład: złość, strach lub szczęście, jednak serwis jest w stanie wykryć znacznie więcej.

### Sposoby wykorzystania

- Szpiegowski program, który ocenia emocję osoby korzystającej z telefonu (przez przednią kamerę). Dzięki temu ocenia, co podoba się danej osobie.
- System nie wpuszczania osób podejrzewanych o terroryzm na lotniska, stacje autobusowe lub do pociągów
- Detekcja i rozpoznanie twarzy w celu udostępnienia pewnych danych, dostępu do pokoju itp. (wraz z innym pomiarem np. odcisku palca)

### Użytkowanie serwisu

**Jak korzystać z serwisu?**

Korzystanie z serwisu polega na komunikacji z API, które jest dostępny od razu po stworzeniu zasobu w Microsoft Azure. Dodatkowo komunikacja z REST API może być przeprowadzana z wykorzystaniem przygotowanych bibliotek np. azure-cognitiveservices-vision-face dla Pythona.

**Płatności**

Dostępne są dwa modele finansowania serwisu:

- Model bezpłatny pozwala na wykonywanie 20 transakcji na minutę. W przypadku tej opcji mamy możliwość wykonywania 30000 bezpłatnych transakcji miesięcznie

- Model standardowy pozwala na wykonywania 10 transakcji na minutę. Cena za jedną transakcję wynosi:

  - Od 0 do 1 mln transakcji - $1 za 1000 transakcji
  - Od 1 mln do 5 mln transakcji - $0,80 za 1000 transakcji
  - Od 5 mln do 100 mln transakcji - $0,60 za 1000 transakcji
  - Ponad 100 mln transakcji - $0,40 za 1000 transakcji

  Dodatkowo, w tym modelu możemy stworzyć magazyn twarzy. Cena za przechowywanie 1000 twarzy na miesiąc wynosi $0,01.

## Custom Vision

### Wstęp

Serwis Custom VIsion  pozwala na tworzenie modeli głębokiego uczenia, które pozwalają na wykonywanie zadań klasyfikacji i detekcji. Modele trenowane są z wykorzystaniem par danych (image - label). Serwis pozwala na przeprowadzanie treningu, a następnie na wykonywanie predykcji nowych obrazów. Po utworzeniu i wytrenowaniu modelu, możemy go opublikować i komunikować się z nim poprzez API. 

## Sposoby wykorzystania

- Sprawdzanie, czy osoby na obrazie mają założoną maseczkę.
- System wyboru najlepszych ziaren jęczmienia w produkcji piwa.
- Wyznaczanie pozycji tablic rejestracyjnych widocznych na obrazach.

## Użytkowanie

**Jak korzystać z narzędzia?**

Korzystanie z narzędzia rozpoczyna się od stworzenia projektu w portalu Custom Vision. Budowanie modelu, tagowanie, trening oraz testowanie mogą zostać wykonane przez przygotowaną aplikację WEB. Komunikacja z serwisem może przebiegać z wykorzystaniem API serwisu. W tym celu należy opublikować model i pobrać odpowiednie dane (endpoint, keys).

**Płatności**

Dostępne są dwa modele finansowania serwisu:

- Model bezpłatny pozwala na wykonywanie 2 transakcji na sekundę. Liczba projektów ograniczona jest do 2. Dzięki wybrani tej opcji możemy przeprowadzić godzinę treningu miesięcznie i  wykonywać 10000 prognoz miesięcznie.
- Model standardowy pozwala na wykonywanie 10 transakcji na sekundę. Liczba projektów ograniczona jest do 100. Koszt 1000 transakcji wynosi $2, godzina treningu kosztuje $20, a przechowywanie 1000 obrazów (każdy do 6MB) - $0,70.

## Video Indexer

### Wstęp

Usługa Video Indexer pozwala nam na analizę danych zawartych w nagraniach wideo. W szczególności pozwala na załadowanie, indeksowanie, wydobywanie szczegółów w nagraniu. Serwis ten wykorzystuje modele ML i DL,. które mogą być edytowane przez użytkownika. Dzięki odpowiedniemu przygotowaniu tych modeli jesteśmy w stanie przygotować bardzo zaawansowane platformy do analizy plików wideo.

## Sposoby wykorzystania

- Wykrywanie niebezpiecznych zachowań w centrach handlowych, bazując na danych z kamer
- System alarmowania pielęgniarek w szpitalach, w przypadku dziwnego zachowania pacjentów na salach
- Automatyzacja detekcji nietypowych zachowań w dowodach policji. W ten sposób nagrania byłyby przetwarzane znacznie szybciej.
- Wykrywanie i wysyłanie informacji do policji o osobach, które będą przemieszczały się w Sylwestra :)

## Użytkowanie

**Jak korzystać z narzędzia?**

Pierwszym krokiem jest stworzenie odpowiedniego zasobu w Microsoft Azure. Następnie mozemy pobrać endpoint i odpowiednie klucze w celu komunikacji z API serwisu. Następnie możemy wysłać do serwisu film, a następnie otrzymać dane takie jak: słowa kluczowe, OCR, transkrypcję itd.

**Płatności**

Cena wykorzystania serwisu jest mocno zależna od szczegółów wykorzystania. Pełen cennik dostępny jest [tutaj](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/video-indexer/). Analiza, indeksowanie itd. mają inne koszta wykorzystania! 



