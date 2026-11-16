---
title: "Polityka prywatności"
url: "https://sumizai.com/pl/legal/prywatnosc.html"
date: "2026-10-17T00:00:00+02:00"
modified: "2026-10-17T00:00:00+02:00"
description: "SumizAI trzyma notatki na Twoim Macu. Nasz serwer przechowuje tylko konto; strona mierzy ruch, a cookies zapisuje dopiero po zgodzie."
tags: ["sumizai", "legal", "privacy"]
---

# Polityka prywatności

Ta polityka dotyczy aplikacji **SumizAI na Maca** dystrybuowanej przez Mac App Store, usługi kont pod adresem `api.sumizai.com`, z którą aplikacja się łączy, oraz tej strony, `sumizai.com`.

W skrócie: Twoje notatki, pytania, dokumenty i vaulty zostają na Twoim Macu. Nigdy do nas nie trafiają. Nasz serwer przechowuje wyłącznie to, co potrzebne do obsługi konta i subskrypcji. Pytania do AI idą z Twojego Maca prosto do wybranego przez Ciebie dostawcy, na Twoim własnym kluczu. W aplikacji nie ma analityki, reklam, śledzenia ani raportów awarii. Strona mierzy ruch, a pliki cookie zapisuje dopiero po Twojej zgodzie.

## Kto odpowiada za Twoje dane

Administratorem opisanych tu danych osobowych jest **Jan Śliwa**, Polska, prowadzący działalność pod firmą **10UP Jan Śliwa** (jednoosobowa działalność gospodarcza wpisana do CEIDG), NIP 8521091009, Kminkowa 26, 72-003 Bezrzecze, Polska.

Kontakt we wszystkich sprawach z tej polityki, w tym w sprawie Twoich praw: [contact@sumizai.com](mailto:contact@sumizai.com). Każdą wiadomość czyta człowiek.

## Czego dotyczy ta polityka

Dokument dotyczy:

- **aplikacji SumizAI na Maca** z Mac App Store;
- **usługi kont** pod adresem `api.sumizai.com`, której aplikacja używa do logowania, obsługi urządzeń i stanu subskrypcji;
- **strony** `sumizai.com`, w tym formularza kontaktowego na stronie [Pomoc](https://sumizai.com/pl/pomoc/).

Aplikacja i strona się różnią: strona korzysta z analityki (pliki cookie dopiero po Twojej zgodzie), aplikacja nie ma żadnej analityki. Same pliki cookie wymienia [polityka cookies](https://sumizai.com/pl/legal/cookies.html).

## Dane, które zostają na Twoim Macu

Wszystko, co tworzysz w SumizAI, jest przechowywane **wyłącznie na Twoim komputerze**:

- **Notatki** — jako zwykłe pliki Markdown (`.md`) w katalogu notatek. Domyślnie jest to katalog `SumizAI` wewnątrz własnego kontenera aplikacji w macOS. W aplikacji możesz wybrać inny katalog.
- **Vaulty, spis treści, rozmowy, Twoje pytania, odpowiedzi AI i zaimportowane dokumenty** — w lokalnej bazie SQLite i plikach na tym samym Macu.
- **Klucze do dostawców AI, tokeny sesji i identyfikator instalacji** — w pęku kluczy macOS na Twoim Macu.

Nic z tego nie jest do nas wysyłane. Nie ma synchronizacji ani prowadzonej przez nas kopii w chmurze. Nie możemy Twoich notatek przeczytać, odtworzyć ani usunąć, bo nigdy ich nie mamy. Jeśli umieścisz katalog notatek w miejscu, które Twój Mac synchronizuje lub archiwizuje (np. iCloud Drive albo Time Machine), tą kopią zajmuje się Apple albo usługa, którą sam skonfigurujesz, na swoich warunkach.

## Twoje konto w api.sumizai.com

Do wykupienia subskrypcji potrzebne jest konto SumizAI. Zakładasz je w aplikacji adresem e-mail i hasłem. Serwer kont przechowuje:

| Dane | Do czego służą |
|---|---|
| Adres e-mail | Login oraz sposób rozpoznania Twojego konta, gdy do nas piszesz. Nie wysyłamy newsletterów ani reklam. Jedyny e-mail, jaki wysyła usługa, to link do ustawienia nowego hasła — i tylko wtedy, gdy o niego poprosisz. |
| Link do ustawienia nowego hasła (tylko na Twoją prośbę) | Jednorazowy link ważny godzinę. Serwer trzyma wyłącznie jego skrót SHA-256 z czasem wygaśnięcia, nigdy sam link. |
| Skrót hasła (BCrypt) | Sprawdzenie hasła przy logowaniu. Samego hasła nigdy nie przechowujemy. |
| Identyfikator konta (losowy UUID) | Wiąże konto z Twoimi urządzeniami, sesjami i subskrypcją w App Store. |
| Stan dostępu i daty | Czy dostęp jest aktywny, próbny, wygasły czy zablokowany, skąd pochodzi (subskrypcja App Store albo dostęp przyznany ręcznie przez nas, np. testerom), kiedy się kończy, oraz opcjonalna notatka wewnętrzna wyjaśniająca ręczne przyznanie. |
| Daty i platforma konta | Kiedy konto założono i ostatnio zmieniono, na jakiej platformie powstało (np. macOS), na jakiej platformie i kiedy było ostatnio używane, oraz znacznik ustawiany, gdy na tym samym komputerze powstaje kolejne konto. |
| Kod polecający | Tylko jeśli konto założono z linku polecającego, który go zawierał. W przeciwnym razie puste. |
| Tokeny sesji | Krótkotrwały token dostępu (15 minut) i token odświeżający (30 dni, wymieniany przy każdym użyciu). Serwer trzyma wyłącznie skrót SHA-256 każdego tokenu odświeżającego, z datą wydania, wygaśnięcia i unieważnienia oraz urządzeniem, do którego należy. |

Nie pytamy o imię i nazwisko, numer telefonu, adres, zdjęcie ani datę urodzenia — serwer nie ma nawet miejsca, by je zapisać.

**Reset hasła:** w aplikacji wybierz **Nie pamiętasz hasła?** i podaj adres e-mail konta. Jeśli jest pod nim konto, nasz własny serwer pocztowy wysyła na ten adres jednorazowy link; odpowiedź w aplikacji jest zawsze taka sama, więc nie da się w ten sposób sprawdzić, kto ma konto. Link otwiera stronę na sumizai.com bez żadnej analityki, działa przez godzinę i tylko raz, a ustawienie nowego hasła wylogowuje wszystkie Twoje urządzenia.

## Identyfikatory urządzeń

Jedno konto może być aktywne na maksymalnie **trzech** komputerach. Żeby pilnować tego limitu — i żeby ten sam komputer nie mógł raz po raz brać okresu próbnego na nowe adresy e-mail — aplikacja przy logowaniu i rejestracji wysyła jeden identyfikator:

- **Identyfikator instalacji** — losowa wartość, którą aplikacja tworzy przy pierwszym użyciu i trzyma w pęku kluczy macOS. Nie jest wyliczana z niczego, co dotyczy Ciebie ani Twojego Maca.

Aplikacja nie odczytuje żadnego identyfikatora sprzętu Twojego Maca (numeru seryjnego, sprzętowego UUID ani adresu sieciowego) i żadnego nie wysyła.

Dla każdego urządzenia serwer zapisuje też platformę, etykietę złożoną z nazwy systemu i pierwszych ośmiu znaków identyfikatora instalacji (np. `macOS · 1a2b3c4d` — nie nazwę Twojego komputera), kiedy urządzenie pojawiło się pierwszy i ostatni raz oraz kiedy je odłączyłeś. Swoje urządzenia widzisz i odłączasz w **Ustawienia → Urządzenia**; odłączenie od razu wylogowuje to urządzenie.

## Zakupy przez Apple

Subskrypcję sprzedaje i pobiera za nią opłatę **wyłącznie Apple** — przez App Store i StoreKit, z Twojego Apple ID. Nie widzimy numeru karty, danych bankowych ani adresu rozliczeniowego i nie przetwarzamy płatności.

Apple wysyła do naszego serwera podpisane powiadomienia o Twojej subskrypcji (np. rozpoczęta, odnowiona, wygasła, zwrócona). Na ich podstawie przechowujemy przy koncie **pierwotny identyfikator transakcji** subskrypcji, źródło dostępu (App Store), datę końca dostępu i jego stan. Zakup jest powiązany z kontem SumizAI przez identyfikator konta. Prowadzimy też dziennik odebranych powiadomień: identyfikator powiadomienia nadany przez Apple, jego rodzaj, środowisko (produkcyjne lub testowe), czy zmieniło Twój dostęp i kiedy przyszło. To, jak Apple przetwarza Twoje dane, opisuje [polityka prywatności Apple](https://www.apple.com/legal/privacy/).

## Wybrani przez Ciebie dostawcy AI

SumizAI nie ma własnej sztucznej inteligencji. Dostawcę wybierasz w aplikacji i podłączasz **własnym kluczem API** (lokalna Ollama albo własny serwer mogą nie wymagać klucza).

Gdy korzystasz z funkcji AI, aplikacja wysyła z Twojego Maca **bezpośrednio do tego dostawcy**: pytanie i przebieg rozmowy, fragmenty notatek użyte jako kontekst (spis treści i treść maksymalnie pięciu najtrafniejszych notatek) treść dokumentów, które importujesz, gdy prosisz AI o pracę na nich, oraz materiał źródłowy notatki, gdy prosisz o jego przekład na język vaulta. Te dane nie przechodzą przez nasze serwery i nie mamy do nich wglądu.

Zanim cokolwiek zostanie po raz pierwszy wysłane do dostawcy, aplikacja pokazuje, co i dokąd pójdzie, podaje link do polityki prywatności dostawcy i prosi o zgodę. Zgodę wycofujesz, odłączając dostawcę w ustawieniach aplikacji — od tej chwili nic do niego nie trafia.

Dostawca przetwarza dane na własnych warunkach i na podstawie umowy z Tobą jako właścicielem klucza. Czy je przechowuje albo używa do trenowania modeli, zależy od tych warunków i ustawień Twojego konta u niego, nie od nas. Ich polityki:

| Dostawca | Dokąd trafiają dane | Jego polityka prywatności |
|---|---|---|
| Anthropic (Claude) | `api.anthropic.com` | [anthropic.com/legal/privacy](https://www.anthropic.com/legal/privacy) |
| OpenAI | `api.openai.com` | [openai.com/policies/privacy-policy](https://openai.com/policies/privacy-policy/) |
| Google Gemini | `generativelanguage.googleapis.com` | [policies.google.com/privacy](https://policies.google.com/privacy) oraz [dodatkowe warunki Gemini API](https://ai.google.dev/gemini-api/terms) |
| Groq | `api.groq.com` | [groq.com/privacy-policy](https://groq.com/privacy-policy/) |
| OpenRouter | `openrouter.ai`, który przekazuje dalej do dostawcy modelu wybranego u niego | [openrouter.ai/privacy](https://openrouter.ai/privacy) |
| Ollama (lokalnie) | `127.0.0.1` — Twój własny komputer. Nic nie opuszcza urządzenia. | Nie dotyczy |
| Własny serwer | Adres, który wpiszesz | Ten, kto prowadzi ten serwer |

Klucze do dostawców są przechowywane w pęku kluczy macOS na Twoim Macu i wysyłane wyłącznie do dostawcy, do którego należą. Nigdy ich nie otrzymujemy.

## Czego aplikacja nie robi

- Żadnej analityki ani statystyk użycia w aplikacji.
- Żadnych reklam ani identyfikatorów reklamowych.
- Żadnego śledzenia między aplikacjami i stronami, żadnych brokerów danych.
- Żadnych raportów awarii ani telemetrii.
- Nie sprzedajemy ani nie udostępniamy danych osobowych nikomu — ani z aplikacji, ani ze strony.

## Strona: sumizai.com

Strona to statyczny HTML na naszym własnym serwerze. Nie ma kont ani logowania. Ma dwa formularze: opisany niżej formularz kontaktowy oraz stronę ustawiania nowego hasła z linku resetu (patrz „Twoje konto w api.sumizai.com”), która nie ładuje żadnej analityki. Strona ładuje dokładnie dwie usługi zewnętrzne, obie do pomiaru ruchu:

- **Google Analytics 4** (usługa `G-RKZ7HS09BS`) — które podstrony zostały otwarte, z jakiego mniej więcej regionu przyszła wizyta, skąd przyszedłeś i jakiego rodzaju urządzenia oraz przeglądarki użyto. To zbiorczy pomiar ruchu; nie mówi nam, kim jesteś.
- **Microsoft Clarity** (projekt `y23mz3osxm`) — zanonimizowane odtworzenia sesji: ruch kursora, kliknięcia, przewijanie i układ strony. To rekonstrukcja strony, a nie nagranie Twojego ekranu, i nie doklejamy do niej żadnego własnego identyfikatora.

Nic więcej: żadnych pikseli reklamowych, tagów remarketingowych, czatu ani fingerprintingu.

### Przed zgodą: pomiar bez zapisu

Dopóki nie zaakceptujesz plików cookie w banerze, oba narzędzia działają w trybie bezcookiesowym (Google _Consent Mode advanced_, tryb bezcookiesowy Clarity): odnotowują, że strona została otwarta, i **nie zapisują niczego na Twoim urządzeniu** — żadnego pliku cookie, pamięci lokalnej, sesyjnej ani identyfikatora, który przetrwałby tę odsłonę. Każda odsłona liczona jest osobno. Podstawą jest nasz prawnie uzasadniony interes w wiedzy, które strony są czytane (art. 6 ust. 1 lit. f RODO); ponieważ nic nie jest zapisywane na Twoim urządzeniu ani z niego odczytywane, art. 398 Prawa komunikacji elektronicznej nie wymaga na to zgody. W każdej chwili możesz wnieść sprzeciw, pisząc do nas.

### Po zgodzie

Akceptacja włącza pliki cookie wymienione w [polityce cookies](https://sumizai.com/pl/legal/cookies.html) oraz nagrywanie sesji — na podstawie Twojej zgody (art. 6 ust. 1 lit. a RODO). Twój wybór zapisujemy w jednym wpisie w pamięci lokalnej przeglądarki — to nie jest plik cookie i jest to jedyna rzecz zapisywana bez pytania, bo inaczej nie dałoby się zapamiętać, że powiedziałeś „nie”. Wybór zmienisz lub wycofasz w każdej chwili linkiem _Ustawienia cookies_ w stopce; wycofanie kasuje zapisane już pliki cookie.

### Adres IP i warunki dostawców

Każde zapytanie do serwera niesie Twój adres IP. W raportach analitycznych, z których korzystamy, nie widzimy adresów IP. Google i Microsoft posługują się nim w swoich usługach na własnych warunkach ([Google](https://policies.google.com/privacy), [Microsoft](https://privacy.microsoft.com/privacystatement)). Nie budujemy profili, nie łączymy tych danych z niczym innym i ich nie sprzedajemy.

## Kiedy do nas piszesz

**E-mailem.** [contact@sumizai.com](mailto:contact@sumizai.com) to skrzynka, którą prowadzimy sami (Postfix, Dovecot i OpenDKIM na naszym serwerze w Hetznerze w Niemczech). Między nami nie ma żadnego dostawcy poczty.

**Przez formularz kontaktowy** na stronie [Pomoc](https://sumizai.com/pl/pomoc/). Formularz wysyła podany adres e-mail, temat i treść wiadomości, a także język i adres strony, do naszego serwera kont pod adresem `api.sumizai.com` (ta sama maszyna w Hetznerze), który przekazuje wiadomość do nas. Jak każde żądanie, trafia ono do logu dostępu wraz z Twoim adresem IP (patrz [Logi serwera](#server-logs)), a adres IP służy przez krótki czas do ograniczenia liczby wiadomości wysyłanych pod rząd. Formularz nie używa plików cookie.

To, co piszesz, wykorzystujemy wyłącznie do odpowiedzi i załatwienia sprawy. Podstawą jest art. 6 ust. 1 lit. b RODO, gdy wiadomość dotyczy korzystania z SumizAI, a w pozostałych przypadkach lit. f — nasz prawnie uzasadniony interes w odpowiadaniu osobom, które do nas piszą. Wiadomości przechowujemy tak długo, jak trzeba do załatwienia sprawy i ewentualnych roszczeń z nią związanych.

## Logi serwera i bezpieczeństwo

Jak każda usługa internetowa, nasze serwery (serwer kont i strona) widzą adres IP każdego żądania. Używamy go tak:

- **Log dostępu** serwera WWW: czas, adres IP, żądany adres, kod odpowiedzi i identyfikator klienta (user agent) aplikacji. Logi rotują automatycznie i są przechowywane najwyżej 90 dni.
- **Log aplikacji**: zdarzenia techniczne i błędy. Adresy e-mail są maskowane do pierwszej litery i domeny, tokeny do ostatnich czterech znaków. Logi aplikacji przechowujemy do 30 dni, potem są kasowane.
- **Ochrona przed zgadywaniem haseł**: nieudane logowania są liczone per adres e-mail i per adres IP, wyłącznie w pamięci serwera, przez 15 minut.

Aplikacja co jakiś czas sprawdza też, która wersja jest aktualna, żeby przestarzała wersja mogła poprosić o aktualizację. To żądanie zawiera wyłącznie nazwę platformy.

## Na jakiej podstawie przetwarzamy dane (RODO)

- **Wykonanie umowy** (art. 6 ust. 1 lit. b RODO): konto, logowanie, sesje, urządzenia, limit urządzeń i stan subskrypcji — bez nich nie możemy świadczyć usługi, którą wykupujesz.
- **Prawnie uzasadniony interes** (art. 6 ust. 1 lit. f RODO): zapobieganie nadużyciom okresu próbnego i limitu urządzeń (identyfikatory urządzeń, zapis opisany w części [Usunięcie konta](#deleting-your-account)), ochrona usługi przed atakami (logi, ograniczanie prób logowania i wysyłek formularza), bezcookiesowy pomiar ruchu na stronie, odpowiadanie na wiadomości oraz ustalanie, dochodzenie i obrona roszczeń.
- **Zgoda** (art. 6 ust. 1 lit. a RODO): analityczne pliki cookie i nagrywanie sesji na stronie, dopiero po ich zaakceptowaniu.
- **Obowiązek prawny** (art. 6 ust. 1 lit. c RODO): gdy przepisy nakazują przechować lub ujawnić dane.

Wysłanie danych do dostawcy AI jest Twoją czynnością, wykonywaną z Twojego Maca Twoim kluczem — my tych danych nie przetwarzamy. Zgoda, o którą aplikacja prosi przed pierwszym wysłaniem, ma zapewnić, że wiesz, co i dokąd idzie.

## Kto jeszcze otrzymuje dane

- **Hetzner Online GmbH** (Industriestrasse 25, 91710 Gunzenhausen, Niemcy) — hosting. Serwer kont, strona i nasza skrzynka pocztowa działają na naszej maszynie w centrum danych Hetznera Falkenstein (FSN1) w Niemczech, w UE. Hetzner jest naszym podmiotem przetwarzającym.
- **Google i Microsoft** — jako dwie usługi analityczne strony (wyżej). Z aplikacji nic do nich nie trafia. Google może też wystąpić jako dostawca AI, jeśli wybierzesz Gemini.
- **Apple** — sprzedaje subskrypcję, pobiera opłaty i informuje nas o jej stanie. W zakresie zakupu Apple jest odrębnym administratorem.
- **Wybrany przez Ciebie dostawca AI** — otrzymuje dane bezpośrednio z Twojego Maca, na podstawie Twojej umowy z nim (patrz wyżej). Od nas nie dostaje niczego.
- **Organy publiczne** — wyłącznie gdy zobowiązuje nas do tego prawo.

Wiadomości wysłane na [contact@sumizai.com](mailto:contact@sumizai.com) są przechowywane na tej samej maszynie w Hetznerze; nie korzystamy z zewnętrznego dostawcy poczty.

## Przekazywanie danych poza UE

Dane konta, stronę i naszą skrzynkę pocztową utrzymujemy w Unii Europejskiej i nie przekazujemy ich poza Europejski Obszar Gospodarczy. Apple, wybrany przez Ciebie dostawca AI oraz usługi analityczne strony (Google, Microsoft) mogą przetwarzać dane w innych krajach, w tym w Stanach Zjednoczonych — regulują to ich własne warunki i zabezpieczenia. Jeśli chcesz tego całkiem uniknąć: używaj w aplikacji lokalnej Ollamy i nie zgadzaj się na analityczne pliki cookie na stronie.

## Jak długo przechowujemy dane

| Dane | Przechowywane do |
|---|---|
| Konto, sesje, urządzenia, stan subskrypcji | Usunięcia konta. Wygasłe tokeny odświeżające i odłączone urządzenia pozostają do tego czasu przy koncie. |
| Identyfikator instalacji urządzeń, które wykorzystały okres próbny | Zostają po usunięciu konta, bez powiązania z jakimkolwiek kontem ani adresem e-mail. Kasowane 3 lata po wpisie. |
| Dziennik powiadomień od Apple | Zostaje po usunięciu konta, z usuniętym powiązaniem z kontem. Kasowany 30 dni po otrzymaniu. |
| Logi dostępu serwera WWW | Najwyżej 90 dni. |
| Logi aplikacji | Do 30 dni. |
| Liczniki nieudanych logowań | 15 minut, w pamięci. |
| Link do ustawienia nowego hasła (jego skrót) | Do użycia albo wygaśnięcia (godzina); usuwany z bazy następnej nocy. |
| Twoje e-maile i wiadomości z formularza | Tak długo, jak trzeba do załatwienia sprawy i ewentualnych roszczeń z nią związanych. |
| Wybór dotyczący cookies na stronie | Jeden wpis w pamięci lokalnej przeglądarki, dopóki go nie usuniesz lub nie zmienisz wyboru. |
| Analityka strony | W Google Analytics i Microsoft Clarity, zgodnie z okresami przechowywania tych usług. Nie trzymamy osobnej kopii. |
| Notatki, vaulty, rozmowy, klucze | Nigdy ich nie mamy. Zostają na Twoim Macu, dopóki ich nie usuniesz. |

## Usunięcie konta

Konto możesz usunąć w każdej chwili w aplikacji: **Ustawienia → Usuń konto**. Usunięcie jest natychmiastowe i nieodwracalne. Kasuje z naszego serwera konto (e-mail, skrót hasła, stan i daty), wszystkie sesje i wszystkie urządzenia. To prawdziwe usunięcie, nie dezaktywacja. Stan subskrypcji i pierwotny identyfikator transakcji Apple zapisane przy koncie są kasowane razem z nim; wpisy w dzienniku powiadomień Apple zostają, z usuniętym powiązaniem z Twoim kontem.

**Zostaje jedna rzecz i tylko w jednym celu.** Identyfikator instalacji urządzeń, które były powiązane z usuniętym kontem, jest przechowywany w osobnej tabeli wraz z datą wpisu, **bez powiązania z jakimkolwiek kontem i bez adresu e-mail**. Służy wyłącznie temu, żeby po usunięciu konta i założeniu nowego na tym samym komputerze nie przyznać ponownie okresu próbnego. Podstawą jest nasz prawnie uzasadniony interes w zapobieganiu nadużyciom (art. 6 ust. 1 lit. f RODO). Możesz wnieść sprzeciw, pisząc na [contact@sumizai.com](mailto:contact@sumizai.com).

**Twoje vaulty i pliki `.md` zostają na Macu.** Usunięcie konta nigdy ich nie dotyka. Aby je usunąć, skasuj katalog notatek i aplikację.

**Usunięcie konta nie anuluje subskrypcji w App Store.** Opłaty pobiera Apple, więc subskrypcję anulujesz w ustawieniach Apple ID ([jak anulować](https://support.apple.com/pl-pl/118428)).

## Twoje prawa

Na podstawie RODO masz prawo do:

- **dostępu** do swoich danych i otrzymania ich kopii;
- **sprostowania** danych nieprawidłowych (np. błędnie wpisanego adresu e-mail);
- **usunięcia** danych — najszybciej przez **Ustawienia → Usuń konto**;
- **ograniczenia** przetwarzania;
- **przenoszenia** danych — dane konta w formacie nadającym się do odczytu maszynowego (notatki i tak są zwykłymi plikami na Twoim Macu);
- **sprzeciwu** wobec przetwarzania opartego na naszym prawnie uzasadnionym interesie;
- **wycofania zgody** w dowolnym momencie, gdy przetwarzanie się na niej opiera — bez wpływu na to, co działo się wcześniej;
- **wniesienia skargi** do organu nadzorczego: Prezesa Urzędu Ochrony Danych Osobowych, ul. Stawki 2, 00-193 Warszawa, [uodo.gov.pl](https://uodo.gov.pl/), albo do organu w kraju UE, w którym mieszkasz lub pracujesz.

Napisz na [contact@sumizai.com](mailto:contact@sumizai.com) z adresu e-mail swojego konta, żebyśmy mogli potwierdzić, że należy do Ciebie. Odpowiadamy w ciągu miesiąca. Nie podejmujemy wobec Ciebie decyzji opartych wyłącznie na zautomatyzowanym przetwarzaniu.

## Jak chronimy dane

- Cały ruch między aplikacją a `api.sumizai.com` jest szyfrowany (HTTPS).
- Hasła przechowujemy wyłącznie jako skróty BCrypt, tokeny odświeżające wyłącznie jako skróty SHA-256.
- Baza danych nie jest dostępna z internetu — dostępny jest tylko serwer WWW.
- Sekrety na Twoim Macu (klucze dostawców, tokeny sesji) są w pęku kluczy macOS.

## Dzieci

SumizAI nie jest skierowane do dzieci i świadomie nie zakładamy kont dzieciom poniżej 16 lat. Jeśli uważasz, że dziecko przekazało nam dane, napisz na [contact@sumizai.com](mailto:contact@sumizai.com) — usuniemy je.

## Zmiany tej polityki

Gdy zmienia się aplikacja albo ta polityka, publikujemy tu nową wersję z nową datą i numerem wersji. Data na górze strony zawsze wskazuje, która wersja obowiązuje.

## Kontakt

10UP Jan Śliwa, Kminkowa 26, 72-003 Bezrzecze, Polska — [contact@sumizai.com](mailto:contact@sumizai.com). Pomoc z aplikacją: [Pomoc](https://sumizai.com/pl/pomoc/). Warunki: [Regulamin](https://sumizai.com/pl/legal/regulamin.html).

