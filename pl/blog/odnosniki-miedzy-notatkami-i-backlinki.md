---
title: "Jak notatki linkują do siebie i co prowadzi z powrotem?"
url: "https://sumizai.com/pl/blog/odnosniki-miedzy-notatkami-i-backlinki.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Jak SumizAI łączy notatki AI: zwykłe linki Markdown w zdaniach, tylko do istniejących plików, lista backlinków pod notatką i zmiana tytułu bez martwych linków."
tags: ["backlinki", "linki markdown między notatkami", "powiązane notatki AI", "odnośniki w notatkach", "przebudowa odnośników", "sumizai"]
---

# Jak notatki linkują do siebie i co prowadzi z powrotem?

Odnośnik między dwiema notatkami AI w SumizAI to fragment zdania, który prowadzi do innego pliku `.md` w tym samym vaulcie. Nic więcej. Wstawia go model piszący notatkę, aplikacja sprawdza, czy plik docelowy istnieje, a pod każdą notatką stoją dwie listy: _Odnośniki z tej notatki_ i _Notatki, które tu prowadzą_.

## Jak wygląda odnośnik w notatce AI?

Jak każdy link Markdown: `[Wysiew pomidorów na rozsadę](wysiew-pomidorow-na-rozsade.md)`. Etykietą jest tytuł drugiej notatki, celem nazwa jej pliku w katalogu `notes/` vaulta.

Wiki-linków nie ma. W plikach nie znajdziesz `[[Wysiew pomidorów na rozsadę]]`, bo podwójne nawiasy to zwyczaj kilku edytorów, a zwykłą formę czyta każdy podgląd Markdown, GitHub i VS Code, bez żadnej wtyczki.

Odnośnik stoi tam, gdzie pasuje do treści. Notatka o kompostowniku mówi na przykład, że dojrzały kompost trafia do podłoża opisanego w notatce o rozsadzie, i właśnie te słowa niosą link. Osobnego bloku _Powiązane_ na końcu nie ma.

Wcześniejsza wersja aplikacji trzymała odnośniki w tabeli bazy i rysowała z niej sekcję „Powiązane”. W prawdziwych vaultach ta sekcja była pusta, bo nic tej tabeli nie wypełniało. Przeniesienie odnośnika do tekstu rozwiązało sprawę na dobre: link jest w pliku albo go nie ma.

## Kto decyduje, co zostanie połączone?

Model, który pisze notatkę. Tyle że nie dostaje wolnej ręki.

Przed pisaniem dostaje mapę **do 8 istniejących notatek**: tytuł po lewej, nazwa pliku po prawej. Kandydatów wybiera wyszukiwarka vaulta na podstawie opracowywanego materiału. Gdy znajdzie mniej niż 5, aplikacja dopełnia listę ostatnio zmienianymi notatkami tego vaulta, żeby model miał z czego wybierać. Ma wpleść link w zdanie, w którym związek jest prawdziwy, a nie dopisać listę.

Potem przy zapisie działa filtr. Każdy link do pliku `.md` spoza mapy znika, a jego etykieta zostaje jako zwykły tekst. Zewnętrzne adresy `https://` zostają bez zmian.

## Dlaczego nie ufać modelowi w nazwach plików?

Bo je wymyśla. Poproś o link do notatki o kwasowości gleby, a dostaniesz `kwasowosc-gleby.md`: rozsądną nazwę pliku, którego nie ma (prawdziwy to `sprawdzanie-ph-gleby.md`).

W vaulcie pełnym notatek AI martwy link kosztuje więcej niż brak linku. Klikasz, nic się nie otwiera i od tej chwili nie ufasz pozostałym. Dlatego reguła jest ostra: model wybiera zdanie, aplikacja decyduje, które cele są prawdziwe.

Ta sama kontrola działa w trybie _Szukaj w notatkach_, gdzie odpowiedź wskazuje notatki odnośnikami. Są sprawdzane z plikami vaulta, zanim odpowiedź zostanie zapisana.

## Skąd się biorą backlinki?

Każda notatka AI czyta listę wychodzącą prosto z pliku. Przychodzącej tak się nie da: odpowiedź na pytanie „kto tu prowadzi?” wymagałaby otwarcia wszystkich plików vaulta przy każdym wejściu w notatkę.

Aplikacja trzyma więc w lokalnym indeksie kolumnę pochodną z celami odnośników każdej notatki i tam szuka bieżącej nazwy pliku. Nazwa jest otoczona spacjami, dzięki czemu `gin.md` nigdy nie trafi w `login.md`.

Kolumnę da się w każdej chwili odbudować z plików. Źródłem zostaje plik, indeks tylko szybciej odpowiada.

## Co się dzieje z odnośnikami po zmianie tytułu?

Idą za notatką. Nazwa pliku to slug tytułu (małe litery, bez ogonków, najwyżej 60 znaków), więc nowy tytuł daje nowy plik. Każde `](stara-nazwa.md)` w pozostałych notatkach vaulta jest przepisywane na nową nazwę.

Kolejność jest stała: zapis nowego pliku, przepisanie odwołań, usunięcie starego. Jeśli coś zawiedzie w połowie, przepisane notatki wracają do poprzedniej treści, a nowy plik znika. Dwa tytuły o tym samym slugu dostają przyrostek `(1)`, `(2)`, a link zapisany z przyrostkiem lub bez niego i tak trafia we właściwy plik.

Jeden koszt jest znany i przyjęty: ZIP pobrany przed zmianą tytułu zachowuje stare nazwy.

## Czy da się przebudować odnośniki w całym vaulcie?

Tak. Na stronie spisu treści vaulta jest przycisk _Przebuduj odnośniki_. Przechodzi każdą notatkę, wycina linki prowadzące donikąd i dokłada brakujące wprost w zdaniach. Działa powoli, w tle, notatka po notatce.

Pasek vaulta: _Przebuduj odnośniki_ obok _Pobierz vault_ oraz eksportu do PDF i PowerPointa.

Najlepiej po imporcie. Notatki AI z katalogu plików `.md`, `.txt` czy `.pdf` powstają po kolei, więc pierwsze nie miały jeszcze sąsiadów.

Na drobniejsze naprawy jest _Sprawdź i napraw_ w ustawieniach vaulta. Działa bez modelu: link `notes/kompost.md` albo `../notes/kompost.md` zostaje poprawiony na `kompost.md`, bo liczy się sama nazwa pliku.

## Czy mogę dopisać odnośnik ręcznie?

Tak, i zachowa się tak samo jak linki w notatkach AI napisanych przez model. Wygenerowany odnośnik to zwykły link Markdown, więc wpisany ręcznie niczym się od niego nie różni.

Wskaż prawdziwą nazwę pliku z `notes/`, zapisz, a link pojawi się na liście wychodzącej. Notatka po drugiej stronie pokaże Twoją pod _Notatki, które tu prowadzą_.

Moje poprawki i poprawki aplikacji żyją w jednym formacie i każdą sprawdzę edytorem tekstu albo samym Obsidianem.

## Obsidian alternatywa, która nie psuje linków przy eksporcie

_Pobierz vault_ daje ZIP z `base.md` (spis treści) i katalogiem `notes/`, a wszystkie linki między notatkami to względne nazwy plików. Rozpakuj, otwórz katalog w Obsidianie, a widok grafu narysuje połączenia bez wtyczki i bez migracji.

Kto szuka alternatywy dla Obsidiana, powinien sprawdzić najpierw ten szczegół: czy eksport zachowuje linki, które Obsidian rozumie. Tutaj zachowuje. SumizAI jako Obsidian alternatywa ma sens dla kogoś, kto chce, żeby notatki z rozmów z AI pisały się same, a wynik dalej był katalogiem do otwarcia w Obsidianie. Pełne porównanie, razem z tym, z czego rezygnujesz (wtyczki, Canvas, synchronizacja), jest na stronie [SumizAI: Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html).

Jak jedna odpowiedź staje się notatką, pokazuje strona główna, czyli [aplikacja do notatek AI](/pl/) w skrócie. Cena: jeden plan za 1 USD miesięcznie po 7 dniach próby. Wersja na Maca trafi wkrótce do Mac App Store; dziś żadnej wersji nie da się pobrać.

## Co odnośniki zmieniają przy następnym pytaniu?

Mniej, niż się wydaje, i to celowo. Przy pytaniu w vaulcie model dostaje spis treści i pełną treść najwyżej 5 trafnych notatek w budżecie 24 000 znaków. Nie chodzi po linkach, żeby dobrać więcej.

Linki są dla Ciebie. Zamieniają zbiór notatek AI w coś, po czym da się chodzić: od kompostu do podłoża, stamtąd do temperatury kiełkowania (22–25 °C w demonstracyjnym vaulcie) i z powrotem przez backlinki.

