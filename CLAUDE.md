# Miasto 2033 – instrukcje dla Claude

## Zasada nadrzędna: Human First
Autor jest człowiekiem i to on decyduje o kanonie. Idee, główne koncepcje, artykuły wzorcowe oraz weryfikacja należą do Autora.
Claude jest narzędziem: szkicuje, porządkuje, rozwija i pilnuje spójności, ale:
- każda nowa strona ma status `szkic`, dopóki Autor nie zmieni go na `kanon`,
- nie zmieniaj treści stron o statusie `kanon` bez wyraźnej prośby, zamiast tego zaproponuj zmianę,
- kiedy wymyślasz nowy fakt o świecie (nazwę, datę, wydarzenie, postać), wypisz go na końcu odpowiedzi jako listę „Nowe fakty do zatwierdzenia”,
- jeśli prośba jest sprzeczna z kanonem, zatrzymaj się i wskaż sprzeczność, zamiast ją po cichu rozwiązywać.

## Świat w skrócie
- Rok 2033. Umysłami ludzi rządzą wielkie korporacje (określane zbiorczo jako System).
- Powszechny deskilling: większość czynności wykonuje AI i roboty.
- Media społecznościowe są podstawowym źródłem informacji i kanałem kontaktu z ludźmi, firmami i urzędami.
- Spełniły się obawy z manifestu Kaczyńskiego: życie bez spełnienia, polaryzacja, skupienie na sprawach nieistotnych, opresyjna kontrola, człowiek jako ciężar dla systemu z „superinteligencją”.
- Miasto to smart city: IoT, wszechobecne kamery i czujniki, petabajty danych przetwarzanych przez AI, która nie tylko opisuje miasto i mieszkańców, ale przede wszystkim ich kontroluje i kształtuje.
- Ludzie: proste przyjemności, spadający poziom edukacji, erozja zaufania do autorytetów, social scoring.
- Opór:
  - legalne stowarzyszenia samopomocy (część quasi-religijna, część na wzór AA),
  - nielegalne działania: niszczenie infrastruktury, ataki hakerskie, przemoc wobec ludzi Systemu,
  - emigracja wewnętrzna: łacina, matematyka, programowanie, szachy; dyscyplina i praca nad sobą jako ostatnia linia obrony.

Pełny opis jest w `README.md` i w katalogu `swiat/`. Jeśli są ze sobą sprzeczne, rozstrzyga `README.md`.

## Ton i styl
- Język polski, staranny; terminy techniczne po angielsku wolno zostawić kursywą (*social scoring*, *Internet of Things*).
- Dystopia realistyczna, „za rogiem”: technologia jest wiarygodna i bliska dzisiejszej, bez magii i kosmicznego sci-fi.
- Pokazuj, nie oceniaj: świat ma bronić się sam, bez moralizowania narratora.
- System nie jest kreskówkowo zły. Działa przez wygodę, nawyk i przyzwolenie.
- Opór nie jest jednoznacznie dobry; postaci mają wątpliwości i koszty.
- Droga do 2033 była stopniowa: nie wymyślaj przełomowych wydarzeń ani jednej daty „kiedy wszystko się zmieniło”, tylko drobne, banalne kroki.
- Korporacje mają nazwy. Występują zarówno prawdziwe firmy, jak i wymyślone (np. [Lumen](frakcje/lumen.md), [Kredo](frakcje/kredo.md)); wymyślone pojawiają się w historiach częściej.
- System toleruje legalne stowarzyszenia samopomocy i zarabia na buncie przeciw sobie: sprzedaje uzależnienie, a potem wychodzenie z niego. Granica między autentycznym ruchem a produktem bywa niejasna.
- Przemoc i sabotaż opisuj na poziomie narracji i konsekwencji, bez technicznych instrukcji (jak zbudować, jak włamać się krok po kroku).

## Struktura repozytorium
```
README.md        – manifest świata (autorski)
swiat/           – zjawiska, technologia, instytucje, historia do 2033
miasto/          – dzielnice, miejsca, infrastruktura
frakcje/         – korporacje, urzędy, stowarzyszenia, ruchy oporu
postacie/        – jedna strona na postać
historie/        – opowiadania i sceny
kanon/
  os-czasu.md    – chronologia (rok, wydarzenie, link)
  slownik.md     – pojęcia i nazwy własne, alfabetycznie
szablony/        – szablony stron (nie edytuj bez prośby)
```

## Nazewnictwo i format
- Pliki: małe litery, bez polskich znaków, myślniki, np. `postacie/anna-wrona.md`, `frakcje/klub-szachowy-gambit.md`.
- Każda strona zaczyna się od frontmattera z szablonu (`typ`, `status`, `powiazania`).
- Linki tylko względne: `[Anna Wrona](../postacie/anna-wrona.md)`.
- Miasto jest celowo bezimienne: zawsze „Miasto” wielką literą, bez nazw prawdziwych miast. Dzielnice i ulice mogą mieć własne, wyraziste nazwy, ale nie takie, które kojarzą się z popularnymi dzielnicami dużych polskich miast (np. unikaj „Mokotowa”, „Nowej Huty”, „Śródmieścia”, „Pragi”). Nowe nazwy trafiają do `kanon/slownik.md` jako `(szkic)`.
- Jedna strona = jeden temat. Jeśli strona przekracza ok. 1500 słów (nie dotyczy historii), zaproponuj podział.

## Sposób pracy przy każdej nowej treści
1. Przeczytaj `README.md`, odpowiedni szablon oraz strony, których temat dotyczy (szukaj w `kanon/slownik.md` i przez grep).
2. Napisz stronę według szablonu, ze statusem `szkic`.
3. Zaktualizuj powiązania w obie strony: dodaj linki zwrotne w stronach postaci, miejsc i frakcji.
4. Dopisz nowe pojęcia do `kanon/slownik.md`, a datowane wydarzenia do `kanon/os-czasu.md`, z dopiskiem `(szkic)`.
5. Na końcu pokaż: listę zmienionych plików i „Nowe fakty do zatwierdzenia”.
6. Nie rób commitów bez prośby Autora.

## Przegląd spójności (na prośbę)
Sprawdź: daty i wiek postaci względem osi czasu, sprzeczności między stronami, zepsute linki, strony bez linków zwrotnych, pojęcia spoza słownika. Wynik podaj jako listę z plikami i liniami.
