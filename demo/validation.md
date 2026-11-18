# Sprawdzenie demo v2 w przeglądarce

Data: 18 listopada 2026. Weryfikowano lokalny plik w Chrome przez agent-browser w osobnej sesji. To sprawdzenie prototypu, nie odbiór systemu produkcyjnego i nie pomiar jakości modelu AI.

## Wykonane próby

- Przeklikano przyciskami przewodnika wszystkie 11 scenariuszy. Zakończone kroki: 13, 6, 7, 4, 4, 6, 8, 5, 6, 5, 4. Odczytano wynik modelu, a nie tylko obecność przycisku.
- Ścieżka główna: dwie umówione rozmowy, trzecie zaproszenie zamknięte jako skompletowany skład; obie strony potwierdziły wynik, dodano przykładową publikację i prywatną ocenę.
- Przegląd profilu zwykłymi formularzami: własna zmiana → operator podaje uzasadnienie → zatwierdzony profil w katalogu. Profil ustawiony jako przygotowany do pierwszego przeglądu zniknął z katalogu: 19 widocznych zamiast 20.
- Zwykłe kontrolki kontaktu: ekspert zaznaczył wyłącznie telefon. Numer nie był obecny w widoku dziennikarza przed potwierdzeniem; po umówieniu pojawił się wybrany telefon, bez niezaakceptowanego e-maila.
- Do prywatnego wątku wybrano lokalny plik tekstowy 65 bajtów, zapisano jego treść w pamięci i uruchomiono pobranie kopii. To nie test serwerowego magazynu i autoryzacji.
- Formularz odłożenia bez decyzji pozostawił temat aktywny i wskazał błąd przy konkretnej rozmowie. Po wyborze „zachowaj” temat został odłożony. Wznowienie zwykłym formularzem z nowymi osobami zachowało jedno wcześniejsze umówienie i utworzyło dwa zaproszenia oczekujące.
- Wykryty problem pozostawienia błędu po zmianie selecta poprawiono: stan błędu czyści się także na zdarzeniu change. Ponowiono i ukończono formularz odłożenia.
- Korekta publikacji przez eksperta nie nadpisała zatwierdzonego powiązania: zachowano grupę appearance-demo i potwierdzenie, a nową grupę zapisano jako oczekującą. Decyzja operatora zastosowała korektę, usunęła wersję oczekującą i zachowała dwa wpisy historii.
- Spór: rozbieżne wyniki → decyzja zespołu; 5 gwiazdek z negatywnym komentarzem → ostrzeżenie → przegląd bez ujawnienia → korekta autora na 2 → zakwestionowanie przez drugą stronę. Historia zachowała wersje i nie ujawniała zatrzymanej treści w odczycie ocenianej osoby.
- Podgląd kolejki: błąd dostarczenia i ponowienie zachowały jedno zdarzenie, ze zwiększoną liczbą prób.
- Pokrycie w interfejsie: 90 kart, 90 unikalnych identyfikatorów US; raport zawiera także 17 decyzji i 18 odniesień T.
- Szerokość 390 px: lista pokrycia, kolejka profili operatora, dostępność oraz skrzynka eksperta mieściły się bez przepełnienia strony. Szerokość 1440 px: katalog mieścił się bez przepełnienia. To emulacja rozmiaru, nie test fizycznego telefonu.
- Klawiatura: Tab z początku prowadził do odsyłacza pomijającego nawigację; po przejściu do dostępności kolejne Tab ustawiło fokus w polu miejscowości. Nowe ekrany kierują fokus na nagłówek, a błędne formularze na kontrolkę.
- Zachowana v1 pod /v1/ otworzyła katalog 20 profili bez roli operatora. Zwykłym formularzem zapisano temat, wracając do katalogu. Nowa v2 działa równolegle pod głównym adresem.
- Odsyłacz z parametrami role=operator&screen=coverage otworzył właściwą rolę i ekran z 90 kartami pokrycia.
- Nie odnotowano błędów JavaScript w odczycie konsoli używanej sesji po tych przebiegach.

## Czego nie sprawdzano

Realnego modelu, SMTP, sesji i zabezpieczeń, transakcji i wyścigów API, trwałego zapisu, dwóch urządzeń, restartu i backupu, rzeczywistych źródeł ani prawdziwych uczestników. Scenariusze T w specyfikacji pozostają kryteriami odbioru produkcyjnej implementacji.
