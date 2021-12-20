# projektNr8_symulacjaObs-ugiKlient-wPrzyOkienkachZWyliczaniemStatystyk	
Symulacja obsługi klientów przy okienkach z wyliczaniem statystyk

Opis zadania

Trzy okienka (na przykład w urzędzie) obsługują klientów przychodzących w jednej z dwóch spraw (A, B).

Okienka reprezentowane są przez obszary w dole okna programu z wyborem
(checkbox) spraw jakie są tam załatwiane i przyciskiem “Następny”.

Nowe osoby chcące cos załatwić reprezentowane są przez wciśnięcia jednego z czterech przycisków na górze okna programu (“A”, “B”, “VIP A”, “VIP B”).
Obok przycisków napisana jest liczba czekających klientów z daną sprawę.

Program automatycznie przydziela osoby do okienek w momencie naciśnięcia przycisku “Następny”. Osoby sę przyjmowane w koIejności przyjścia, najpierw z kolejek VIP, a następnie (gdy kolejka VIP jest pusta) ze zwykłych kolejek. Jeśli zwykle kolejki tez są puste, to następny pasujący klient który przyjdzie przyjmowany jest bez czekania.

Jeśli klient VIP czeka dtu2ej ni2 10 sekund, powinno sit wyświetIić okno z tekstem “To skandaliczne!”.

Klienci są reprezentowani przez klasy KlientZwykly i KIientVIP dziedziczące po
klasie Klient. Posiadają one metody wejście, wyjście i tick odpowiednio wywoływane przy wejściu klienta, jego wyjściu i co sekundę, rejestrujące odpowiednie czasy i reagujące na zdarzenia.

Program posiada również w głównym oknie przycisk “Zakończ” wyświetIający statystyki (średni czas oczekiwania w poszczególnych okienkach i w ogóle z rozbiciem na sprawy i bez) jak poniżej i resetujący stan. Wyświetlone maję być dwie tabele, osobno dla zwykłych klientów i klientów VIP.


Testy
1.	Ustawienie okienka pierwszego na obsługę spraw A, drugiego na obsługę spraw B, a trzeciego na obsługę obu typów spraw (dotyczy wszystkich podpunktów o ile nie wyszczególniono inaczej). Wpuszczenie klienta ze sprawę A, naciśnięcie obsługi przy okienku drugim, naciśnięcie obsługi przy okienku pierwszym, wpuszczenie klienta ze sprawę B (powinien od razu być załatwiony w drugim okienku), zakończenie.

2.	Wpuszczenie klienta A, wpuszczenie klienta VIP A, następny w  okienku pierwszym, następny w okienku trzecim. Czasy obsługi powinny wskazywać na to, ze klient VIP byt obstu2ony jako pierwszy.

3.	Wpuszczenie klienta VIP A, wpuszczenie klienta B, następny w okienku trzecim, następny w okienku drugim, zakończenie.

4.	Wpuszczenie klienta VIP B, wpuszczenie klienta A, następny w okienku trzecim, następny w okienku pierwszym, zakończenie.

5.	Wpuszczenie klienta A, zakończenie (podsumowanie powinno wskazywać czas od wejścia klienta do zakończenia).

6.	Wpuszczenie klienta A, wpuszczenie klienta VIP B, następny w okienku pierwszym, odczekanie do momentu wyświetIenia komunikatu o zbyt wolnej obsłudze.

7.	Wpuszczenie po czterech klientów każdego rodzaju i obsługa ich wszystkich w okienkach pierwszym i drugim. Zakończenie.
