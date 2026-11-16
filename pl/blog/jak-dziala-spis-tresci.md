---
title: "Jak spis treści układa Twoje notatki?"
url: "https://sumizai.com/pl/blog/jak-dziala-spis-tresci.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Drzewo rozdziałów do sześciu poziomów, model, który odkłada notatki AI przez wybór numeru, i przebudowa całego vaulta porcjami po 60 notatek."
tags: ["automatyczny spis treści", "porządkowanie notatek AI", "drzewo rozdziałów", "konspekt markdown", "base.md", "sumizai"]
---

# Jak spis treści układa Twoje notatki?

Zapisywać jest łatwo. Folder z notatkami umiera przy odkładaniu na miejsce: po paru tygodniach nikt już nie decyduje, gdzie co ma leżeć, i robi się sterta. W SumizAI tę decyzję przy każdej z Twoich **notatek AI** podejmuje model, w strukturze na tyle ciasnej, że przy sześćsetnej notatce nadal jest spójnie. Poniżej: jak zbudowane jest drzewo, co poprawiasz ręcznie i kiedy kazać aplikacji ułożyć je od nowa.

## Jak wygląda spis treści?

To drzewo rozdziałów, najwyżej sześć poziomów, z jedną ciągłą numeracją: `1.` → `1.1` → `a)` → `a.1)` → `a.1.1`. Notatki są liśćmi i biorą numer z tego samego ciągu. W demonstracyjnym vaulcie _Ogród przydomowy_ _Wysiew pomidorów na rozsadę_ ma numer 1.2 w rozdziale _1. Warzywa_.

Numery nie są nigdzie zapisane. Liczą się z pozycji w drzewie, więc po przesunięciu rozdziału wszystko pod nim numeruje się samo.

To prawdziwa struktura, którą aplikacja utrzymuje, a nie widok składany w locie z tagów. Model da się poprosić o odłożenie notatki do struktury, do chmury tagów już nie. Tym SumizAI różni się jako alternatywa dla Obsidiana: Obsidian ma foldery, tagi i linki, ale konspekt prowadzisz tam wyłącznie Ty.

Obsidian alternatywa z gotowym spisem: każda notatka AI dostaje numer w tym samym ciągu co rozdziały, a obok tytułu widać podsumowanie.

## Jak notatka AI znajduje swój rozdział?

Model widzi rozdziały jako ponumerowaną listę i odpowiada **numerem**. Może też poprosić o nowy podrozdział pod istniejącym rozdziałem. Nowa gałąź główna powstaje tylko wtedy, gdy nic nigdzie nie pasuje.

Wybór zamiast nazywania to decyzja, na której stoi cały projekt. Wcześniejsza wersja kazała modelowi nazwać właściwy rozdział dla każdej notatki i drzewo rozsypało się na warianty jednej myśli: _Warzywa_, _Uprawa warzyw_, _Warzywa w ogrodzie_, trzy siostrzane gałęzie o tym samym. Numeru nie da się sparafrazować.

Pełnego spisu model też nie czyta. Dostaje skrót vaulta trzymany w 4000 znaków: mapę rozdziałów i krótkie wnioski, przycinane od najgłębszych poziomów, gdy się nie mieszczą. Koszt odkładania zależy więc od liczby rozdziałów, a nie od tego, ile napisałeś. Nazwa vaulta nigdy nie trafia na listę rozdziałów, a dwa rozdziały o tej samej nazwie z ogonkami i bez scalają się przy odczycie drzewa.

## A jeśli notatka trafi nie tam, gdzie trzeba?

Większość notatek AI model odkłada sensownie, resztę przesuwasz Ty. Drzewo jest w pełni edytowalne: przeciągnij notatkę albo rozdział w nowe miejsce lub użyj **Przesuń wyżej**, **Przesuń niżej**, **Zrób podrozdziałem rozdziału powyżej** i **Wysuń o jeden poziom**. Rozdział da się przemianować, dodać (**Dodaj rozdział**, **Dodaj podrozdział**) i usunąć.

Usunięcie rozdziału nie usuwa notatek. Okno potwierdzenia mówi to wprost (_Notatki zostaną w vaultcie_), a one przechodzą do rozdziału nadrzędnego.

Notatka bez rozdziału też nie ginie: w aplikacji stoi w grupie **Jeszcze nieuporządkowane**, a w `base.md` i w każdym eksporcie na końcu.

## Czy jedną rozmowę da się trzymać w jednym rozdziale?

Tak. Czat przypina się do rozdziału (drzewo oznacza go jako _Rozmowa przypięta do rozdziału_) i od tej chwili model odkłada notatki AI z tej rozmowy wyłącznie w poddrzewie tego rozdziału. Reszty drzewa nawet nie widzi, więc nie ucieknie do korzenia.

Przydaje się przy miesiącu pytań o podwyższone grządki: każda odpowiedź ląduje pod jednym nagłówkiem, a nowe podrozdziały rosną właśnie tam.

## Co robi Przebuduj spis treści, czego nie zrobi zwykłe odkładanie?

Patrzy na wszystko naraz. Odkładanie przy tworzeniu waży jedną notatkę wobec obecnego drzewa. To dobra decyzja przy tej wiedzy, jaką ma, ale nigdy nie naprawi struktury, która wykrzywiła się, zanim ta notatka powstała.

**Przebuduj spis treści** w pasku vaulta czyta wszystkie notatki porcjami po 60 i układa rozdziały od nowa Twoim głównym modelem, w tle. Notatka pominięta przez model zostaje na swoim miejscu. Nieudana odpowiedź nie rusza drzewa; przebudowa nie zatrzyma się w połowie, zostawiając bałagan.

Wynik ma jedną twardą regułę: drzewo ma być **płaskie, najwyżej cztery poziomy, bez rozdziału-parasola**, który zbiera całą resztę. Jeśli model go jednak zostawi, strażnik go zdejmuje. Korzeń nad korzeniem to dodatkowe kliknięcie i zero informacji.

## Kiedy przebudowa ma sens?

Po zrywie pracy, który zmienił kształt tego, co wiesz. Nie według kalendarza.

Sygnał: spis treści, który przewijasz zamiast czytać. Rozdział sensowny przy 20 notatkach AI, a teraz z 60, albo dwie gałęzie, które ciągle mylisz. Uruchom, obejrzyj wynik, popraw ręcznie to, z czym się nie zgadzasz. Powtarzanie jest bezpieczne.

Czemu cztery poziomy, skoro drzewo pozwala na sześć? Za głębokość płacisz przy każdym czytaniu, a zyskujesz na niej raz, przy zapisie. Sześć poziomów jest po to, żeby temat, który naprawdę tak się zagnieżdża, nie był zablokowany. Zostawiony sam sobie model chętnie zbuduje pięciopoziomową taksonomię dla 40 notatek, a Ty przez poziomy cztery i pięć będziesz tylko przeklikiwać.

## Jak spis treści wygląda na dysku?

Jako plik `base.md` w katalogu vaulta: konspekt w Markdownie ze względnymi linkami do plików w `notes/`. Jest generowany, nigdy pisany ręcznie, więc nie rozjedzie się z drzewem w aplikacji.

Dzięki niemu wyeksportowany vault jest dokumentem, a nie workiem plików `.md`. Otwórz `base.md` w Obsidianie, VS Code albo na GitHubie i indeks działa, bo linki to względne ścieżki między prawdziwymi plikami. Na stronie [Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html) opisuję resztę różnic; tutaj ta najważniejsza: porządek powstaje z Twoich rozmów, a i tak otwiera się w Obsidianie.

Import plików `.md`, `.txt` i `.pdf` działa tak samo: z każdego pliku powstaje notatka odłożona jak odpowiedź z czatu, a spis treści aktualizuje się po każdej z nich.

## Czy drzewo służy tylko do przeglądania?

Nie. To mapa, którą dostaje model. Z zaznaczonym **Korzystaj z notatek** każde pytanie idzie razem ze spisem treści vaulta, a aplikacja na jego podstawie i z pomocą wyszukiwarki wybiera najwyżej 5 notatek, wysyłanych w całości w limicie 24 000 znaków. Porządne drzewo wyostrza ten wybór, rozjechane go rozmywa.

W tej samej kolejności idzie każdy eksport: PDF (same podsumowania albo pełne notatki AI) i edytowalny PowerPoint z 15 motywami. Lepsze drzewo daje lepszy dokument dla kogoś innego. Resztę [aplikacji do notatek AI](/pl/) opisuje strona główna, a drogę notatki do drzewa tekst [jak odpowiedź z czatu staje się notatką](/pl/blog/jak-odpowiedz-z-czatu-staje-sie-notatka.html).

