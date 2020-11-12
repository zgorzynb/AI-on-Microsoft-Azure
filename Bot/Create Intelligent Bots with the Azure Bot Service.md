# Create Intelligent Bots with the Azure Bot Service

## QnA Maker and Azure Bot Service

### Wstęp

QnA Maker pozwala na tworzenie bazy wiedzy poprzez podawanie najczęstszych pytań wraz z odpowiedziami. Dzięki takiemu przygotowaniu danych, będzie możliwe stworzenie bota, który będzie w stanie zarówno zadawać pytania jak i na nie odpowiadać.  

Azure Bot pozwala na tworzenie dowolnego typu botów poprzez integrację rozmaitych serwisów dostępnych na Microsoft Azure. Dodatkowo takiego bota możemy udostępnić na jakimś kanał np. Skype, MS Teams i z niego korzystać.

### Sposoby wykorzystania

Poniżej przedstawiono kilka przykładowych możliwości wykorzystania omawianych serwisów:

- Przygotowanie bota, który przyjmie zamówienie na burgera, dokładnie wypyta o składniki i szczegóły przygotowania. Dodatkowo odpowie na pytania zamawiającego
- Bot odpowiadający na najczęściej zadawane pytania w związku z panującą pandemią

### Użytkowanie serwisu

**Jak korzystać z serwisu?**

W celu utworzenia bazy pytań i odpowiedzi w serwisie QnA możemy wybrać jedną z dwóch opcji.  Wykorzystanie interfejsu, który został do tego przeznaczony lub wczytanie odpowiednio przygotowanego pliku tekstowego. 

Wykorzystywanie Azure Bot Service jest niezwykle proste. Po utworzeniu odpowiedniego zasobu, możemy wybrać interesujący nas szablon, a następnie wykorzystać tak stworzonego bota na rozmaitych kanałach.

**Płatności**

W przypadku serwisu QnA Maker niezależnie od wybranego pakietu jesteśmy w stanie obsłużyć 3 transakcję na sekundę. Microsoft oferuje 2 modele finansowania:

- Model bezpłatny posiada ograniczenie do 100 transakcji na minutę oraz 50000 na miesiąc. Dodatkowo każdy dokument musi być w rozmiarze poniżej 1 Mb. Maksymalna liczba zarządzanych dokumentów to 3.
- Model standardowy kosztuje $10 miesięcznie. Posiada on ograniczenie do 100 transakcji na minutę, jednak możemy dzięki niemu zarządzać nieograniczoną liczbą dokumentów

Wykorzystywanie Azure Bot Service na kanałach standardowych jest darmowe i pozwala na nieograniczoną liczbę komunikatów niezależnie od wybranego modelu finansowania. W przypadku kanałów premium (własne witryny i aplikacje) mamy możliwość wykonania 10 000 komunikatów miesięcznie za darmo. W przypadku, kiedy potrzebujemy większej liczby komunikatów musimy się zdecydować na plan S1. 1000 komunikatów kosztuje w tym przypadku $0.50. Dodatkowo musimy pamiętać, że wszystkie inne serwisy wykorzystane w naszej aplikacji również podlegają płatności zgodnie ze swoimi nominalnymi stawkami.

## Bot Framework Composer

### Wstęp

Bot Framework Composer jest narzędziem, które pozwala na bardzo łatwe tworzenie skomplikowanych botów. Jego głównym zadaniem jest łączenie działania rozmaitych serwisów, dostępnym w Microsoft Azure. Praca w tej aplikacji opiera się na wykorzystywaniu interfejsu graficznego. 

## Sposoby wykorzystania

Bot Framework Composer jest bardzo rozległą aplikacją, która wraz z innymi serwisami daje użytkownikowi szerokie pole manewru w tworzeniu różnego rodzaju botów. Stworzyć można przeróżne boty, przetwarzające zarówno dane pisane jak i dźwiękowe. Integracja z odpowiednimi serwisami pozwoli na tworzenie bardzo zaawansowanych struktur, dzięki czemu będziemy w stanie rozwiązać wiele zadań żmudnych dla człowieka.

## Użytkowanie

**Jak korzystać z narzędzia?**

W celu wykorzystania Bot Framwork Composer-a należy pobrać odpowiednią aplikację oraz pozostałe programy, które są wymagane (Bot Framework Emulator oraz .NET Core SDK 3.1 lub późniejsza wersja). Aplikacja posiada bogatą oprawę graficzną, a korzystanie z niej jest intuicyjne. 

Ogólne użytkowanie narzędzia polega na korzystaniu z aplikacji, a tworzenie botów praktycznie nie wymaga programowania. Wynikiem tego jest większa otwartość narzędzia dla ludzi, którzy nie są związani z programowaniem tylko na przykład z biznesem.

**Płatności**

Bot Framework Composer jest narzędziem typu open source. Korzystanie z niego jest bezpłatne. 

Jedynymi kosztami są serwisy, z których korzystamy.



