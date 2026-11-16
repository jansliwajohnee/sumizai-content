---
title: "Czym jest vault i dlaczego jest granicą?"
url: "https://sumizai.com/pl/blog/czym-jest-vault-w-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Vault trzyma Twoje notatki AI, ich spis treści i ustawienia duplikatów, a do tego wyznacza granicę tego, co model widzi, kiedy zadajesz mu pytanie."
tags: ["vault notatek AI", "vault sumizai", "vault wiedzy", "granica kontekstu AI", "vault markdown", "sumizai"]
---

# Czym jest vault i dlaczego jest granicą?

W większości aplikacji notes albo folder służy do tego, żeby panel boczny wyglądał porządnie. W SumizAI pojemnik ma robotę do wykonania. **Vault decyduje, co widzi model**, co porównuje sprawdzanie duplikatów, co opisuje spis treści i co trafia do eksportu. Dobrze podzielone vaulty sprawiają, że notatki AI są przydatne także przy trzechsetnej.

## Czym dokładnie jest vault?

Nazwaną przestrzenią, do której należą cztery rzeczy: notatki, spis treści, rozmowy i ustawienia. Tworzysz ją przyciskiem **Utwórz vault**, nadajesz nazwę i od tej chwili każda odpowiedź zachowana z rozmowy w środku staje się jedną z jego notatek AI.

Na dysku to zwykły katalog w folderze, który wskazałeś na notatki. W środku leży `base.md` z wygenerowanym spisem treści, obok katalog `notes/` z jednym plikiem `.md` na notatkę. Lokalna baza indeksuje te pliki dla wyszukiwania i drzewa, ale notatkami są pliki. Kto zna Obsidiana, zna to słowo: tam vault też jest katalogiem plików Markdown, i dlatego ta aplikacja działa jako alternatywa dla Obsidiana bez żadnej konwersji.

Demonstracyjny vault Home garden: numerowane rozdziały, każda notatka odłożona pod jeden z nich.

Vault jest też jednostką, w której myśli aplikacja. Pytanie, sprawdzenie duplikatów, przebudowa spisu treści: każde z nich działa na dokładnie jednym vaulcie.

## Co granica vaulta znaczy dla notatek AI w praktyce?

Kiedy pytasz w vaulcie, model dostaje spis treści tego vaulta i pełną treść najwyżej 5 jego najtrafniejszych notatek, w limicie 24 000 znaków. **Notatki z innych vaultów nie trafiają tam nigdy.** Żadnego rankingu między vaultami, żadnych niespodzianek typu „powiązane z innego miejsca”.

Wyobraź sobie dwa vaulty. W _Home garden_ „grządka” to podwyższona grządka, a pytanie o nią wciąga Twoje notatki o kompoście i rozstawie. W vaulcie o umowie IT dla szpitala to samo słowo nie pada wcale albo znaczy coś innego. Notatki AI jednego vaulta nie przeciekają do odpowiedzi drugiego.

To również cecha prywatności, którą łatwo sprawdzić. Zapytanie idzie prosto z komputera do dostawcy, którego podłączyłeś, aplikacja pyta o zgodę przed wysłaniem, a materiał z vaulta, w którym nie pytasz, po prostu nie jest częścią zapytania.

## Jak wyznaczyć granice między vaultami?

Nie pytaj, o czym jest notatka. Zapytaj, **co powinno być w pokoju, kiedy o to pytasz**.

Takie pytanie daje mniej vaultów, za to większych, niż podział tematyczny, i to dobry wynik. Odpowiedzi są dobre dzięki kontekstowi. Vault z czterema notatkami AI nie da modelowi nic, czego nie dałby folder.

Szybki test dla pojedynczej notatki: zirytowałaby Cię odpowiedź, która ją pominęła? Wtedy należy do vaulta, w którym zadajesz to pytanie. Zirytowałaby Cię odpowiedź, która jej _użyła_? Wtedy jej miejsce jest w innym vaulcie, nawet jeśli temat brzmi podobnie i kusi, żeby trzymać wszystko razem.

## Jakie ustawienia należą do vaulta?

W **Ustawieniach vaulta** są dwie grupy.

**Duplikaty.** Tryb (pytaj, zawsze łącz albo zawsze twórz) i próg podobieństwa. Przed zapisem wyszukiwanie pełnotekstowe i trigramy szukają kandydatów w tym samym vaulcie, a drugi model ocenia każdego od 0 do 1. Powyżej progu decyduje tryb. W trybie pytaj notatki czekające na Twoją decyzję widać na stronie vaulta, nie tylko w czacie.**Język notatek.** Notatki powstają w języku vaulta bez względu na język wklejonego materiału; _Automatycznie_ idzie za notatkami, które już są w vaulcie. Język interfejsu to osobna sprawa, do wyboru jest 16.

Vault do nauki i vault prowadzony jak dziennik potrzebują innych odpowiedzi w sprawie duplikatów, i właśnie dlatego to ustawienie siedzi na vaulcie, a nie na koncie.

## Jak przenieść notatkę z jednego vaulta do drugiego?

Przez pliki, bo notatki to pliki. Klikasz **Pobierz vault**, dostajesz ZIP z `base.md` i `notes/`, bierzesz potrzebny plik `.md` i importujesz go do drugiego vaulta. Import przyjmuje `.md`, `.markdown`, `.txt` i `.pdf`, plik po pliku; zaimportowany tekst zostaje źródłem nowej notatki, a spis treści przebudowuje się po każdej.

Cały ZIP też da się wczytać z powrotem. Archiwum vaulta zaimportowane do aplikacji zawsze tworzy nowy vault, a nazwa, która już istnieje, dostaje przyrostek, zamiast cokolwiek nadpisać.

Tu aplikacja spotyka się z Obsidianem. ZIP używa zwykłych linków Markdown `[Tytuł](plik.md)`, a nie wiki-linków, więc rozpakowany katalog otwiera się jako vault Obsidiana z działającymi linkami. SumizAI jako [Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html) pisze notatki za Ciebie, a Obsidian zostaje czytnikiem tych samych plików.

## Ile vaultów mieć?

Mniej, niż Ci się wydaje. Klasyczny błąd to vault na projekt: dwadzieścia pojemników po cztery notatki, z których żaden na nic nie odpowie.

Działa jeden vault na _obszar myślenia_, który trwa dłużej niż pojedynczy projekt. Praca. Dziedzina, której się uczysz. Długie hobby, jak ogród. Projekty stają się rozdziałami w środku, a do tego służy spis treści do sześciu poziomów (`1.`, `1.1`, `a)`, `a.1)`).

Podział później to operacja na plikach, nie migracja. Eksport, wybór notatek, import tam, gdzie pasują.

## Co dzieje się z vaultami, gdy przestaniesz płacić?

Zostają do czytania. Po rezygnacji aplikacja nadal otwiera i eksportuje vaulty, przestaje tylko zaczynać nowe rozmowy. A skoro każda notatka AI to plik `.md` w Twoim katalogu, otworzy ją dowolny edytor tekstu, nawet bez aplikacji. Każda Obsidian alternatywa powinna przejść ten test: co się dzieje z plikami w dniu, w którym odchodzisz.

Licencja to podpisany token ważny 7 dni, więc tydzień offline to normalna praca, a nie blokada. Usunięcie konta też nie rusza vaultów: one i ich pliki zostają na komputerze. Jedyną niszczącą operacją jest usunięcie vaulta, dlatego aplikacja każe wpisać jego nazwę dla potwierdzenia.

## Czy vault jest współdzielony, czy tylko Twój?

Tylko Twój. Nie ma wspólnych vaultów, linków do udostępniania, wspólnej edycji ani synchronizacji między urządzeniami. Nie ma serwera z notatkami, a SumizAI nie zbiera notatek, pytań ani dokumentów.

Udostępniasz wynik: ZIP z Markdownem, PDF (same podsumowania albo pełne notatki) albo edytowalną prezentację `.pptx` z 15 motywami w kolejności spisu treści. Jeśli potrzebujesz zespołowej wiki z synchronizacją i wtyczkami, wybierz narzędzie do tego zrobione.

I praktyczna uwaga: nic nie jest jeszcze do pobrania. Aplikacja na macOS trafi wkrótce do Mac App Store, pozostałe platformy są w przygotowaniu, a po 7 dniach próbnych kosztuje 1 USD miesięcznie. Pełny opis znajdziesz na stronie [aplikacja do notatek AI](/pl/).

