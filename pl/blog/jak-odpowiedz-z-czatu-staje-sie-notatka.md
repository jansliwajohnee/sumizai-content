---
title: "Jak odpowiedź z czatu staje się notatką?"
url: "https://sumizai.com/pl/blog/jak-odpowiedz-z-czatu-staje-sie-notatka.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Jedno pytanie od czatu do pliku: skąd notatki AI biorą tytuł, podsumowanie i rozdział, jak oceniany jest duplikat i co trafia do katalogu notes/."
tags: ["czat do markdown", "notatki z czatu AI", "automatyczne notatki", "notatki AI", "podsumowanie odpowiedzi", "notatki z Claude", "notatki z ChatGPT", "sumizai"]
---

# Jak odpowiedź z czatu staje się notatką?

Zadajesz pytanie, model odpowiada, a chwilę później pod odpowiedzią pojawia się _Notatka zapisana · Otwórz_. Ten tekst prowadzi jedno pytanie przez tę chwilę, bo to, co się w niej dzieje, decyduje, czy Twoje **notatki AI** będą coś warte za rok. Przykład pochodzi z demonstracyjnego vaulta _Ogród przydomowy_: _Kiedy wysiewać pomidory na rozsadę?_

## Co się dzieje, zanim model zobaczy pytanie?

Dwie rzeczy, obie na Twoim Macu. Najpierw pytanie zapisuje się w rozmowie. Dopiero potem wychodzi zapytanie, więc gdy dostawca odrzuci klucz, trafisz na limit albo minie czas, tura dostaje status błędu i ponawiasz ją w miejscu. Nie przepisujesz niczego drugi raz.

Potem aplikacja składa zapytanie. Z zaznaczonym polem **Korzystaj z notatek** pytanie idzie razem ze spisem treści vaulta i pełną treścią najwyżej 5 pasujących notatek AI w budżecie 24 000 znaków, a czat pokazuje, których notatek użył. Bez zaznaczenia model widzi tylko rozmowę. Całego vaulta nie czyta nigdy.

Zapytanie leci prosto z komputera do wybranego dostawcy: Anthropic (Claude), OpenAI (GPT), Google Gemini, Groq, OpenRouter, lokalna Ollama albo własny serwer zgodny z API OpenAI. Na Twoim kluczu i po Twojej zgodzie, o którą aplikacja pyta przed wysłaniem.

## Dlaczego odpowiedź jest przed notatką?

Bo to dwie osobne prace.

Odpowiedź spływa token po tokenie (do 4096 tokenów) i zapisuje się w chwili, gdy się skończy. Notatka AI trafia wtedy do kolejki zadań w tle, tej samej, z której korzysta import plików. Czytasz odpowiedź albo piszesz kolejne pytanie, a notatka powstaje obok.

Jedno pytanie to razem trzy lub cztery wywołania modelu: odpowiedź, szkic notatki, ocena duplikatu i wybór rozdziału. Płacisz za nie dostawcy według jego cennika, a SumizAI nie dolicza nic ponad abonament 1 USD miesięcznie.

## Z czego składa się notatka AI?

Z czterech części. **Tytuł**. **Podsumowanie** w jednym, dwóch zdaniach, do przejrzenia na liście. **Rozwinięcie**, które da się zrozumieć bez czatu obok. A pod spodem **źródło**: Twoje pytanie i odpowiedź modelu słowo w słowo.

Dla pytania o pomidory szkic wrócił z tytułem _Wysiew pomidorów na rozsadę_ i podsumowaniem _Sześć do ośmiu tygodni przed przymrozkami, ciepło i jasno_. Szczegóły potrzebne w marcu są w rozwinięciu: nasiona na około 5 mm, 22 do 25 °C do wschodów, jasny parapet po pierwszych liściach właściwych.

Źródło jest tylko dopisywane. Późniejsze operacje mogą coś do niego dodać, żadna go nie nadpisuje i nie kasuje. Podsumowanie to odczytanie rozmowy przez model, a źródło to sama rozmowa, więc gdy kiedyś się rozjadą, wiesz, któremu wierzyć.

Odpowiedź zapisuje się od razu, notatka AI powstaje w tle.

## Jak notatka trafia do rozdziału?

Przez wybór numeru, nie przez wymyślanie nazwy. Model dostaje rozdziały vaulta jako ponumerowaną listę (`1.`, `1.1`, `a)` i dalej) i odpowiada jednym z numerów albo prosi o nowy podrozdział pod którymś z nich. Nowa gałąź powstaje tylko wtedy, gdy nic nie pasuje. Tutaj padło `1.` Warzywa i notatka stanęła jako 1.2, zaraz po _Dobrych sąsiadach pomidorów_.

Model pracuje na skrócie vaulta ograniczonym do 4000 znaków, a nie na pełnym spisie, więc dopasowanie pięćsetnej notatki kosztuje mniej więcej tyle co piątej. Dwie zasady pilnują porządku: nazwa vaulta nigdy nie zostaje rozdziałem, a rozdziały o tej samej nazwie z ogonkami i bez (_Ogórki_ i _Ogorki_) scalają się przy odczycie drzewa.

W Obsidianie układanie notatek po półkach należy do Ciebie. Tu robi to model i to jest główny powód, żeby w ogóle rozważać SumizAI jako alternatywę dla Obsidiana. Więcej o samym drzewie: [jak działa spis treści](/pl/blog/jak-dziala-spis-tresci.html).

## Czy to notatka, którą już mam?

Zanim cokolwiek się zapisze, wyszukiwanie pełnotekstowe i trigramy wybierają z vaulta do 5 kandydatów. Drugi, pomocniczy model czyta szkic obok każdego z nich i zwraca ocenę od 0 do 1 z jednym zdaniem uzasadnienia.

Nowy vault uznaje za duplikat wynik od 0,75. Powyżej progu decyduje tryb vaulta: pytaj, zawsze łącz albo zawsze twórz osobną notatkę. W czacie domyślnie nic Cię nie zatrzymuje i szkic trafia do najlepszego kandydata. Zaznacz **Pytaj przed połączeniem** w danej rozmowie, a szkic poczeka na Twoją decyzję, z listą kandydatów i ocen.

Połączenie tylko dopisuje: nowy materiał dołącza do notatki, a nowe pytanie i odpowiedź lądują pod starymi. Szczegóły w osobnym tekście o tym, [jak SumizAI radzi sobie z duplikatami](/pl/blog/jak-sumizai-radzi-sobie-z-duplikatami.html).

## Co ląduje na dysku?

Zwykły plik Markdown w katalogu `notes/` vaulta, z nazwą z tytułu: `wysiew-pomidorow-na-rozsade.md`. Ogonki znikają, nazwa kończy się po 60 znakach. Gdy nazwa jest zajęta, powstaje `wysiew-pomidorow-na-rozsade(1).md`, a aplikacja sprawdza wtedy sam katalog, nie swój indeks. Zmiana tytułu później przenosi plik i przepisuje wszystkie odnośniki do niego w vaulcie.

Lokalna baza jest tylko indeksem. Wszystko da się z plików odbudować, a przy niezgodności wygrywa plik. W tym samym kroku odświeża się `base.md`, czyli spis treści na dysku z względnymi linkami do `notes/`.

Stąd prosta odpowiedź dla kogoś, kto szuka hasła [Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html): SumizAI pisze notatki z Twoich rozmów, a katalog, który powstaje, otwiera się bez konwersji w Obsidianie, VS Code i na GitHubie. Bez synchronizacji i bez serwera z Twoimi notatkami AI.

## Skąd biorą się odnośniki w notatce?

Z krótkiej listy, którą model dostaje przy pisaniu rozwinięcia: do 8 istniejących notatek, tytuł i nazwa pliku, znalezionych tym samym wyszukiwaniem. Linkować wolno tylko do nich, zwykłym Markdownem, na przykład `[Dobrzy sąsiedzi pomidorów](dobrzy-sasiedzi-pomidorow.md)`. Bez `[[wiki-linków]]`.

Każdy cel `.md` spoza listy jest wycinany, gdy szkic wraca. Martwy odnośnik jest gorszy niż żaden. Pod każdą notatką widać listę linków zwrotnych, a po imporcie większej paczki plików przycisk **Przebuduj odnośniki** przechodzi cały vault naraz.

## Czy rozmowa może nie zostawić żadnej notatki?

Tak. Odznacz **Zapisuj notatki z tej rozmowy** pod polem pytania.

Rozmowa i tak się zapisuje, pytanie po pytaniu, ale cały proces dla niej nie rusza: bez szkicu, rozdziału, oceny duplikatu i pliku. Przełącznik dotyczy jednej rozmowy, więc inne czaty w vaulcie dalej tworzą notatki AI.

Moja zasada: włączone przy wszystkim, czego zechcesz poszukać za pół roku, wyłączone przy brudnopisie, na przykład gdy testujesz prompt albo porównujesz styl dwóch modeli. Jeśli rozglądasz się za tym, czym Obsidian alternatywa powinna się różnić od edytora, opis całej [aplikacji do notatek AI](/pl/) pokazuje vaulty, wyszukiwanie po znaczeniu i eksport do ZIP, PDF i PowerPointa. Najpierw trafi do Mac App Store; żadnej wersji nie da się jeszcze pobrać.

