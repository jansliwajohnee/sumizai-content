---
title: "Jak zamienić vault w PDF albo prezentację?"
url: "https://sumizai.com/pl/blog/eksport-notatek-do-pdf-i-powerpointa.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Vault z notatkami AI zamienisz w ZIP z plikami Markdown, PDF z podsumowaniami albo pełnymi notatkami, lub edytowalny plik .pptx z 15 szablonami."
tags: ["eksport notatek do pdf", "notatki do powerpointa", "markdown do pptx", "prezentacja z bazy wiedzy", "eksport pdf", "sumizai"]
---

# Jak zamienić vault w PDF albo prezentację?

Vault z notatkami AI, który urósł z czterdziestu rozmów, ma już porządek: każda notatka wybrała rozdział w dniu, w którym powstała. **Eksport zamienia ten porządek w plik** jednym kliknięciem, a Ty wybierasz, w jaki.

## W co da się zamienić vault z notatkami AI?

W trzy rodzaje plików, pod czterema przyciskami na pasku _Eksport_ nad vaultem: _Pobierz vault_, _PDF_, _PDF+_ i _PowerPoint_. Każdy bierze wszystkie notatki AI z vaulta naraz.

_Pobierz vault_ zapisuje ZIP z plikami dokładnie takimi, jakie leżą na dysku. _PDF_ i _PDF+_ dają jeden dokument w dwóch poziomach szczegółowości. _PowerPoint_ tworzy plik `.pptx`, który otworzysz i poprawisz jak każdą inną prezentację.

## Co jest w archiwum ZIP?

Katalog nazwany jak vault, w nim `base.md` i wszystkie notatki w `notes/`. Układ jest ten sam co na dysku, więc po drodze nic się nie konwertuje.

`base.md` to spis treści w Markdownie: rozdziały z numerami (`1.`, `1.1`, `a)`), a pod każdym link w rodzaju `[Wysiew pomidorów w domu](notes/wysiew-pomidorow-w-domu.md)`. Notatki, których model jeszcze nie przydzielił, mają osobną listę, więc żaden plik nie wypada ze spisu.

Wszystkie linki są względne. Po rozpakowaniu katalog działa w VS Code, na GitHubie i w Obsidianie. Z tej drogi korzystają osoby, dla których SumizAI to Obsidian alternatywa do pisania, a czytają dalej w Obsidianie; opisuje to strona [SumizAI jako alternatywa dla Obsidiana](/pl/alternative-to/sumizai-alternative-to-obsidian.html).

## PDF czy PDF+?

_PDF_ daje jedną stronę w formie slajdu na notatkę, z tytułem i podsumowaniem. _PDF+_ daje taką samą stronę z pełną treścią: podsumowaniem i rozwinięciem.

To dwa różne dokumenty, a nie jeden z innym rozmiarem czcionki. Weź przykładowy vault o ogrodzie: krótka wersja to ściąga na dziesięć minut, lista tego, czego się dowiedziałeś o rozsadzie, ziemi i podlewaniu. Długa to podręcznik, który trzymasz otwarty przy pracy.

W obu strony idą według spisu treści, a każda notatka ma numer taki jak w aplikacji. Pierwsza strona niesie nazwę vaulta.

## Dlaczego polskie znaki nie znikają z PDF-a?

Bo font jedzie w pliku. Czternaście standardowych fontów PDF-a nie ma ani jednej polskiej litery, a font wzięty z systemu odbiorcy dawałby inny dokument na każdym komputerze. Aplikacja osadza więc w każdym PDF-ie cały plik fontu DejaVu.

Dlatego do wysyłki poza firmę bezpieczniejszy jest PDF. Plik PowerPointa gra według zasad PowerPointa i korzysta z fontów komputera, na którym go otwierasz, jak każda prezentacja.

## Jak wygląda prezentacja?

Jeden slajd na notatkę, w kolejności spisu treści, z tytułem i podsumowaniem każdej notatki AI. Przed eksportem wybierasz _Szablon_: piętnaście, w trzech grupach po pięć.

**Proste**: Klasyczny, Ciepły, Chłodny, Nocny, Leśny. Tekst na jednolitym tle.**Z grafiką**: Indygo (pas boczny), Grafit (nagłówek), Morski (dwie kolumny), Bursztyn (narożnik), Śliwka (karta).**Z ilustracją**: Elektronika, Przemysł, Laboratorium, Karaiby, Medyczny. Pas z rysowanym motywem: układ scalony ze ścieżkami, sylweta fabryki, kolby i probówki, morze z palmami, linia EKG.

Ilustracje są rysowane w kodzie jako kształty, a nie wklejane z banku zdjęć, więc motyw wygląda tak samo na slajdzie 3 i 43. Każda para kolorów tekstu i tła spełnia progi kontrastu WCAG (4,5:1 dla tekstu, 3:1 dla dużego kroju), co ma znaczenie, kiedy rzutnik spłaszcza kolory. Domyślny jest Klasyczny: grafit na bieli.

## Czy rozmowa trafia na slajd?

Nie, ani w PDF-ie, ani w PowerPoincie. Twoje pytanie i surowa odpowiedź modelu zostają w notatce jako jej źródło, nietknięte, ale żaden eksport nie pokazuje ich publiczności. Zapis czatu na slajdzie jest gorszy niż pusty slajd.

Znaczniki Markdown też znikają: `##` i `**` odpadają, punkty list stają się kropkami, a bloki kodu nie trafiają na slajd.

## Skąd sensowna kolejność w eksporcie?

Kolejność powstała wcześniej, notatka po notatce. Przy zapisie notatki AI model wybiera istniejący rozdział po numerze albo prosi o nowy podrozdział, a drzewo sięga sześciu poziomów.

Eksport tylko to rysuje. Aplikacje z płaską listą notatek muszą wymyślić porządek w chwili eksportu, i stąd ich wynik wygląda jak lista posortowana po dacie.

Reguła praktyczna: **poprawiaj spis treści, nie slajdy**. Jeśli rozdziały wychodzą w złej kolejności, popraw spis treści w aplikacji albo przebuduj go i wyeksportuj jeszcze raz. To szybsze niż przesuwanie czterdziestu slajdów.

Spis treści vaulta o ogrodzie. Strony PDF-a i slajdy trzymają się dokładnie tej numeracji.

## Ile poprawek wymaga wynik?

Nastaw się na cięcie. Dostajesz kompletny, dobrze ułożony szkic każdej notatki AI z vaulta, a dobre wystąpienie korzysta z części.

Odpada wieczór pracy: ustalanie kolejności, pisanie linijki podsumowania do każdej sekcji i formatowanie czterdziestu slajdów tak samo. Plik `.pptx` to prawdziwy PowerPoint, więc skracasz go w Keynote, PowerPoincie albo Prezentacjach Google.

## Czy wyeksportuję tylko część vaulta?

Nie wprost. Eksport obejmuje cały vault, więc wycinek to edycja wyniku albo podział vaulta.

Jednorazowo usuń zbędne slajdy. Vault z sześćdziesięcioma notatkami AI daje sześćdziesiąt slajdów; zostaw te, których potrzebuje publiczność. Jeśli ciągle eksportujesz ten sam rozdział dla tych samych ludzi, niech będzie osobnym vaultem, bo vault wyznacza też granicę tego, co widzi pytanie. Jak notatki powstają, trafiają do rozdziałów i dają się szukać, opisuje [aplikacja do notatek AI](/pl/).

## Czy eksporty zostają po rezygnacji z subskrypcji?

Tak. Po rezygnacji notatki dalej się otwierają, a każdy przycisk eksportu działa; aplikacja przestaje tylko zaczynać nowe rozmowy. Pliki `.md` cały czas leżały na Twoim dysku, a ZIP to ten sam katalog w kopercie. Mało która aplikacja do notatek ma tak krótkie wyjście i to jeden z powodów, dla których zwykłe pliki bronią się jako alternatywa dla Obsidiana: odejście nic nie kosztuje.

