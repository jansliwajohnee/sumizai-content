---
title: "Jak SumizAI chroni bibliotekę przed prawie-duplikatami?"
url: "https://sumizai.com/pl/blog/jak-sumizai-radzi-sobie-z-duplikatami.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Do 5 kandydatów z wyszukiwania pełnotekstowego i trigramów, ocena od 0 do 1, trzy tryby vaulta i scalanie, które w notatkach AI tylko dopisuje."
tags: ["duplikaty notatek", "scalanie notatek", "próg podobieństwa", "duplikaty notatek AI", "porządek w bazie wiedzy", "sumizai"]
---

# Jak SumizAI chroni bibliotekę przed prawie-duplikatami?

Zapytaj model o proporcje w kompostowniku w kwietniu, w czerwcu i jeszcze raz we wrześniu, a zwykła historia czatu da Ci trzy odpowiedzi w trzech miejscach. Folder z **notatkami AI** zrobiłby to samo, gdyby nic go nie zatrzymało: trzy pliki, każdy trochę lepszy od poprzedniego, żaden pełny. SumizAI stawia przed każdym zapisem jedno sprawdzenie, które łapie dokładnie to.

## Co się dzieje, zanim nowa notatka się zapisze?

Dwa przebiegi. Najpierw tani, potem drogi.

Pierwszy to wyszukiwanie. Szkic porównywany jest z vaultem wyszukiwaniem pełnotekstowym (SQLite FTS5 po tytułach, podsumowaniach, treści i materiale źródłowym) oraz podobieństwem trigramów. Razem dają krótką listę najwyżej 5 istniejących notatek AI. To praca bazy danych, trwa milisekundy.

Drugi to ocena. Pomocniczy model czyta szkic obok każdego kandydata i zwraca **wynik od 0 do 1 i jedno zdanie uzasadnienia**. Krótkie wywołanie, do 800 tokenów, na Twoim kluczu u dostawcy, jak wszystko inne. Porównanie szkicu przez model z 900 notatkami byłoby za drogie, a baza nie zrozumie, że dwa akapity mówią to samo. Każda strona robi to, w czym jest dobra.

## Po co dwie metody wyszukiwania?

Bo gubią co innego. Wyszukiwanie pełnotekstowe trzyma się słów i nie widzi tych, których nie użyłeś. Trigramy porównują trzyliterowe kawałki, więc łapią literówki, odmianę i podobne zapisy: _kompostownik_ i _kompostowanie_, _grządka_ i _grządki_.

Indeks usuwa też ogonki, a zapytanie przechodzi przez to samo. Po polsku pisze się bez ogonków z czystego nawyku (_zrodlo_ zamiast _źródło_), i gdyby tylko jedna strona była znormalizowana, takie notatki AI nigdy nie spotkałyby się jako kandydaci.

## Co znaczy wynik?

Czy dwa teksty są o _tym samym temacie_, a nie czy mają wspólne słowa. Tego żaden indeks nie zrobi.

Zdanie uzasadnienia waży tyle co liczba. „Oba podają proporcję brązowego do zielonego, nowy dodaje, jak często przerzucać pryzmę” mówi, co doda scalenie. „Oba wspominają kompost, ale jeden jest o pH gleby” mówi, czemu do niego nie dojdzie.

Wynik porównuje się z **Progiem podobieństwa** vaulta. Nowy vault zaczyna od 0,75. Wyżej znaczy mniej łączeń i więcej osobnych notatek, niżej odwrotnie.

## Który tryb wybrać dla vaulta?

Ustawienia vaulta mają trzy, w sekcji _Gdy notatka wygląda na duplikat_.

**Pytaj za każdym razem** to ustawienie domyślne. Okno _To wygląda na coś, co już masz_ pokazuje szkic, każdego kandydata z jego zgodnością i trzy przyciski: _Połącz z tą_, _Zapisz jako nową_, _Zdecyduję później_. Odłożone szkice czekają na stronie vaulta pod _Czekają na decyzję_.**Zawsze łącz** scala bliskie szkice samo, ale tylko powyżej progu. Dobre dla vaulta, który jest długą nauką kilku pojęć: wolisz dziesięć głębokich notatek niż sto płytkich.**Zawsze zostaw obie** nigdy nie łączy. Właściwe dla dziennika, w którym dwa wpisy o tym samym z różnych tygodni to naprawdę dwa wpisy.

Czat ma jedną różnicę. Notatki z rozmowy powstają w tle, gdy dalej piszesz, więc w trybie pytania czat Ci nie przerywa: szkic trafia do najlepszego kandydata powyżej progu. Zaznacz **Pytaj przed połączeniem** pod polem pytania, a ta rozmowa przywróci okno. Import też rozstrzyga bez pytania, bo nikt nie chce 40 okien po wrzuceniu katalogu PDF-ów.

## Co dzieje się z notatką AI przy scaleniu?

Materiał się dopisuje, nic się nie podmienia. Nowa treść dołącza do istniejącej notatki, a nowe pytanie i odpowiedź trafiają do jej źródła pod te, które już tam są, słowo w słowo.

Żadna ścieżka w kodzie nie zmieni ani nie usunie wcześniejszego materiału źródłowego, ani przypadkiem, ani celowo: warstwa zapisu po prostu nie ma takiej operacji. W edytorze z pustą kartką scalanie dwóch notatek należy do Ciebie i to, co wytniesz, przepada, jeśli nie masz kopii. Kto szuka hasła Obsidian alternatywa pod notatki z czatów AI, niech od tej różnicy zacznie.

Scalona notatka rośnie więc w dwóch warstwach: na wierzchu najlepsza obecna wersja myśli, pod spodem każda rozmowa, która ją zasiliła, własnymi słowami. Po pół roku nadal widać, która odpowiedź kazała przerzucać pryzmę co dwa tygodnie i w jakich warunkach.

Scalanie ręczne: zaznacz dwie lub więcej notatek AI na liście i kliknij Scal.

## Czy mogę scalić notatki sam?

Tak, gdy sprawdzenie czegoś nie złapało. Zaznacz notatki na liście **Notatki** i kliknij **Scal** albo użyj **Scal notatki** nad spisem treści.

Model pisze jeden szkic z tego, co zaznaczone notatki mówią dziś. Powstaje nowa notatka AI z materiałem źródłowym wszystkich, w kolejności ich powstania. Stare notatki znikają, a każdy odnośnik do ich plików zostaje przepisany na nowy plik. Model jest pytany najpierw i nic się nie zmienia, dopóki nie odpowie, więc gdy dostawca odmówi, vault zostaje taki, jak był.

## A kandydaci poniżej progu?

Są powiązani, ale nie tacy sami, a od powiązanych notatek AI są odnośniki. Szkic, który staje się nową notatką, dostaje krótką mapę istniejących notatek z tego samego wyszukiwania, tytuły i nazwy plików, i wplata do tekstu zwykłe linki Markdown: `[Sprawdzanie pH gleby](sprawdzanie-ph-gleby.md)`. Linki do plików spoza mapy są wycinane.

Dlatego próg warto stroić, a nie wyciągać w skrajność. Przy 0,95 powtórki przechodzą jako nowe pliki. Przy 0,4 łączą się notatki, które powinny zostać osobno, i znika link, który by je połączył.

## A jeśli scalenie poszło źle?

Nic nie przepadło, bo materiał źródłowy obu rozmów nadal jest w notatce, w całości. Otwórz ją i użyj **Przebuduj z materiału źródłowego**: materiał przechodzi przez cały proces jeszcze raz, a długi tekst wraca jako kilka powiązanych notatek w miejsce scalonej.

Wolisz ręcznie? Notatka to zwykły plik `.md` w katalogu `notes/` vaulta, więc podział to robota w edytorze tekstu.

Zwykłe pliki to też powód, dla którego SumizAI w ogóle stoi na liście, gdzie [Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html) jest głównym hasłem: logika scalania należy do aplikacji, pliki do Ciebie, a vault wyeksportowany jako ZIP otwiera się w Obsidianie. Jako alternatywa dla Obsidiana zamienia wtyczki na notatki, które same się piszą i pilnują powtórzeń. Resztę [aplikacji do notatek AI](/pl/) (vaulty, wyszukiwanie, eksport do PDF i PowerPointa) opisuje strona główna, a całą drogę odpowiedzi tekst [jak odpowiedź z czatu staje się notatką](/pl/blog/jak-odpowiedz-z-czatu-staje-sie-notatka.html).

