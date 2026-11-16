---
title: "Polityka cookies"
url: "https://sumizai.com/pl/legal/cookies.html"
date: "2026-10-17T00:00:00+02:00"
modified: "2026-10-17T00:00:00+02:00"
description: "Co sumizai.com zapisuje na Twoim urządzeniu, kiedy i na jak długo. Przed Twoim wyborem nie działa nic poza niezbędnym. Aplikacje nie mają cookies."
tags: ["sumizai", "legal", "cookies"]
---

# Polityka cookies

Ta strona wymienia wszystko, co SumizAI zapisuje na Twoim urządzeniu przez przeglądarkę, po co to robi i jak to wyłączyć. Analityka uruchamia się dopiero po Twojej zgodzie. Aplikacje SumizAI nie zapisują żadnych cookies.

## Czego dotyczy ten dokument

Nazwę SumizAI noszą dwie różne rzeczy, a każda zapisuje na Twoim urządzeniu zupełnie co innego. Ten dokument mówi wprost, która jest która.

- **Strona `sumizai.com`** — to, co właśnie czytasz, razem z blogiem i dokumentami prawnymi. Tylko tutaj istnieje analityka.
- **Aplikacja SumizAI** na Twoim komputerze. **Nie zapisuje żadnych plików cookie** i nie ma w niej analityki, telemetrii ani raportowania awarii.

Słowo „cookies” jest tu skrótem na wszystko, co strona zapisuje na Twoim urządzeniu: same pliki cookie, ale też wpisy w `localStorage`. Zapisanie czegokolwiek, co nie jest niezbędne do usługi, o którą poprosiłeś, wymaga Twojej zgody — tak wynika z przepisów o łączności elektronicznej wdrażających dyrektywę ePrivacy. Dane osobowe, które analityka później zbiera, przetwarzamy właśnie na podstawie tej zgody, art. 6 ust. 1 lit. a RODO. Szerzej o danych mówi [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html).

## Nasza zasada: przed Twoim wyborem nic się nie zapisuje

Google Analytics i Microsoft Clarity nie siedzą w kodzie strony. Wstrzykuje je jeden nasz własny skrypt, `/assets/consent.js`, obecny na każdej podstronie.

**Zanim odpowiesz, a także gdy odmówisz, oba narzędzia działają w trybie bezcookiesowym.** Odnotowują, że strona została otwarta, i przesyłają nam ten fakt. Czego _nie_ robią: nie zapisują niczego na Twoim urządzeniu — żadnego pliku cookie, żadnej pamięci lokalnej ani sesyjnej, żadnego identyfikatora, po którym ktokolwiek rozpoznałby Cię przy następnej wizycie. Google nazywa ten stan _Consent Mode advanced_ i oznacza pomiar jako modelowany; Microsoft nazywa go _trybem bezcookiesowym_ i nadaje każdej odsłonie jednorazowy numer. Zgody wymaga art. 398 Prawa komunikacji elektronicznej, wdrażający art. 5 ust. 3 dyrektywy ePrivacy — przepis dotyczy przechowywania i odczytu danych na Twoim urządzeniu, a w tym stanie nie robimy ani jednego, ani drugiego.

**Dopiero po Twojej zgodzie** zapisują się pliki cookie z tabeli poniżej i rusza nagrywanie sesji.

**Twój wybór nie jest zapisany w pliku cookie.** Leży w `localStorage` Twojej przeglądarki, pod kluczem `sumizai.consent`, jako dane pierwszej strony, i nigdy nie opuszcza Twojego urządzenia. Wpis zawiera trzy rzeczy: numer wersji, informację czy zgodziłeś się na analitykę, oraz datę i godzinę wyboru.

Jeżeli `localStorage` jest niedostępny — tryb prywatny, wyłączona pamięć — wyboru nie da się zapamiętać. Wtedy baner pojawi się przy kolejnej wizycie, a do czasu odpowiedzi pomiar znowu pozostaje bezcookiesowy. Awaria celowo idzie w stronę ciszy, nie w stronę śledzenia.

Na tej stronie **nie ma cookies reklamowych**: żadnej sieci reklamowej, remarketingu, pikseli konwersji, brokerów danych, fingerprintingu ani cookie wall. Odmowa nic Cię nie kosztuje — strona działa dokładnie tak samo.

## Pamięć ściśle niezbędna

Tych nie da się wyłączyć w panelu, bo ich wyłączenie zepsułoby to, o co poprosiłeś. Nie wymagają zgody.

| Nazwa | Gdzie | Do czego służy | Jak długo |
|---|---|---|---|
| `sumizai.consent` | sumizai.com — `localStorage`, nie plik cookie | Pamięta odpowiedź, której udzieliłeś banerowi, żeby nie pytać na każdej podstronie. To jest sam zapis zgody. | Do czasu wyczyszczenia danych tej strony albo podniesienia przez nas numeru wersji zapisu i ponownego zapytania. |

To jedyny ściśle niezbędny wpis. Strona nie ma logowania i nie ustawia ciasteczka sesji.

## Cookies analityczne (dopiero po zgodzie)

Jeśli zgodzisz się na analitykę, ładują się dwa narzędzia: **Google Analytics 4** (usługa `G-RKZ7HS09BS`) i **Microsoft Clarity** (projekt `y23mz3osxm`). Używamy ich, żeby wiedzieć, które strony są czytane, które porzucane i w którym miejscu tekst myli czytelnika. To jedyne usługi zewnętrzne na tej stronie.

| Cookie | Kto ustawia | Po co | Czas życia (domyślny u dostawcy) |
|---|---|---|---|
| `_ga` | Google Analytics 4 | Odróżnia jedną przeglądarkę od drugiej, żeby powracająca osoba nie liczyła się jako nowa. | 2 lata |
| `_ga_RKZ7HS09BS` (wzorzec `_ga_*`) | Google Analytics 4 | Przechowuje stan sesji dla tej konkretnej usługi Analytics. | 2 lata |
| `_clck` | Microsoft Clarity | Przypisuje przeglądarce identyfikator Clarity, żeby kilka odsłon należało do jednego nagrywanego użytkownika. | 1 rok |
| `_clsk` | Microsoft Clarity | Łączy odsłony jednej wizyty w jedno nagranie sesji. | 1 dzień |
| `MUID` | Microsoft | Identyfikator Microsoftu używany w jego własnych usługach; zapisywany tam, gdzie domeny Microsoftu są dla Twojej przeglądarki osiągalne. | 1 rok |
| `CLID` | Microsoft Clarity | Identyfikator Clarity oznaczający pierwsze zetknięcie Clarity z tą przeglądarką. | 1 rok |
| `ANONCHK` | Microsoft | Krótko żyjący plik cookie Microsoftu związany ze sposobem obsługi `MUID`; opisuje go lista Microsoftu podlinkowana niżej. | 10 minut |

**Nazwy, przeznaczenie i czasy życia w tej tabeli pochodzą od samych dostawców — tak, jak udokumentowali je w chwili powstania tej strony; żadnej z tych wartości nie ustawiamy my.** Google i Microsoft mogą to zmienić bez informowania nas, a `MUID`, `CLID` i `ANONCHK` są zapisywane w domenach Microsoftu, nie w naszej — więc to, czy w ogóle się pojawią, zależy od ustawień cookies zewnętrznych w Twojej przeglądarce. Za wiążące traktuj zawsze aktualne listy dostawców, podlinkowane niżej. Jeśli wolisz gwarancję zamiast udokumentowanej wartości domyślnej, odmów zgody na analitykę — wtedy nie istnieje żaden z tych wpisów.

Nasza procedura wycofania zgody czyści dodatkowo `_gid`, `_gat` i `SM`, gdyby dostawca je ustawił.

**Dokąd trafiają te dane.** Google i Microsoft działają na globalnej infrastrukturze, więc dane zbierane przez ich skrypty mogą być przetwarzane poza Europejskim Obszarem Gospodarczym — na zabezpieczeniach, które te firmy publikują dla swoich usług; nie mamy z żadną z nich odrębnych ustaleń poza ich standardowymi warunkami. Nie trzymamy też własnej kopii: statystyki zostają w Google Analytics i w Clarity, tak długo, jak te usługi je przechowują, i nie umiemy usunąć tam historii pojedynczego użytkownika. Odmowa zgody albo jej późniejsze wycofanie oznacza, że skrypty w ogóle się nie ładują i nie ma czego przekazywać. Szerzej opisuje to [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html).

## Co naprawdę nagrywa Microsoft Clarity

Mówimy to wprost, zamiast zostawiać Cię z dokumentacją dostawcy: **Clarity nagrywa Twoją wizytę jako odtwarzalną sesję**. Zgodnie z opisem produktu podawanym przez Microsoft zapisuje sygnały interakcji — ruch kursora, przewijanie strony, kliknięcia i dotknięcia ekranu, rozmiar okna oraz kolejność podstron — i odtwarza je jako film z oglądanej przez Ciebie strony, a te same sygnały składa w **mapy ciepła**. Co dokładnie jest zapisywane, decyduje Microsoft, nie my; wiążącym i aktualnym opisem jest jego dokumentacja, podlinkowana niżej.

Więc tak: jeśli zgodziłeś się na analitykę, Twoje przewijanie tej strony może zostać odtworzone. Ogranicza to dwie rzeczy.

- Instalujemy Clarity w postaci, w jakiej przychodzi, i zostawiamy jego domyślne maskowanie treści tekstowych i pól formularzy. Nie używamy API Clarity, żeby doczepić do sesji tożsamość, adres e-mail czy jakikolwiek własny znacznik. Zakres tego maskowania definiuje jednak Microsoft — nie możemy obiecywać za niego więcej.
- To jest publiczna strona informacyjna. Na `sumizai.com` nie ma logowania, więc w nagraniu nie może pojawić się treść konta ani treść notatek. Twoje notatki w ogóle nie trafiają na tę stronę.

Przed zgodą nie nagrywa się nic i po jej wycofaniu również nic. To, co Microsoft robi z zebranymi danymi — gdzie je trzyma i jak długo — reguluje własna informacja Microsoftu, podlinkowana niżej; nie mamy na to wpływu i nie będziemy jej tu streszczać.

## Google Consent Mode: domyślnie odmowa

Zanim na stronie w ogóle może pojawić się jakikolwiek skrypt Google, nasz skrypt zgody ustawia domyślne wartości Google Consent Mode v2. Odmowa jest punktem wyjścia, a nie awaryjnym zabezpieczeniem.

| Sygnał | Domyślnie | Po zgodzie na analitykę |
|---|---|---|
| `analytics_storage` | odmowa | zgoda |
| `ad_storage` | odmowa | nadal odmowa |
| `ad_user_data` | odmowa | nadal odmowa |
| `ad_personalization` | odmowa | nadal odmowa |
| `functionality_storage` | zgoda | zgoda |
| `security_storage` | zgoda | zgoda |

Trzy sygnały reklamowe zostają na odmowie na stałe, bo nie prowadzimy reklamy i nie mają czego włączyć. Zgoda przestawia dokładnie jeden przełącznik. Odmowa albo późniejsze wycofanie zgody ustawia `analytics_storage` z powrotem na odmowę.

## Zmiana i wycofanie zgody

Wycofanie zgody musi być tak samo łatwe jak jej udzielenie, więc to ten sam panel, dostępny z tego samego miejsca na każdej stronie.

- Otwórz **„Ustawienia cookies”** w stopce dowolnej strony.
- Włącz albo wyłącz sekcję **Analityczne**.
- Naciśnij **Zapisz wybór**.

**Wycofanie zgody nie tylko zatrzymuje śledzenie na przyszłość — kasuje też to, co już zostało zapisane.** Gdy wyłączysz analitykę, skrypt natychmiast wygasza analityczne pliki cookie w domenie tej strony: `_ga`, `_ga_*`, `_gid`, `_gat`, `_clck`, `_clsk`, `CLID`, `MUID`, `ANONCHK` i `SM`, w wariantach z kropką na początku domeny i bez niej.

Czego zrobić nie może: sięgnąć po pliki cookie zapisane w domenach Google czy Microsoftu — żadna strona nie kasuje cookies cudzej domeny. Do tego służą ustawienia przeglądarki albo narzędzia rezygnacji dostawców, podlinkowane niżej.

Wycofanie działa na przyszłość. Nie cofa pomiarów już wykonanych i wysłanych do dostawców i nie wpływa na zgodność z prawem tego, co działo się w czasie obowiązywania zgody. Jeśli chcesz, żeby zająć się też wcześniejszymi zapisami, napisz do nas i zajrzyj do [Polityki prywatności](https://sumizai.com/pl/legal/prywatnosc.html), która opisuje Twoje prawo dostępu i usunięcia danych.

## Ustawienia przeglądarki

Przeglądarka potrafi więcej niż nasz panel i działa na wszystkich stronach, nie tylko na tej. W Chrome, Firefoksie, Safari i Edge możesz zablokować cookies w całości, zablokować tylko cookies zewnętrzne, usunąć dane pojedynczej strony albo przeglądać w oknie prywatnym, gdzie wszystko znika po zamknięciu. Rzetelną instrukcję znajdziesz w pomocy swojej przeglądarki; zmienia się zbyt często, żebyśmy ją tu przepisywali.

Dwie konsekwencje warte zapamiętania:

- Wyczyszczenie danych tej strony kasuje też wpis `sumizai.consent`, więc baner wraca i pytamy jeszcze raz. To znikający zapis, a nie ignorowanie Twojej decyzji.
- Na `sumizai.com` nie zepsuje się nic, nawet jeśli zablokujesz wszystko; zapytamy tylko ponownie o cookies przy kolejnej wizycie.

Mówimy uczciwie: **nie** reagujemy dziś na nagłówek „Do Not Track” ani na sygnał Global Privacy Control. Sygnałem, na który reagujemy, jest wybór dokonany w panelu — i dlatego panel domyślnie nie uruchamia niczego.

## Aplikacje

**Aplikacje SumizAI nie zapisują żadnych plików cookie.** To natywne programy, w których nie ma analityki, telemetrii ani raportowania awarii — nie ma w nich też banera zgody, bo na urządzeniu nie ma na co się zgadzać. Twoje vaulty, notatki i rozmowy zostają w lokalnej bazie SQLite i w plikach Markdown w wybranym przez Ciebie folderze, a zapytania do wybranego dostawcy AI idą prosto z Twojego komputera do tego dostawcy i nie przechodzą przez żaden nasz serwer.

Do logowania i sprawdzania subskrypcji aplikacja łączy się z naszym serwerem kont, `api.sumizai.com`. Używa do tego tokenów sesji trzymanych w pęku kluczy systemu, nie plików cookie, i nigdy nie wysyła tam notatek, pytań ani dokumentów. Co ten serwer przechowuje, opisuje [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html).

## Dokumenty dostawców

To aktualne dokumenty dostawców. Są źródłem wiążącym dla tego, jakie pliki cookie ustawiają i co potem robią z danymi. Nie mamy wpływu na te strony i nie obiecamy, że linki będą działać wiecznie.

**Google**

- [Polityka prywatności Google](https://policies.google.com/privacy?hl=pl)
- [Jak Google używa plików cookie](https://policies.google.com/technologies/cookies?hl=pl)
- [Pliki cookie w Google Analytics 4](https://support.google.com/analytics/answer/11397207)
- [Dodatek do przeglądarki blokujący Google Analytics](https://tools.google.com/dlpage/gaoptout)

**Microsoft**

- [Oświadczenie o ochronie prywatności Microsoft](https://privacy.microsoft.com/pl-pl/privacystatement)
- [Lista plików cookie Microsoft Clarity](https://learn.microsoft.com/clarity/setup-and-installation/cookie-list)

Innych usług zewnętrznych na tej stronie nie ma. Nie ładujemy z cudzych serwerów fontów, map, filmów, czatów ani osadzonych widgetów.

## Zmiany tej polityki

Numer wersji i data na górze strony to cała historia zmian. Aktualizujemy ten dokument zawsze, gdy zmienia się narzędziownia strony — dochodzi narzędzie, znika narzędzie, dostawca zmienia nazwę pliku cookie.

Jeżeli zmiana sprawia, że udzielona przez Ciebie zgoda przestaje odpowiadać temu, co miałoby działać, nie opieramy się po cichu na starej odpowiedzi. Podnosimy numer wersji zapisu zgody, co unieważnia wszystkie zapisane wybory, przywraca baner i pyta każdego od nowa. Do czasu nowej odpowiedzi nie działa nic poza tym, co ściśle niezbędne.

## Kontakt

Administratorem danych osobowych zbieranych przez analitykę tej strony — oraz danych kont na `api.sumizai.com` — w rozumieniu art. 4 pkt 7 RODO jest operator wskazany niżej. Notatki z aplikacji nigdy do nas nie docierają. Pytania o cokolwiek z tej strony albo żądanie dotyczące już zebranych danych trafiają do człowieka, nie do formularza.

**Operator**
10UP Jan Śliwa, jednoosobowa działalność gospodarcza wpisana do CEIDG

**Adres**
Kminkowa 26, 72-003 Bezrzecze, Polska

**NIP**
8521091009

**E-mail**
[contact@sumizai.com](mailto:contact@sumizai.com)

Nie publikujemy numeru telefonu, więc kanałem kontaktu jest poczta. Prawo dostępu, usunięcia, ograniczenia i sprzeciwu oraz sposób ich wykonania opisuje [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html). Możesz też złożyć skargę do Prezesa Urzędu Ochrony Danych Osobowych, ul. Stawki 2, 00-193 Warszawa. Konsumentom i przedsiębiorcom na prawach konsumenta przysługują wszystkie uprawnienia ustawowe wynikające z prawa polskiego i unijnego; nic w tym dokumencie ich nie ogranicza. Ta strona opisuje, co robi serwis — nie jest poradą prawną.

