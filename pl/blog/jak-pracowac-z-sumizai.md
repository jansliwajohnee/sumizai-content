---
title: "Jak właściwie pracować z SumizAI na co dzień?"
url: "https://sumizai.com/pl/blog/jak-pracowac-z-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Podłącz klucz dostawcy, załóż vault, zadawaj pytania, a notatki AI same trafią do rozdziałów. Rytm pracy od pierwszego pytania po eksport do PDF i .pptx."
tags: ["notatki AI", "jak używać sumizai", "workflow notatek AI", "konfiguracja vaulta", "notatki markdown workflow", "sumizai"]
---

# Jak właściwie pracować z SumizAI na co dzień?

SumizAI ma bardzo mało ustawień, a te, które ma, naprawdę coś zmieniają. **Konfiguracja zajmuje kilka minut.** Przydaje się wiedza, które trzy czy cztery decyzje podjąć świadomie, a które zostawić aplikacji, która pisze Twoje notatki AI.

## Jak wygląda pierwsze pięć minut?

Pięć kroków w tej kolejności: konto z adresem e-mail, podłączenie dostawcy AI, nowy vault, jedno prawdziwe pytanie, rzut oka na spis treści. Po czwartym kroku masz już pierwsze notatki, a piąty pokazuje, gdzie trafiły.

Podłączenie dostawcy to wklejenie własnego klucza API w ustawieniach. Na liście jest siedmiu: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, lokalna Ollama i dowolny serwer zgodny z API OpenAI. Zanim zamkniesz ekran, kliknij **Testuj połączenie**. To prawdziwe wywołanie, więc literówkę w kluczu zobaczysz od razu, a nie w połowie pierwszej rozmowy.

Ustawienia dostawców: wybierasz jednego z siedmiu, wklejasz klucz i klikasz Testuj połączenie.

Potem zapytaj o coś, co naprawdę chcesz wiedzieć. Bez testowych promptów. Odpowiedź spływa strumieniem, chwilę później zapisuje się notatka AI, a spis treści pokazuje ją już pod numerowanym rozdziałem.

## Jak zdecydować, co ma być osobnym vaultem?

Rozstrzyga jedno pytanie: **kiedy pytam o to, co jeszcze model powinien widzieć?** Wszystko, co ma być w zasięgu wzroku, idzie do jednego vaulta. Reszta gdzie indziej.

Vault to twarda granica. Pytanie zadane w środku idzie ze spisem treści tego vaulta i jego notatkami, a z innych vaultów nie dostaje niczego. Dokładnie tego chcesz, kiedy projekt dla klienta i hobby używają słowa „grządka” w zupełnie innym sensie.

Myśl szeroko. Vault z czterdziestoma notatkami AI daje modelowi materiał do pracy; vault z trzema to folder z ładną nazwą.

## Czy zmieniać ustawienia duplikatów?

Nie w pierwszych tygodniach. Domyślnie aplikacja pyta Cię za każdym razem, gdy nowa notatka przypomina istniejącą, a te pytania uczą, co uznaje za ten sam temat, póki vault jest mały i łatwo go poprawić.

Każdy vault ma dwa ustawienia. **Tryb**: pytaj, zawsze łącz albo zawsze twórz. Oraz **próg** dla oceny podobieństwa od 0 do 1, którą drugi model wystawia każdemu kandydatowi. Próg działa w każdym trybie, bo to on definiuje „ten sam temat”.

Ustaw _zawsze łącz_, kiedy vault to długa nauka jednej dziedziny i chcesz jednej rosnącej notatki na pojęcie. Ustaw _zawsze twórz_, kiedy vault działa jak dziennik i dwa wpisy o tym samym to naprawdę dwa wpisy. Połączenie niczego nie kasuje: oryginalne pytania i odpowiedzi obu notatek zostają pod spodem.

## Jak pytać, żeby notatki AI wychodziły dobre?

Pytaj o jedną rzecz naraz. Notatka powstaje z jednej wymiany, więc pytanie, w którym kryją się cztery pytania, daje jedną notatkę o czterech sprawach: trudną do odłożenia, trudną do połączenia i trudną do znalezienia w maju.

Daj modelowi ramę, którą chcesz dostać z powrotem. „Wyjaśnij hartowanie rozsady” i „Porównaj hartowanie pomidorów przez 7 i przez 14 dni pod kątem ryzyka i nakładu pracy” dają zupełnie inne rozwinięcia. Do drugiej notatki wrócisz następnej wiosny.

Mów wprost, kiedy coś postanawiasz. Odpowiedzi z zapisem tego, co wybrałeś, co odrzuciłeś i dlaczego, to notatki AI, które później spłacają całą konfigurację, bo właśnie to uzasadnienie ginie w przewiniętym czacie.

## Co robić ze spisem treści?

Przeważnie nic. Każda notatka trafia na półkę w chwili powstania, z samą sobą w polu widzenia: to dobra decyzja, która nie widzi przyszłego miesiąca.

Dlatego co jakiś czas kliknij **Przebuduj spis treści** na pasku vaulta. Aplikacja czyta wszystkie notatki porcjami po 60 i układa rozdziały od nowa, a nieudana próba zostawia stare drzewo bez zmian. Zrób to po intensywnym tygodniu, kiedy to, co wiesz, zmieniło kształt, a półki za tym nie nadążyły.

Drzewo edytujesz też ręcznie: zmiana nazwy, kolejności, nowy rozdział, zagnieżdżenie, usunięcie. Usunięty rozdział oddaje notatki rodzicowi.

## Kiedy zmienić tytuł notatki?

Kiedy przestał ją opisywać. Notatkom AI zdarza się to po dwóch, trzech połączeniach.

Zmiana tytułu to więcej niż kosmetyka. Nazwa pliku idzie za tytułem, więc aplikacja przenosi plik `.md` i przepisuje każdy link `[Tytuł](plik.md)` do niego w pozostałych notatkach vaulta. Kolejność jest stała: nowy plik, potem linki, na końcu usunięcie starego, a jeśli któryś krok się nie uda, całość się cofa. Katalog zostaje czytelny z zewnątrz: `hartowanie-rozsady.md` to notatka o hartowaniu rozsady. To zarazem format linków, który czyta Obsidian, więc jeśli traktujesz tę aplikację jako alternatywę dla Obsidiana, link zepsuty tutaj byłby zepsuty także w eksporcie.

## Jak wyciągać rzeczy z powrotem?

Na trzy sposoby, do trzech sytuacji.

**Wyszukiwarka**, kiedy z grubsza pamiętasz, co padło. Przeszukuje tytuły, podsumowania, treść oraz oryginalne pytanie i odpowiedź, ignoruje polskie znaki i pokazuje pasujący fragment z podświetloną frazą.**Pytanie do vaulta**, kiedy nie wiesz, gdzie leży odpowiedź. Idzie ze spisem treści i pełną treścią najwyżej 5 trafnych notatek w limicie 24 000 znaków, a odpowiedź wymienia notatki, z których skorzystała.**Eksport**, kiedy czytać będzie ktoś inny: ZIP z Markdownem, PDF z samymi podsumowaniami albo pełnymi notatkami, edytowalny `.pptx` w kolejności spisu treści z 15 motywami.

ZIP zawiera `base.md` i katalog `notes/` z linkami względnymi. To praktyczna odpowiedź dla każdego, kto rozważa SumizAI jako [Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html) dla notatek pisanych przez model: eksportowany katalog otwiera się w Obsidianie z działającymi linkami.

## Jak wygląda realistyczny tydzień?

Od poniedziałku do czwartku pracujesz tak jak dotąd i pytasz model o to, czego potrzebujesz. Notatki AI przybywają bez Twojego udziału, a mniej więcej dwa razy dziennie odpowiadasz jednym kliknięciem na pytanie o połączenie.

Piątek, dziesięć minut. Otwierasz vault, przeglądasz spis treści, przebudowujesz go, jeśli kształt się rozjechał, i zmieniasz tytuły dwóch notatek, które przestały pasować.

Gdy zbliża się termin, szukasz wątku, eksportujesz do PDF-a albo prezentacji i skracasz. Ten krok jest krótki, bo struktura zapadła czterdzieści rozmów wcześniej, notatka po notatce. W tym tygodniu nie ma wtyczek, synchronizacji ani grafu. Taka Obsidian alternatywa oddaje te trzy rzeczy w zamian za notatki, które piszą się same.

## Jakie są dwa najczęstsze błędy?

Pierwszy: traktowanie vaulta jak archiwum. Dwieście notatek w dwa tygodnie, zero pytań zadanych z powrotem i wniosek, że to wymyślny magazyn logów czatu. Wartość widać w drodze powrotnej, kiedy pierwsza odpowiedź powstaje z pięciu Twoich notatek i je wymienia.

Drugi: jeden ogromny vault na wszystko. Każde pytanie niesie wtedy mniej celny zestaw notatek, a sprawdzanie duplikatów porównuje materiał, który nigdy nie był powiązany. Dziel wcześnie.

I uwaga o oczekiwaniach, bo ten tekst opisuje rytm pracy, a nie pobieranie: żadna wersja nie jest jeszcze dostępna. Aplikacja na macOS trafi wkrótce do Mac App Store, Windows, iOS i Android są w przygotowaniu, a plan to 7 dni za darmo, potem 1 USD miesięcznie. Ogólny opis znajdziesz na stronie głównej: [aplikacja do notatek AI](/pl/).

