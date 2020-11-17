# Bot dla sklepu z traktorami

## Wstęp

Celem projektu było stworzenie bota, który będzie odpowiadał potencjalnym klientom sklepu z traktorami. W związku z dużym obłożeniem firmy i małą ilością pracowników, nie możliwe było odpowiadanie wszystkim potencjalnym klientom. Część z nich dopytywała wyłącznie o oczywiste rzeczy, takie jak numer telefonu do dilera lub adres firmy. Część z tych przypadków zostanie obsłużona przy pomocy stworzonego bota.

## Dodatkowe pliki

Pliki źródłowe bota zostały zapisane [tutaj](https://github.com/zgorzynb/AI-on-Microsoft-Azure/tree/main/Bot/Tractor_shop_bot)

Nagranie prezentujące bota zostało zamieszczone [tutaj](https://www.youtube.com/watch?v=ci2BcX1Rcd8&ab_channel=Bart%C5%82omiejZg%C3%B3rzy%C5%84ski)

# TODO

## Wykorzystane usługi

Podczas tworzenia bota wykorzystano aplikację Bot Framework Composer, który pozwolił na stworzenie bota w graficznym środowisku. Warto zaznaczyć, że przygotowane rozwiązanie jest w większości wykonane właśnie w graficznym środowisku. Dodatkowo, podczas tworzenia bota wykorzystano następujące serwisy:

- LUIS - serwis ten został wykorzystany w celu rozpoznawania znaczenia tekstu. Wszystkie wyzwalacze, które zostały wykorzystane w bocie zostały zbudowane na podstawie predykcji tego serwisu. Przygotowane zostały następujące klasy:
  - help - pozwalał na pokazanie pomocy. Zawierał 4 przykłady m. in "help" oraz "open help"
  - buy - pozwala na rozpoczęcie dobierania odpowiedniego ciągnika. Zawiera 7 przykładów m. in "I want to buy something" oraz "explore your tractors"
  - question - pozwala na napisaniu zachęty do zadawania pytań. Zawiera 5 przykładów m.in "Can I have a question?" oraz "Can I ask something?"
  - cancel - pozwala na zakończenie wszystkich otwartych dialogów. Zawiera 8 przykładów m.in "Cancel" oraz "Bye"
- QnA Maker - serwis ten pozwolił na stworzenie bazy pytań, które mógłby zadać potencjalny klient. Przykładowe pary pytań i odpowiedzi zostały przedstawione poniżej:
  - Pytanie: "How can I contact you?" Odpowiedź: "You can phone our dealer: +48 999-999-999"
  - Pytanie: "What does your company do?" Odpowiedź: "Our company sells tractors in Poland. We are the largest company of this type in the country."
  - Pytanie: "How could I order a tractor?" Odpowiedź: "You should contact our dealer."

Połączenie wszystkich wymienionych usług pozwoliło na stworzenie stosunkowo zaawansowanego bota.

## Architektura Bota

Stworzona architektura bota nie należy do skomplikowanych. Opiera się na 3 dialogach. Zostaną one omówione poniżej.

1. Dialog główny rozpoczyna rozmowę. Po przedstawieniu się, bot pyta użytkownika o imię w celu częściowej personalizacji dalszej części rozmowy. Dla tego dialogu przygotowane zostały 4 triggery, które odpowiadają klasom stworzonym w bazie LUIS-a.
2. Kolejny dialog pozwala na przeprowadzanie dosyć trywialnego doboru odpowiedniego ciągnika. Użytkownik w trakcie tej części rozmowy proszony jest o podawanie kolejnych informacji. Dialog ten uruchamiany jest przez wyzwalacz "buy". Przed rozpoczęciem doboru ciągnika, bot pyta, czy na pewno chcemy przeprowadzić taką operację
3. Ostatni dialog jest przykładem trywialnym i polega na pożegnaniu się bota  i zakończeniu wszystkich aktywnych dialogów. Wyzwalany jest poprzez trigger "cancel".
4. Wyzwalacz "question" pozwala na odpowiedzenie użytkownikowi, zachęcając go do zadawania pytań
5. wyzwalacz "help" wyświetla dostępną pomoc, która zawiera dostępne ścieżki rozmowy.

## Napotkane problemy

Podczas przygotowywania bota napotkano kilka problemów. Część z nich postaram się omówić poniżej.

1. Trudności w wykorzystaniu serwisu LUIS w inny sposób niż triggery. 

2.  Trudności związane z debugowaniem
3. Pierwsze zetknięcie się z prawdziwym zadaniem na chmurze. Poza wcześniejszymi ćwiczeniami nie miałem okazji korzystać z żadnych dostępnych serwisów.

## Sposoby na dalszy rozwój bota

Zdaję sobie sprawę z tego, że przygotowany przeze mnie bot nie jest idealny. Poniżej zamieszczę listę rzeczy, które mogą zostać rozwinięte w kolejnych wersjach programu.

1. Rozwinięcie bazy pytań i odpowiedzi w celu pokrycia większej części najczęściej zadawanych pytań. 
2. Dodanie większej liczby przykładów do każdej z klas.
3. Wykorzystanie usługi, która pozwoli na tłumaczenie ludzkich odpowiedzi na inne języki. W ten sposób bot będzie mógł rozmawiać w wielu językach.
4. Rozwój doboru odpowiedniego ciągnika. W naszym przypadku proces ten jest liniowy i nie opiera się na żadnym mechanizmie Machine Learning. Można również powiększyć bazę dostępnych ciągników / pobierać dane z zewnętrznej bazy danych. Dodać wycenę. 

## Podsumowanie

Dzięki wykorzystaniu Bot Framework Composera udało się stworzyć nietrywialnego bota, który po dopracowaniu mógłby służyć na stronie internetowej pracodawcy, lub na innym serwisie społecznościowym. Tworzenie bota nie okazało się bardzo trudne, jednak wymagało bardzo dużo czasu. Dodatkowo bardzo pomocne okazały się oficjalne dokumentacje usług oraz rozmaite fora, w których znalazłem odpowiedzi na nurtujące mnie pytania.






