---
title: "Czego szuka wyszukiwarka SumizAI?"
url: "https://sumizai.com/pl/blog/jak-dziala-wyszukiwarka-w-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Jak przeszukujesz notatki AI: tytuł, podsumowanie, treść i oryginalna rozmowa z wagami, odporność na literówki i tryb czatu, który znajduje notatkę po sensie."
tags: ["wyszukiwanie notatek", "wyszukiwanie pełnotekstowe", "szukanie w notatkach AI", "szukanie po znaczeniu", "znajdź notatkę", "sumizai"]
---

# Czego szuka wyszukiwarka SumizAI?

SumizAI ma trzy sposoby szukania w notatkach AI i każdy odpowiada na inne pytanie. Pole _Szukaj w notatkach_ znajduje słowo. Tryb czatu _Szukaj w notatkach_ znajduje notatkę, gdy pamiętasz tylko, o czym była. _Znajdź w notatce_ (Cmd+F) znajduje frazę w otwartej notatce.

## Które części notatki AI czyta pole wyszukiwania?

Cztery, każda z własną wagą w rankingu: **tytuł** (10), **podsumowanie** (5), **treść** (2) i **materiał źródłowy** (1), czyli Twoje pytanie i odpowiedź modelu zapisane słowo w słowo pod notatką.

Ta czwarta znaczy więcej, niż sugeruje waga. Tytułu notatki prawie nikt nie pamięta. Pamięta się przykład z rozmowy, liczbę, nazwę produktu, która padła raz. Ten tekst też jest w indeksie, więc notatka o kompostowniku wyskoczy po wpisaniu _azot_, nawet jeśli to słowo stoi tylko w odpowiedzi sprzed trzech tygodni.

Wagi pilnują porządku. Trafienie w tytule wygrywa ze wzmianką głęboko w źródle.

## Co widzę w wynikach szukania w notatkach AI?

Tytuł, jednozdaniowe podsumowanie i, gdy trafienie jest w treści, krótki fragment (około 40 słów) z podświetlonymi słowami.

Lista notatek w demonstracyjnym vaulcie. Podpowiedź w polu mówi, w czym jest najlepsze: tytuł albo słowo z podsumowania.

Przy kilkudziesięciu notatkach AI o jednym temacie ten fragment oszczędza otwierania pięciu, żeby trafić na właściwą. Z listy widać, czy to notatka, w której ustaliłeś harmonogram podlewania, czy taka, gdzie padł mimochodem. To samo pole stoi nad spisem treści na stronie vaulta.

## Czy radzi sobie z ogonkami, odmianą i literówkami?

Z ogonkami tak. Indeks pomija znaki diakrytyczne, więc _pomidor_ i _pomidór_ to to samo słowo, a pisanie bez polskich liter nie jest błędem.

Odmianę obsługuje dopasowanie po początku słowa. Każde wpisane słowo jest traktowane jak przedrostek, więc _kompost_ znajdzie też _kompostownik_ i _kompostowanie_. Słownika form za tym nie ma, dlatego krótszy rdzeń (_pomidor_) łapie więcej niż pełna forma (_pomidorami_).

Literówki dostają drugie podejście. Gdy indeks słów nie zapełni strony wyników, aplikacja porównuje zapytanie z tytułami i podsumowaniami przez podobieństwo trigramowe i dokłada notatki z wynikiem powyżej 0,6. Lądują pod trafieniami dokładnymi.

Słowa w polu łączy AND: _rozsada pomidorów_ zwraca notatki z oboma słowami.

## Jak działa szukanie po znaczeniu?

To tryb czatu, na wypadek gdy wyszukiwarka słów nie ma się czego chwycić. Przykład, od którego się zaczęło: pytanie o „bibliotekę w Java Spring do FHIR”, a notatka mówi _HAPI FHIR_ i słowa _biblioteka_ nie zawiera.

Model pomocniczy rozpisuje pytanie na 3 do 8 haseł i dopisuje odpowiedniki angielskie oraz oczywiste nazwy własne, bo nazwy bibliotek i narzędzi pisze się po angielsku także w polskich notatkach.Pytanie i hasła idą do tej samej wyszukiwarki co pole, po 6 wyników na hasło. Notatka trafiona kilkoma hasłami idzie wyżej.Model główny widzi do 12 kandydatów (tytuł, nazwa pliku, podsumowanie, fragment do 400 znaków), odpowiada w 2 do 4 zdaniach i wymienia notatki z odpowiedzią jako odnośniki.

Ma odpowiadać wyłącznie z tych notatek, przyznać wprost, gdy żadna nie pasuje, i pominąć kandydata bez związku. Odnośniki w odpowiedzi są sprawdzane z plikami vaulta. Ten tryb nie tworzy nowych notatek AI: szukasz, nie piszesz.

Bez embeddingów i bez bazy wektorowej. Sens biorą na siebie dwa wywołania modelu u Twojego dostawcy (Claude, GPT, Gemini albo inny z 7 obsługiwanych), a każdy krok da się prześledzić.

## Jak wyszukiwarka łączy się z tym, co czyta model?

Ten sam indeks dobiera kontekst do zwykłego pytania. Model dostaje spis treści i pełną treść najwyżej 5 najtrafniejszych notatek w budżecie 24 000 znaków, a aplikacja pokazuje, których użyła.

Model nigdy nie czyta całego vaulta. Jeśli odpowiedź pomija jedną z Twoich notatek AI, na którą liczyłeś, wyszukaj ją sam: gdy pole też jej nie znajdzie, kłopot leży w słowach notatki, nie w modelu.

## Czy wyszukiwanie obejmuje jeden vault?

Tak. Każde zapytanie niesie vault: w polu, w trybie czatu i przy kontekście. Ogród i praca nigdy nie mieszają się w wynikach.

Pięćdziesiąt notatek AI o jednym temacie przeszukuje się łatwo, pięćset o wszystkim już nie, więc wolę najpierw otworzyć właściwy vault. Użytkownik Obsidiana zna ten pomysł: tam vault też jest katalogiem, i to jeden z powodów, dla których ta aplikacja sprawdza się jako alternatywa dla Obsidiana, a nie nowy format do nauki.

## Co, jeśli wyszukiwarka nie widzi notatki, która na pewno jest?

W ustawieniach vaulta uruchom _Sprawdź i napraw_. Indeks to dane pochodne: tekst do szukania jest liczony z plików `.md`, a w każdym sporze rację ma plik.

Sprawdzenie odtwarza z plików notatki, które wypadły z indeksu, i dopasowuje nazwy plików do tytułów. Notatki AI, która ma swój plik, nigdy nie usuwa.

## Obsidian alternatywa z wyszukiwarką do notatek z czatów

Notatki leżą na Twoim Macu jako zwykłe pliki Markdown, a lokalna baza obok służy za indeks. Wyszukiwanie nie wychodzi poza komputer; wyjątkiem są dwa wywołania modelu w trybie czatu, które idą prosto do dostawcy, którego klucz podałeś.

Dlatego SumizAI jako Obsidian alternatywa ma sens przy jednym zadaniu: AI pisze i odkłada notatki, szukasz ich tutaj, a ten sam katalog dalej otwiera się w Obsidianie, gdy chcesz wtyczek albo grafu. Kompromisy, w tym brak synchronizacji, opisuje strona [Obsidian alternatywa: porównanie](/pl/alternative-to/sumizai-alternative-to-obsidian.html).

Jeśli jesteś tu pierwszy raz, [aplikacja do notatek AI](/pl/) na stronie głównej pokazuje całą drogę od odpowiedzi w czacie do notatki. Wersja na Maca trafi wkrótce do Mac App Store; po 7 dniach próby kosztuje 1 USD miesięcznie.

## A Znajdź w notatce?

Cmd+F otwiera nad notatką pasek wyszukiwania z licznikiem („3 z 7”), przyciskami następnego i poprzedniego trafienia oraz podświetleniem. Aplikacja przejmuje ten skrót celowo, bo okno, w którym działa, nie ma własnego paska znajdowania.

Przydaje się przy długich notatkach z PDF-a albo dużego importu.

