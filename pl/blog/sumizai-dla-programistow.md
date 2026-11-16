---
title: "Co SumizAI daje programistom?"
url: "https://sumizai.com/pl/blog/sumizai-dla-programistow.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Notatki AI w pracy programisty: decyzje projektowe i sesje debugowania zapisane w Markdownie, z oryginalną wymianą zachowaną słowo w słowo pod notatką."
tags: ["notatki programisty", "decyzje architektoniczne", "notatki z debugowania", "inżynierska baza wiedzy", "notatki markdown dla programistów", "sumizai"]
---

# Co SumizAI daje programistom?

Programiści rozmawiają z modelami przez cały dzień i przez cały dzień te odpowiedzi znikają w historii czatu. Kod przetrwa w repozytorium. **Rozumowanie nie**: dlaczego to podejście, co odrzucono, co pokazał benchmark. SumizAI zamienia takie wymiany w notatki AI w Markdownie, odłożone według tematu, ze źródłem zachowanym słowo w słowo.

## Co warto trzymać jako notatki AI?

Decyzje razem z opcjami, które odrzuciłeś. Większość reszty jest już w kodzie albo nie zasługuje na plik.

Notatka „używamy RabbitMQ” nic nie wnosi, to samo mówi plik konfiguracyjny. Notatka „wybraliśmy RabbitMQ zamiast Kafki, bo potwierdzanie pojedynczych wiadomości ważyło więcej niż przepustowość przy 2 000 wiadomości na sekundę” zawiera dokładnie to, czego nie zapisze żaden commit. Poproś model o rozpisanie kompromisu, zachowaj odpowiedź, a stanie się jedną z Twoich notatek AI z tytułem, podsumowaniem i rozwinięciem.

Druga kategoria: sesje debugowania zakończone wyjaśnieniem. Poprawka to commit. Powód, dla którego błąd był możliwy, to notatka.

## Źródło pod notatką jest tylko dopisywane

Każda notatka trzyma pod podsumowaniem oryginalne pytanie i odpowiedź, znak w znak. Późniejsze scalenia dopisują do źródła, nic go nie poprawia ani nie usuwa.

Twierdzenia inżynierskie się starzeją. Gdy notatka mówi, że pula połączeń nie pomogła, otwierasz źródło i widzisz, że rozmowa dotyczyła PostgreSQL 12, puli 20 połączeń i jednego konkretnego obciążenia. Samo podsumowanie tego nie powie, a podsumowanie, którego nikt nie sprawdzi, zamienia się w legendę zespołu.

Przykładowa notatka „Sowing tomatoes indoors”. Notatka o wyborze kolejki ma te same części: podsumowanie na górze, źródło na dole.

## Pliki Markdown obok repozytorium

Vault to zwykłe pliki `.md` w katalogu na Twoim dysku, a lokalna baza służy wyłącznie jako indeks. Nie ma synchronizacji ani serwera z notatkami.

**Pobierz vault** daje archiwum ZIP: `base.md` ze spisem treści i katalog `notes/`. Linki są względne, więc rozpakowujesz całość do `docs/decisions/`, commitujesz i odnośniki dalej działają w pull requeście na GitHubie. Diff notatek AI czyta się jak diff kodu. Działa na nich `grep -r`, `rg` i podgląd Markdowna w edytorze.

Odnośniki w notatce to zwykłe linki Markdown, np. `[Polityka ponowień](polityka-ponowien.md)`, a nie wiki-linki. Model dostaje mapę istniejących tytułów i nazw plików i linkuje tylko do nich, więc nie zostajesz z odwołaniami do plików, które nigdy nie istniały.

## Jeden vault na system

Nie na ticket. Vault jest granicą: pytanie zadane w środku widzi wyłącznie jego notatki. Zadaj sobie pytanie: gdy pytam o usługę rozliczeń, czy model powinien widzieć notatki o aplikacji mobilnej? Jeśli nie, to dwa vaulty.

W środku strukturę niesie spis treści. Ma do sześciu poziomów, numerowanych `1.`, `1.1`, `a)`, `a.1)`, a model odkłada nową notatkę do istniejącego rozdziału po numerze albo prosi o podrozdział. Podsystemy to dobre rozdziały, tickety nie. Usunięcie rozdziału przenosi jego notatki do rodzica, więc przebudowa struktury nic nie kosztuje.

## Modele lokalne i krok zgody

Do kodu, którego nie wolno wysłać do chmury, podłączasz Ollamę na własnej maszynie albo własny serwer zgodny z API OpenAI (vLLM, LM Studio, firmowa bramka). To dwóch z siedmiu dostawców; pozostali to Anthropic, OpenAI, Google Gemini, Groq i OpenRouter.

Każdy działa na Twoim własnym kluczu API. Zapytania idą prosto z komputera do dostawcy, a przed wysłaniem aplikacja prosi o zgodę w oknie, które wylicza, co wychodzi: pytania, fragmenty notatek użyte jako kontekst, importowane dokumenty.

Kontekst ma granice. Pytanie idzie ze spisem treści i pełną treścią najwyżej pięciu najtrafniejszych notatek, w budżecie 24 000 znaków, a aplikacja pokazuje, których użyła. Vault z 800 notatkami AI nie oznacza 800 notatek w każdym prompcie.

## Kod w repozytorium, uzasadnienie w vaulcie

SumizAI nie jest menedżerem snippetów, a notatka to kiepskie miejsce na kod, który ma się kompilować. Krótkie fragmenty w notatkach AI są w porządku jako ilustracja.

Zasada, której bym się trzymał: jeśli coś się uruchamia, idzie do repozytorium. Jeśli wyjaśnia, dlaczego to, co się uruchamia, wygląda tak, a nie inaczej, idzie do vaulta.

Istniejące opisy wchodzą przez import. Wskaż katalog z plikami `.md`, `.markdown`, `.txt` albo `.pdf` (stare ADR-y, specyfikacja dostawcy w PDF), a każdy plik stanie się notatką z oryginalnym tekstem dołączonym jako źródło.

## Jak znaleźć starą decyzję

Wyszukiwanie działa po znaczeniu w tytułach, podsumowaniach i treści notatek AI, więc „czemu nie Kafka” znajdzie notatkę o kolejce, nawet gdy słowo Kafka stoi tylko w źródle.

Duplikaty są wyłapywane, zanim się namnożą. Wyszukiwanie pełnotekstowe i trigramy wskazują kandydatów, drugi model ocenia podobieństwo od 0 do 1 z uzasadnieniem, a powyżej ustawienia **Próg podobieństwa** decydujesz, czy połączyć, czy zostawić obie. Jeśli co sprint wracasz do tych samych tematów, ustaw vault na **Zawsze łącz**.

## Gdzie nie wystarcza i gdzie pasuje Obsidian

Brak synchronizacji, więc laptop i desktop mają osobne biblioteki. Brak wspólnych vaultów i funkcji zespołowych, więc to narzędzie osobiste używane w zespole. Brak wtyczek, grafu i wiki-linków.

Wielu programistów trzyma już vault Markdowna w Obsidianie i wcale nie szuka alternatywy dla Obsidiana. SumizAI nie zastępuje edytora; to [Obsidian alternatywa na etap pisania notatek](/pl/alternative-to/sumizai-alternative-to-obsidian.html). Model pisze je i odkłada, a wyeksportowany katalog otwiera się w Obsidianie bez zmian, razem z linkami względnymi. Jeśli Twój układ stoi na trzydziestu wtyczkach, uczciwa odpowiedź brzmi: żadna alternatywa dla Obsidiana bez wtyczek go nie zastąpi, a ta nawet nie próbuje.

Przy przekazywaniu usługi koledze eksport daje więcej niż katalog linków: PDF+ drukuje pełne notatki w kolejności spisu treści, a eksport `.pptx` tworzy edytowalne slajdy w jednym z 15 motywów, bez wymian źródłowych.

## Cena i dostępność

Siedem dni za darmo, potem 1 USD miesięcznie, jeden plan. Model rozlicza Twój dostawca, SumizAI nic nie dolicza. Żadnej wersji nie da się jeszcze zainstalować: wydanie na macOS (Apple silicon i Intel) trafi do Mac App Store, a Windows, iOS i Android są w przygotowaniu. Aktualny stan opisuje strona [aplikacja do notatek AI](/pl/).

