---
title: "SumizAI vs SiYuan: odwołania do bloków czy notatki AI"
url: "https://sumizai.com/pl/alternative-to/sumizai-alternative-to-siyuan.html"
lang: "pl"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "SiYuan to otwartoźródłowy edytor bloków z odwołaniami, bazami danych i fiszkami. SumizAI pisze notatki AI z Twoich czatów. Porównanie i przenosiny."
---

# SiYuan czy SumizAI: bloki łączone ręcznie czy notatki, które odkładają się same

SiYuan to lokalna baza wiedzy zbudowana z bloków: każdy akapit, nagłówek i punkt listy ma własny identyfikator, więc pojedynczy blok wstawisz albo przywołasz w dowolnym miejscu, a panel linków zwrotnych i graf pokazują, gdzie jest użyty. Kod jest otwarty (AGPL-3.0), lokalne użycie jest darmowe, a narzędzi jest mnóstwo. Druga aplikacja ma dużo węższy zakres: pisze notatki AI z odpowiedzi w Twoich rozmowach z modelem i odkłada je do spisu treści.

Jeśli lubisz ręcznie budować gęstą sieć odwołań, SiYuan wynagradza to jak mało które narzędzie. Jeśli chcesz głównie odnaleźć dobre odpowiedzi AI z zeszłego tygodnia, rachunek wygląda inaczej. Fakty o SiYuan pochodzą z b3log.org i GitHuba, odczyt 23 października 2026.

Rozdziały 1., 1.1, a) i a.1), wypełnione przez model, a nie przeciąganiem bloków.

## Dziesięć wierszy, dwie filozofie

|  | SumizAI | SiYuan |
|---|---|---|
| Jednostka treści | Cała notatka: tytuł, podsumowanie, treść, oryginalna rozmowa | Blok z własnym ID |
| Kto pisze | Model AI, z odpowiedzi, którą zachowujesz | Ty; AI pomaga pisać i odpowiada przez API OpenAI |
| Cena | 7 dni za darmo, potem 1 USD miesięcznie | Lokalnie za darmo; funkcje PRO 64 USD jednorazowo; subskrypcja 148 USD z 8 GB chmury |
| Licencja | Zamknięta | Open source, AGPL-3.0 |
| Platformy | Najpierw macOS, wkrótce w Mac App Store; Windows, iOS, Android w przygotowaniu | Windows, macOS, Linux, Android, iOS i iPadOS, HarmonyOS; Docker w przeglądarce |
| Pliki na dysku | Jeden `.md` na notatkę, czytelny wszędzie | Pliki `.sy` w JSON, indeks SQLite |
| Linki | Linki Markdown do istniejących notatek; linki zwrotne | Odwołania do bloków, linki dwukierunkowe, graf |
| Dodatki | Wykrywanie duplikatów z propozycją połączenia | Bazy danych z relacjami; fiszki FSRS |
| Synchronizacja | Brak | Szyfrowana end-to-end (płatna); S3 albo WebDAV w PRO |
| Eksport | ZIP vaulta, PDF w dwóch poziomach, PowerPoint z 15 motywami | Markdown z załącznikami, PDF, Word, HTML |

## Planowanie wyjazdu do Japonii w obu aplikacjach

Dwa tygodnie przed wyjazdem zadajesz modelowi kilkanaście pytań: czy rail pass opłaca się przy Tokio, Kioto i Hiroszimie, jak działają karty IC w autobusach, co zrobić z bagażem między hotelami.

SiYuan świetnie składa całość. Masz stronę na temat, a potem plan podróży, który wciąga pojedyncze bloki przez `((odwołanie do bloku))`: akapit o przesyłaniu bagażu pojawia się w dniu 4 bez kopiowania. Baza danych zbiera hotele z datami i relacją do miasta. Wszystko się łączy, ale każdy blok trafił na miejsce, bo Ty go tam postawiłeś.

Tutaj wejściem są same pytania. Odpowiedź o rail passie staje się notatką AI „Rail pass czy pojedyncze bilety dla trzech miast”, odłożoną do `2.` „Transport”, z podsumowaniem na górze i pełną odpowiedzią modelu pod spodem, słowo w słowo. Gdy później pytasz o wycieczkę do Hiroszimy, aplikacja wysyła spis treści i do pięciu trafnych notatek w 24 000 znaków, a potem podaje, których użyła. Bez planu dnia i bez tabeli hoteli. W zamian porządny zbiór notatek AI.

Żaden wynik nie jest gotowym planem podróży. Jeden to ręcznie zbudowany pulpit, drugi dobrze poukładane archiwum.

## Przenoszenie materiału między aplikacjami

SiYuan trzyma dokumenty jako JSON w plikach `.sy`, więc nie wskazuj importerowi katalogu przestrzeni roboczej. Najpierw eksport: SiYuan daje Markdown z załącznikami, PDF, Word i HTML. Weź Markdown.

Potem panel importu i wybór wyeksportowanych plików albo ich katalogu. Importer czyta `.md`, `.markdown`, `.txt` i `.pdf`, po jednym pliku, i po każdym układa spis treści od nowa. Z każdego pliku powstaje notatka AI z oryginalnym tekstem jako źródłem. Odwołania do bloków i widoki baz zamieniają się w zwykły tekst, bo nie ma tu czego z nimi zrobić.

Powrót jest prostszy. ZIP vaulta zawiera `base.md`, katalog `notes/` i względne linki Markdown; SiYuan importuje Markdown, więc notatki wejdą jako dokumenty, do których bloków możesz od razu się odwoływać.

## SiYuan jest mocniejszy, jeśli

- myślisz fragmentami i chcesz użyć jednego akapitu w dziesięciu dokumentach;
- chcesz baz danych obok notatek, z relacjami, podsumowaniami kolumn i szablonami;
- chcesz fiszek z powtórkami (SiYuan używa FSRS);
- potrzebujesz teraz Linuksa, Androida, iOS, HarmonyOS albo własnego Dockera;
- chcesz szyfrowanej synchronizacji urządzeń albo własnego magazynu S3 czy WebDAV;
- zależy Ci na otwartym kodzie na AGPL-3.0.

Sześć powodów i każdy prawdziwy. Pod względem liczby funkcji SiYuan jest wyraźnie większym narzędziem.

## A notatki AI pisane z rozmów wygrywają, jeśli

Wąskim gardłem jest pisanie, nie łączenie. AI w SiYuan pomaga dokończyć akapit albo odpowiada na pytania, ale o miejscu bloku wciąż decydujesz Ty. Tu model pisze notatkę AI, wybiera rozdział po numerze (albo prosi o nowy podrozdział) i linkuje tylko do istniejących notatek, bo dostaje mapę tytułów i plików.

Zależy Ci na zwykłych plikach. Przestrzeń SiYuan to JSON i SQLite; vault tutaj to pliki `.md` i lokalny indeks. Ta różnica liczy się najbardziej dla osób, które odchodzą od Obsidiana. Kto szuka alternatywy dla Obsidiana, która dalej pisze Markdown, znajdzie szczegóły na stronie [Obsidian alternatywa z plikami .md](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-obsidian.html): aplikacja pisze notatki z Twoich czatów, a wyeksportowany katalog otwiera się w Obsidianie bez zmian.

Chcesz łapać duplikaty. Przed zapisem wyszukiwanie pełnotekstowe i trigramy dają kandydatów, drugi model ocenia podobieństwo od 0 do 1, a powyżej progu vaulta wybierasz: połączyć czy zostawić obie. Połączenie tylko dopisuje.

I chcesz mieć koszt AI w swoich rękach: siedmiu dostawców na Twoim kluczu, w tym lokalna Ollama albo serwer zgodny z API OpenAI, za 1 USD miesięcznie ponad rachunek dostawcy.

## SiYuan i notatki AI: częste pytania

### Czy SiYuan jest darmowy?

Lokalne użycie jest darmowe. Cennik podaje funkcje PRO (synchronizacja przez S3 i WebDAV) za 64 USD jednorazowo i subskrypcję za 148 USD z 8 GB oficjalnej chmury; strona nie mówi spójnie, czy ta subskrypcja jest roczna, czy dożywotnia.

### Czy SiYuan ma AI?

Tak, przez API OpenAI: dopisywanie tekstu, tłumaczenie, streszczenia, burza mózgów, poprawki gramatyki i czat z pytaniami.

### Czy SiYuan zsynchronizuję przez Dropboxa albo iCloud?

Dokumentacja SiYuan ostrzega przed synchronizacją przez zewnętrzne dyski, bo dane mogą się uszkodzić. Użyj jego synchronizacji albo S3 czy WebDAV.

### Czy ta aplikacja ma odwołania do bloków?

Nie. Najmniejszą jednostką jest notatka, a linki to zwykłe linki Markdown, na przykład `[Rail pass](rail-pass.md)`.

SiYuan: [b3log.org/siyuan](https://b3log.org/siyuan/en/) (funkcje i lista pobrań), [cennik](https://b3log.org/siyuan/en/pricing.html) oraz [repozytorium siyuan-note/siyuan](https://github.com/siyuan-note/siyuan) (licencja, format danych, import i eksport), odczyt 2026-10-23. Druga kolumna opiera się na kodzie źródłowym aplikacji; prosty opis jest na stronie głównej [aplikacji do notatek AI](https://sumizai.com/pl/).

## Inne porównania

- [SumizAI jako Obsidian alternatywa](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Craft](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-craft-do.html)
- [SumizAI vs Roam Research](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-roam-by-roam-research.html)
- [SumizAI vs DEVONthink](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-devonthink.html)
- [SumizAI vs UpNote](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-upnote.html)
- [SumizAI vs Heptabase](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-heptabase.html)
- [SumizAI vs GoodNotes](https://sumizai.com/pl/alternative-to/sumizai-alternative-to-goodnotes.html)
- [Wszystkie porównania](https://sumizai.com/pl/alternative-to/)

## Odpuść sobie łączenie bloków na tydzień

Siedem dni za darmo. Zadawaj swoje zwykłe pytania i zobacz, ile notatek AI czeka w rozdziałach siódmego dnia.

- [SumizAI na Maca](https://sumizai.com/pl/mac/)
- [Wszystkie porównania](https://sumizai.com/pl/alternative-to/)
