---
title: "Gdzie SumizAI trzyma Twoje notatki?"
url: "https://sumizai.com/pl/blog/gdzie-sumizai-trzyma-twoje-notatki.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Twoje notatki AI to zwykłe pliki .md w wybranym katalogu: osobny katalog na vault, base.md ze spisem treści, notes/ z notatkami. Baza danych jest tylko indeksem."
tags: ["lokalne notatki markdown", "notatki AI na dysku", "format pliku notatki", "bez vendor lock-in", "eksport notatek zip", "sumizai"]
---

# Gdzie SumizAI trzyma Twoje notatki?

Każda z Twoich notatek AI to zwykły plik `.md` w katalogu na Twoim Macu. Katalog wybierasz sam, otwierasz go w Finderze i jest w nim wszystko, co aplikacja wie o notatkach. Lokalna baza danych to indeks zbudowany z tych plików, więc gdy kiedyś się rozjadą, rację ma plik.

## Jak wygląda katalog z notatkami AI?

Wskazujesz go w Ustawieniach, w sekcji _Katalog notatek_: „Wszystkie vaulty trzymają swoje pliki .md w tym katalogu na Twoim komputerze”. W środku każdy vault ma własny katalog nazwany od vaulta. Demonstracyjny _Ogród przydomowy_ to `ogrod-przydomowy/`:

`base.md`: spis treści z rozdziałami `1.`, `1.1`, `a)` i dalej, z odnośnikami do notatek;`sumi.md`: krótki skrót vaulta, z którego model korzysta, żeby dobrać rozdział dla nowej notatki bez czytania wszystkiego;`notes/`: jeden plik `.md` na notatkę, na przykład `wysiew-pomidorow-na-rozsade.md`;`documents/`: zaimportowane pliki, każdy obok notatki, która z niego powstała.

Żadnego ukrytego katalogu z metadanymi, żadnego zamkniętego kontenera. _Zmień katalog_ sam przenosi pliki w nowe miejsce. Gdy katalog zniknie (odłączony dysk, zmiana nazwy w Finderze), aplikacja zgłasza brak dostępu i prosi o ponowne wskazanie. Notatki nie przepadają.

## Co jest w pojedynczym pliku notatki AI?

Otwórz `wysiew-pomidorow-na-rozsade.md` w dowolnym edytorze. Od góry:

frontmatter między liniami `---`: `id`, `title`, `summary`, `section` (rozdział), `created`, `updated`, język notatki i do trzech pytań na dalszą rozmowę;tytuł jako nagłówek `#` i treść notatki w punktach;opcjonalna sekcja `## Pełna treść` z dłuższą wersją;`## Materiał źródłowy`: Twoje pytanie i odpowiedź modelu słowo w słowo, każdy wpis z datą.

Ta sama notatka w aplikacji. Na dysku to `ogrod-przydomowy/notes/wysiew-pomidorow-na-rozsade.md`.

Do sekcji źródłowej tylko się dopisuje. Gdy do notatki zostaje dołączony duplikat, jego pytanie i odpowiedź lądują pod starymi. Nic nie jest nadpisywane.

Odnośniki do innych notatek to zwykłe linki Markdown w treści, `[Sprawdzanie pH gleby](sprawdzanie-ph-gleby.md)`, więc plik czyta się i przegląda poprawnie w każdym edytorze.

## Skoro pliki mają wszystko, po co baza danych?

Dla szybkości. Lokalna baza zna tytuły, podsumowania, położenie każdego pliku, tekst do wyszukiwania i listę celów odnośników. Odpowiada na pytania, na które pliki nie odpowiedzą tanio, jak „które notatki tu prowadzą?” albo „które pięć notatek najlepiej pasuje do pytania?”.

To indeks, nie druga kopia. W _Ustawieniach vaulta_ przycisk _Sprawdź i napraw_ porównuje go z katalogiem: plik znaleziony pod inną nazwą wraca do indeksu, notatki są odtwarzane z plików, nazwy plików dopasowywane do tytułów, a wpis bez pliku znika ze spisu treści.

Notatki AI da się więc poprawiać w innym edytorze. Po sprawdzeniu aplikacja czyta to, co naprawdę leży na dysku.

## Czy nazwy plików się zmieniają?

Tak, gdy zmienia się tytuł. Nazwa pliku to slug tytułu: małe litery, bez ogonków, najwyżej 60 znaków. Zmień tytuł notatki AI, a plik się przeniesie, i każdy odnośnik do niego w pozostałych notatkach vaulta zostanie przepisany.

Dwa tytuły o tym samym slugu dostają przyrostek `(1)`, `(2)`, ustalany według tego, co już leży w katalogu. ZIP pobrany przed zmianą zachowuje stare nazwy. Uważam, że to dobra cena za katalog, którego nazwy mówią, co jest w plikach.

## Jak zabrać vault ze sobą?

Kliknij _Pobierz vault_ na stronie vaulta. Dostajesz ZIP z `base.md` i katalogiem `notes/`, czyli vault taki, jaki jest, ze względnymi odnośnikami między plikami.

Rozpakuj i otwórz w Obsidianie, w VS Code albo wrzuć do repozytorium na GitHubie. Linki działają od razu, a graf Obsidiana pokazuje je bez wtyczki i bez skryptu migracji. Dla kogoś, kto szuka alternatywy dla Obsidiana, ten eksport jest siatką bezpieczeństwa: jeśli odejdziesz, vault idzie z Tobą jako katalog, który Obsidian już rozumie.

Stąd SumizAI jako Obsidian alternatywa: notatki AI piszą się same z Twoich rozmów, a na końcu masz lokalne pliki do otwarcia w Obsidianie. Z czego rezygnujesz (wtyczki, Canvas, synchronizacja), opisuje strona [SumizAI: Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html).

Poza ZIP-em jest PDF w dwóch poziomach (same podsumowania albo pełne notatki) i edytowalny PowerPoint `.pptx` z 15 motywami, ze slajdami w kolejności spisu treści.

## Co backupować?

Katalog notatek. Są w nim wszystkie Twoje notatki AI, w otwartym formacie.

Wystarczy Time Machine albo zwykła kopia. Bazę da się odbudować z plików, więc jej utrata kosztuje jedno _Sprawdź i napraw_, a nie notatki.

## Gdzie leży klucz do dostawcy AI?

W pęku kluczy macOS (Keychain), nie w katalogu notatek. To celowe: katalog kopiujesz, backupujesz, czasem trzymasz na dysku w chmurze, a klucz API nie ma z nim podróżować. Jeśli sprawdzasz, która Obsidian alternatywa z wbudowanym AI jest dla Ciebie, zapytaj każdą, gdzie trzyma klucz.

Klucz jest Twój (BYOK). Aplikacja obsługuje 7 dostawców: Anthropic (Claude), OpenAI (GPT), Google Gemini, Groq, OpenRouter, lokalną Ollamę i własny serwer zgodny z API OpenAI. Zapytania idą prosto z Twojego komputera do dostawcy, po Twojej zgodzie, a za model płacisz dostawcy. SumizAI nic nie dolicza.

## Czego nie ma w zapisie i czego nie ma w synchronizacji?

Nie ma serwera z Twoimi notatkami AI. SumizAI nie zbiera notatek, pytań ani dokumentów. Konto (adres e-mail) służy subskrypcji: 7 dni za darmo, potem 1 USD miesięcznie, jeden plan na wszystkie Twoje Maki.

**Nie ma synchronizacji między urządzeniami.** Dwa Maki to dwa osobne katalogi. Wolę napisać to tutaj, niż pozwolić Ci odkryć to po dwóch tygodniach pisania na niewłaściwym komputerze.

Po rezygnacji nic nie zostaje zablokowane. Notatki dalej się otwierają i eksportują; aplikacja przestaje tylko zaczynać nowe rozmowy. Wersja na Maca trafi wkrótce do Mac App Store, dziś żadnej wersji nie da się pobrać. Szerszy obraz daje strona [aplikacja do notatek AI](/pl/).

