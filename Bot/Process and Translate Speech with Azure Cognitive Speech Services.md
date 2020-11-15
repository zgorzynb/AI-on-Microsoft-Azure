# Process and Translate Speech with Azure Cognitive Speech Services

## Transcribe speech input to text

### Wstęp

Usługa speach-to-text (inaczej speach recognition) pozwala na przetwarzanie plików w formacie audio do formy tekstowej. Konwersja odbywa się w czasie rzeczywistym. Dzięki tej usłudze jesteśmy w stanie wyświetlać oraz przetwarzać dane, które użytkownik zadaje w formie komend głosowych. Jedną z możliwości wykorzystania możliwości serwisu jest trenowanie własnych modeli językowych, dzięki czemu będzie można łatwiej poradzić sobie z hałasem dobiegającym z otoczenia lub specyficznym słownictwem.

### Sposoby wykorzystania

Poniżej przedstawiono przykładowe zastosowania usługi speech-to-text:

- Obsługa radia i klimatyzacji podczas prowadzenia samochodu. Podawanie komend głosowych pozwoli na zwiększenie bezpieczeństwa jazdy, ponieważ kierowca nie musi odrywać rąk od kierownicy
- Bot do przeprowadzania rozmów SANEPID-u, w związku z panującą epidemią. Dzięki wykorzystaniu serwisu, będziemy w stanie zrozumieć osobę dzwoniącą
- Automatyczne tworzenie napisów do filmu. Dodatkowo takie napisy można w łatwy sposób przetłumaczyć na interesujący nas język.

### Użytkowanie serwisu

**Jak korzystać z serwisu?**

Serwis może być użyty z poziomu strony AZURE poprzez REST API, poprzez Speech SDK oraz Speech CLI. Korzystanie z serwisu polega na programowaniu w jednym z obsługiwanych języków między innymi: C#, C++, Java, Python, JavaScript oraz Objective-C. W przypadku języka Python, obsługa serwisu polega na importowaniu przygotowanych bibliotek i korzystaniu z nich.

**Płatności**

Microsoft oferuje dwa modele płatności za opisywany serwis. W przypadku modelu darmowego, możemy przetworzyć 5 godzin nagrań audio na miesiąc. Dodatkowo hostowanie jednego modelu jest darmowe. W przypadku modelu Standardowego, opłata za przetworzenie godziny nagrania audio wynosi:

- $1 w standardowym przypadku
- $1.40 w niestandardowym przypadku. Dodatkowo utrzymanie modelu kosztuje $1.2904 za godzinę
- $2.10 w przypadku dźwięku wielokanałowego (?)

## Synthesize Text Input to Speech

### Wstęp

Usługa text-to-speech jest pewnego rodzaju syntezatorem mowy. Przekształca dane zapisane w formacie tekstowym do języka naturalnego. W serwisie dostępnych jest wiele różnych głosów. Na chwilę obecną mamy możliwość na wykorzystanie jednego z 75 głosów, mówiących w 45 różnych językach. 

### Sposoby wykorzystania

Poniżej przedstawiono kilka przykładowych możliwości wykorzystania usługi text-to-speech:

- Ogłoszenia na rozmaitych stacjach PKP, PKS lub metra. Wykorzystanie serwisu pozwoli na łatwe zmiany w komunikatach
- Lektor bajek dla dzieci w przedszkolach oraz szkołach podstawowych. Również dla dzieci niewidomych.

### Użytkowanie serwisu

**Jak korzystać z serwisu?**

Korzystanie z usługi text-to-speech polega na wykorzystaniu przeznaczonego do tego REST API lub Speech SDK. Korzystanie z usługi jest niezwykle podobne do poprzedniego przypadku, różnią się jedynie wykorzystane funkcje.

**Płatności**

Podobnie jak  w poprzednim przypadku dostępne są dwa modele finansowania.

Model darmowy pozwala na przetworzenie 5 mln znaków miesięcznie, z czego 0.5 mln może być przetworzone do języka neuralnego, który cechuje się lepszą jakością i większym podobieństwem do prawdziwego głosu.

Model standardowy, opłaty za przetworzenie miliona znaków wynoszą:

- $4 w standardowym przypadku
- $16 w przypadku głosów neuralnych, $100 jeżeli audio okaże się długie
- $6 w niestandardowych przypadkach (stworzone własne modele). Koszt hostingu wynosi $0.0537 za godzinę
- $24 w niestandardowych przypadkach. Koszt hostingu wynosi: $4.04 za godzinę

## Translate speech with the speech service

### Wstęp

Speech translation pozwala na automatyczne tłumaczenia nagrania audio na jeden z wielu dostępnych języków. Wynikiem operacji jest tekst we wskazanym języku, a na wejściu podajemy ścieżkę audio, którą chcemy przetłumaczyć. 

### Sposoby wykorzystania

Wykorzystanie usługi Speech Translation może pozwolić na przykład na:

- Wykorzystanie 3 omówionych usług może pozwolić na tworzenie automatycznego lektora w wielu językach
- Prowadzenie wszelkiego rodzaju rozmów biznesowych, przez ludzi nie znających swoich języków. 

### Użytkowanie serwisu

**Jak korzystać z serwisu?**

Korzystanie z serwisu przebiega podobnie jak w przypadku dwóch opisywanych wcześniej usług.

**Płatności**

Podobnie jak we wcześniej omawianych usługach istnieją dwa plany płatności.

Plan darmowy powala na tłumaczenie 5 godzin audio miesięcznie.

W przypadku modelu standardowego, przetłumaczenie godziny nagrań to koszt $2.5.



