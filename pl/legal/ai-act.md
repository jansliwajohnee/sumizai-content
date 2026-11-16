---
title: "Informacja o AI Act"
url: "https://sumizai.com/pl/legal/ai-act.html"
date: "2026-10-17T00:00:00+02:00"
modified: "2026-10-17T00:00:00+02:00"
description: "Jak działa AI w SumizAI w świetle rozporządzenia (UE) 2024/1689: co pisze model, jaka jest nasza rola i czego AI nie gwarantuje."
tags: ["sumizai", "legal", "ai-act"]
---

# Informacja o AI Act

SumizAI zamienia pytanie i odpowiedź w notatkę, a pisze ją model językowy. Ta informacja mówi wprost, które elementy produktu są sztuczną inteligencją, kto za co odpowiada na gruncie rozporządzenia (UE) 2024/1689 (akt o sztucznej inteligencji) i w których miejscach wyniku nie należy przyjmować bez przeczytania.

## Czym jest ta informacja

To informacja o przejrzystości dotycząca sztucznej inteligencji działającej w SumizAI. Jest napisana dla osób korzystających z produktu, nie dla urzędu, i dotyczy rozporządzenia (UE) 2024/1689 — aktu o sztucznej inteligencji — którego obowiązki przejrzystości z art. 50 stosuje się od 2 sierpnia 2026 r.

Operatorem SumizAI jest **10UP Jan Śliwa**, Kminkowa 26, 72-003 Bezrzecze, Polska, NIP 8521091009, kontakt [contact@sumizai.com](mailto:contact@sumizai.com).

To informacja, a nie porada prawna, i nie ogranicza żadnego uprawnienia przysługującego Ci na podstawie aktu o sztucznej inteligencji, RODO, prawa polskiego ani unijnego prawa konsumenckiego. Konsumenci oraz _przedsiębiorcy na prawach konsumenta_ zachowują wszystkie uprawnienia ustawowe niezależnie od treści naszych dokumentów.

Nazwa „SumizAI” obejmuje trzy różne rzeczy, więc ta informacja za każdym razem wskazuje, o której mówi: **strona** sumizai.com, **aplikacja desktopowa** oraz zamrożona, starsza **aplikacja webowa** pod adresem app.sumizai.com. Na samej stronie nie ma żadnej sztucznej inteligencji.

## Co naprawdę robi model

SumizAI opiera się na jednej pętli: zadajesz pytanie, model odpowiada, a odpowiedź staje się notatką. Model bierze udział w każdym kroku tej pętli.

**Odpowiada na pytanie**
Odpowiedź, którą czytasz w rozmowie, jest generowana przez model, a nie pobierana z bazy gotowych odpowiedzi.

**Najpierw czyta fragment Twojego zbioru notatek**
Do dostawcy trafia nie tylko wpisane pytanie. Trafia też spis treści zbioru oraz pełny tekst **maksymalnie pięciu** notatek uznanych za najbardziej powiązane, w budżecie **24 000 znaków**. Aplikacja pokazuje, których notatek użyła.

**Pisze notatkę**
Pełny tekst pytania i odpowiedzi jest wysyłany ponownie, żeby model przygotował notatkę: jej **tytuł**, **streszczenie** i **treść** pisze model. Nie uzupełniasz szablonu.

**Decyduje, gdzie notatka trafi**
Model umieszcza nową notatkę w spisie treści zbioru — wybór miejsca to decyzja modelu, a nie reguła z Twoich ustawień.

**Ocenia duplikaty**
Model porównuje nowy materiał z tym, co już jest w zbiorze, i ocenia, czy powiela istniejącą notatkę.

Wszystko to dzieje się automatycznie, w jednym przebiegu, bez proszenia Cię o potwierdzenie każdego kroku.

**Dokąd idzie zapytanie.** W **aplikacji desktopowej** zapytanie idzie bezpośrednio z Twojego urządzenia do wybranego dostawcy. Nie przechodzi przez żaden serwer SumizAI, a my nigdy nie widzimy pytania, odpowiedzi ani notatki. W zamrożonej **aplikacji webowej** pod adresem app.sumizai.com zapytanie wysyła serwer, odszyfrowując na potrzeby pojedynczego żądania zapisany klucz dostawcy.

## Nasza rola: podmiot stosujący, nie dostawca modelu

Akt o sztucznej inteligencji odróżnia podmiot, który buduje model i wprowadza go do obrotu, od podmiotu, który go stosuje. Jesteśmy tym drugim.

- Jesteśmy **podmiotem stosującym**: wbudowujemy w aplikację do notatek modele ogólnego przeznaczenia zbudowane przez inne firmy.
- **Nie jesteśmy dostawcą modelu AI ogólnego przeznaczenia.** Nie trenujemy, nie dostrajamy i nie hostujemy żadnego modelu. SumizAI nie ma własnych zdolności AI.
- Model **wybierasz Ty**, w ustawieniach, spośród siedmiu opcji: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, lokalna instancja Ollama albo dowolny inny zgodny z OpenAI adres, który sam wpiszesz.
- Model działa na **Twoim własnym kluczu API**. Klucz wnosisz Ty; aplikacja nie ma u żadnego dostawcy konta, limitu ani środków. Lokalna Ollama może w ogóle nie wymagać klucza — a w wersji desktopowej, gdzie zapytanie wychodzi z Twojego komputera, przy lokalnej Ollamie nic tego komputera nie opuszcza.

Firma stojąca za wybranym przez Ciebie modelem jest jego dostawcą i to na niej spoczywają obowiązki dostawcy, w tym obowiązki dotyczące modeli ogólnego przeznaczenia. Twoja relacja z tą firmą jest Twoją relacją: jej regulamin, jej cennik, jej zasady przetwarzania danych. Nie jesteśmy jej stroną, a w produkcie desktopowym nie moglibyśmy zajrzeć w ten ruch, nawet gdybyśmy chcieli.

## Klasyfikacja ryzyka: ryzyko ograniczone

SumizAI to system AI **ograniczonego ryzyka**. Obowiązek, który go dotyczy, to przejrzystość z art. 50 — poinformowanie Cię, że masz do czynienia z AI i że notatki pisze AI. Robi to właśnie ten dokument.

**To nie jest system wysokiego ryzyka z załącznika III.** Załącznik III wymienia obszary, w których system AI rozstrzyga o czymś istotnym dla człowieka. SumizAI nie robi nic z tej listy:

- Nie prowadzi identyfikacji biometrycznej, kategoryzacji biometrycznej ani rozpoznawania emocji.
- Nie służy do zarządzania infrastrukturą krytyczną ani jej eksploatacji.
- W edukacji nie decyduje o przyjęciu, nie ocenia efektów uczenia się, nie przypisuje poziomu i nikogo nie nadzoruje podczas egzaminu. Pisze notatki dla osoby, która zadała pytanie, i nikogo nie ocenia.
- Nie uczestniczy w rekrutacji, przydzielaniu zadań, awansach ani rozwiązywaniu umów.
- Nie decyduje o dostępie do świadczeń publicznych ani usług prywatnych, nie ocenia zdolności kredytowej, nie wycenia ubezpieczeń i nie kwalifikuje zgłoszeń alarmowych.
- Nie jest używany w kontekście ścigania przestępstw, migracji, granic ani azylu.
- Nie ma żadnej roli w sprawowaniu wymiaru sprawiedliwości ani w procesach demokratycznych.

Nie jest też związanym z bezpieczeństwem elementem produktu z załącznika I. Skoro nie jest systemem wysokiego ryzyka, nie ma tu oceny zgodności, oznakowania CE, wpisu do bazy UE ani udziału jednostki notyfikowanej — i niczego takiego nie deklarujemy. Nie posiadamy dla tego produktu żadnego certyfikatu.

## Obowiązki przejrzystości i sposób ich realizacji

Poniższa tabela wymienia każdy punkt przejrzystości, jego status u nas oraz sposób realizacji. Tam, gdzie czegoś nie wdrożyliśmy, jest to napisane wprost.

| Obowiązek | Status | Jak jest realizowany |
|---|---|---|
| Art. 50 ust. 1 — człowiek musi wiedzieć, że wchodzi w interakcję z systemem AI | Spełniony | Produkt jest w całości przedstawiany jako notatnik oparty na AI: to Ty wybierasz dostawcę i model, to Ty wklejasz własny klucz, a aplikacja pokazuje, które notatki trafiły do modelu przy danej odpowiedzi. |
| Art. 50 ust. 2 — oznaczanie treści syntetycznych w formacie nadającym się do odczytu maszynowego | **Nie wdrożone po naszej stronie** | Notatki zapisujemy jako zwykłe pliki Markdown i nie dodajemy do nich znaku wodnego ani żadnego znacznika maszynowego mówiącego, że powstały z użyciem AI. To, czy dostawca modelu oznacza własne wyniki, zależy od niego i nie możemy tego obiecać. Przyjmij, że każda notatka w zbiorze SumizAI jest napisana przez AI. |
| Art. 50 ust. 3 — rozpoznawanie emocji i kategoryzacja biometryczna | Nie dotyczy | Nie prowadzimy ani jednego, ani drugiego. Produkt pracuje na tekście, który wpisujesz, i na notatkach, które już masz. |
| Art. 50 ust. 4 akapit pierwszy — ujawnianie treści typu deepfake (obowiązek podmiotu stosującego) | Nie dotyczy | Produkt generuje wyłącznie tekst. Nie ma w nim generowania obrazu, dźwięku ani wideo. |
| Art. 50 ust. 4 akapit drugi — ujawnianie tekstu wygenerowanego przez AI publikowanego w celu informowania opinii publicznej o sprawach leżących w interesie publicznym (obowiązek podmiotu stosującego) | Nie dotyczy | SumizAI niczego nie publikuje. Notatka powstaje w Twoim własnym zbiorze: w wersji desktopowej w pliku na Twoim dysku, a w zamrożonej, starszej aplikacji webowej w zasobach Twojego konta w tej aplikacji. Nic nie trafia do żadnych odbiorców. |
| Art. 50 ust. 5 — informacja ma być jasna i przekazana najpóźniej przy pierwszej interakcji | Spełniony przez publikację | Ta informacja jest opublikowana na sumizai.com i linkowana ze stopki każdej strony, obok polityki prywatności i regulaminu. Za to odpowiadamy; nie twierdzimy natomiast, że sama aplikacja powtarza tę informację przy pierwszym uruchomieniu. |
| Art. 4 — kompetencje w zakresie AI po stronie osób korzystających z systemu | Realizowany dokumentacyjnie | Ta informacja wyjaśnia, co robi model, co jest wysyłane do dostawcy i gdzie wynik zawodzi. Poza dokumentacją nie prowadzimy programu szkoleń. |
| Ocena zgodności, oznakowanie CE, rejestracja, certyfikacja | Brak — i niczego nie deklarujemy | Dotyczą systemów wysokiego ryzyka. SumizAI nim nie jest, więc żadnej takiej procedury nie przeprowadzono i w żadnym naszym dokumencie nie ma takiego twierdzenia. |

## Nadzór człowieka: recenzentem jesteś Ty

Nic, co napisze model, nie jest publikowane ani pokazywane komukolwiek poza Tobą. Notatka powstaje i zapisuje się w Twoim własnym zbiorze — w wersji desktopowej w plikach na Twoim dysku, a w zamrożonej, starszej aplikacji webowej w zasobach Twojego konta w tej aplikacji — i tam czeka na Ciebie.

- Czytasz odpowiedź, zanim cokolwiek z niej wyniknie.
- Możesz notatkę poprawić, napisać od nowa albo usunąć. W wersji desktopowej notatki to zwykłe pliki Markdown w wybranym przez Ciebie folderze, więc otworzy je dowolny edytor.
- Możesz przenieść notatkę, jeśli model umieścił ją w złym miejscu, i zachować notatkę, którą model uznał za duplikat.
- Jedyne wychodzące zapytanie AI to wywołanie wybranego przez Ciebie dostawcy, z opisaną wyżej treścią. SumizAI niczego nie publikuje i niczego w Twoim imieniu nikomu nie udostępnia.

Powiedzmy sobie jedno uczciwie: **produkt nie wymusza na Tobie sprawdzenia**. Dziś nie ma obowiązkowego kroku akceptacji — notatka powstaje i zapisuje się w jednym przebiegu. Nadzór jest realny, ale to Ty go sprawujesz, i ma największe znaczenie wtedy, gdy później opierasz się na notatce, której nikt nie przeczytał.

**Nie zapada żadna decyzja wobec Ciebie.** Model pisze tekst; nikogo nie ocenia, nie profiluje, nie punktuje ani nie szereguje, a w SumizAI nie powstaje decyzja opierająca się wyłącznie na zautomatyzowanym przetwarzaniu, która wywoływałaby wobec Ciebie skutki prawne lub podobnie istotne w rozumieniu art. 22 RODO. Jakie dane osobowe w ogóle występują, kto jest ich administratorem oraz jak wykonać prawo dostępu, sprostowania, usunięcia, ograniczenia, sprzeciwu i przenoszenia danych, opisuje [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html). Jeżeli Twoje notatki lub pytania zawierają dane osobowe innych osób, wysłanie ich do wybranego dostawcy jest Twoją decyzją i to Ty odpowiadasz za podstawę prawną.

## Wybór modelu, wersje i regulamin Twojego dostawcy

**Nie przypinamy wersji modelu.** Wybierasz dostawcę i nazwę modelu; firma stojąca za tą nazwą może w każdej chwili podmienić model, którego ta nazwa dotyczy, wycofać go albo zmienić jego zachowanie — i nie musi nas o tym informować. To samo pytanie może więc jutro dać inną odpowiedź, a notatka sprzed miesiąca została napisana przez to, czym ten model był miesiąc temu. Nie potrafimy odtworzyć dawnego wyniku i nie obiecujemy powtarzalności.

**O tym, czy Twoje treści posłużą do trenowania, decyduje Twój dostawca, nie my.** Zapytanie — pytanie, spis treści i notatki wybrane jako kontekst — jest wysyłane na koncie, którego klucz API został wklejony w ustawieniach. To, co ta firma z nim robi, regulują warunki tego konta. Przeczytaj je. Wielu dostawców traktuje płatny ruch API inaczej niż swoje konsumenckie czaty, a część daje na to ustawienie; to ustawienie jest u nich, nie w SumizAI.

Praktyczne wnioski:

- Jeśli nie chcesz, by notatki w ogóle opuszczały Twój komputer, korzystaj z aplikacji desktopowej z lokalnym modelem w Ollamie: zapytanie wysyła wtedy Twoje urządzenie i żadne połączenie do podmiotu trzeciego nie następuje. W zamrożonej, starszej aplikacji webowej notatki są już na serwerze i to on wykonuje zapytanie, więc lokalny model na Twoim komputerze nie wchodzi w grę.
- Jeśli w opcji własnej wskażesz swój zgodny z OpenAI adres, ten adres oceniasz we własnym zakresie — nie wiemy o nim nic.
- Zmiana dostawcy zmienia styl odpowiedzi, ocenę duplikatów i miejsce notatki w spisie treści. To wszystko są decyzje modelu.

## Praktyki zakazane (art. 5): nie stosujemy żadnej

Art. 5 aktu o sztucznej inteligencji zakazuje wprost krótkiej listy praktyk. SumizAI nie stosuje żadnej z nich i potwierdzamy to bez ogródek:

- Brak technik podprogowych, manipulacyjnych lub wprowadzających w błąd, które zniekształcają zachowanie.
- Brak wykorzystywania wieku, niepełnosprawności ani sytuacji społecznej lub ekonomicznej.
- Brak scoringu społecznego osób lub grup.
- Brak przewidywania przestępstw na podstawie profilowania lub cech osobowości.
- Brak nieukierunkowanego pobierania wizerunków twarzy w celu budowy bazy rozpoznawania.
- Brak wnioskowania o emocjach w miejscu pracy i w edukacji.
- Brak kategoryzacji biometrycznej w celu wnioskowania o rasie, poglądach politycznych, przynależności związkowej, wyznaniu, życiu seksualnym lub orientacji seksualnej.
- Brak zdalnej identyfikacji biometrycznej w czasie rzeczywistym w przestrzeni publicznej.

Produkt przyjmuje wpisany tekst i czyta notatki ze zbioru, który kontrolujesz. Nie ma żadnego wejścia biometrycznego, nie buduje Twojego profilu i nie podejmuje decyzji wobec żadnej osoby.

## Czego AI nie robi dobrze

Modele językowe tworzą płynny tekst niezależnie od tego, czy jest prawdziwy. To jest sekcja, którą warto zapamiętać.

- **Halucynacje.** Model potrafi wymyślić fakty, daty, źródła, cytaty i przypisy — i poda je tak samo pewnym tonem jak resztę. Notatka z SumizAI nie jest dokumentem zweryfikowanym.
- **Ograniczony wgląd w zbiór.** Każda odpowiedź powstaje ze spisu treści i **najwyżej pięciu** notatek, w limicie **24 000 znaków**. Jeśli odpowiedź zależała od szóstej notatki albo od tej części długiej notatki, która nie zmieściła się w budżecie, model jej nie zobaczył. Aplikacja pokazuje, których notatek użyła — warto na tę listę spojrzeć.
- **Błędna ocena duplikatów.** Model może uznać naprawdę nową notatkę za duplikat albo nie zauważyć rzeczywistego powtórzenia.
- **Błędne umiejscowienie.** Notatka może trafić pod niewłaściwy nagłówek w spisie treści.
- **Brak gwarancji poprawności.** Nie zapewniamy — wprost ani w sposób dorozumiany — że odpowiedź, tytuł, streszczenie czy treść notatki są poprawne, kompletne lub przydatne do określonego celu.
- **To nie jest porada specjalisty.** Nie opieraj wyłącznie na wyniku SumizAI decyzji medycznych, prawnych, finansowych, podatkowych, dotyczących bezpieczeństwa ani innych o istotnych skutkach. Sprawdź to, co ważne, w źródle, któremu ufasz.

Ta sekcja nie narusza ustawowych uprawnień konsumentów ani _przedsiębiorców na prawach konsumenta_ wynikających z prawa polskiego i unijnego.

## Jak to się ma do pozostałych dokumentów

Ta informacja opisuje sztuczną inteligencję. Sąsiednie dokumenty opisują resztę:

- [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html) — jakie dane istnieją, gdzie są i kto jest ich administratorem. W skrócie: aplikacja trzyma notatki na Twoim urządzeniu i wysyła nam tylko to, czego wymaga konto i subskrypcja; strona używa analityki po zgodzie.
- [Regulamin](https://sumizai.com/pl/legal/regulamin.html) — umowa, zasady korzystania z produktu i granice naszej odpowiedzialności.
- [DPA](https://sumizai.com/pl/legal/dpa.html) — umowa powierzenia przetwarzania, która ma sens wyłącznie dla aplikacji webowej, bo w produkcie desktopowym nie przetwarzamy niczego w Twoim imieniu.
- [Polityka cookies](https://sumizai.com/pl/legal/cookies.html) — analityka na stronie oraz niezbędne pliki cookie aplikacji webowej. Aplikacja desktopowa nie ustawia żadnych cookies.
- [Zwroty](https://sumizai.com/pl/legal/zwroty.html) — opublikowana oferta i prawo odstąpienia.

Jeżeli ta informacja i inny dokument wydają się mówić co innego o AI, napisz na [contact@sumizai.com](mailto:contact@sumizai.com) — poprawimy zapis, zamiast spierać się, który ma pierwszeństwo.

## Przegląd i zmiany

Fakty w tej informacji zweryfikowano ze źródłami produktu **14 sierpnia 2026 r.**, a wersja i data są wydrukowane u góry strony.

Przeglądamy ją, gdy produkt zmienia się w zakresie, który ten dokument opisuje — nowy dostawca, zmiana tego, ile ze zbioru notatek jest wysyłane, zmiana tego, co model rozstrzyga samodzielnie — oraz gdy akt o sztucznej inteligencji lub wytyczne do niego zmieniają to, co trzeba napisać. Nieaktualne zdania zastępujemy, a nie po cichu łagodzimy: jeśli obowiązek przejdzie z „nie wdrożone” na „spełniony”, tabela to pokaże.

Dalsze korzystanie z SumizAI po zmianie oznacza korzystanie z wersji wtedy opublikowanej. Nic w tej informacji nie nakłada na Ciebie obowiązku akceptacji czegokolwiek — to opis działania systemu.

## Kontakt

Pytania o AI w SumizAI — co jest wysyłane, co rozstrzyga model, dlaczego notatka wyszła tak, a nie inaczej — trafiają do człowieka:

- **10UP Jan Śliwa**, jednoosobowa działalność gospodarcza wpisana do CEIDG
- Kminkowa 26, 72-003 Bezrzecze, Polska
- NIP 8521091009
- [contact@sumizai.com](mailto:contact@sumizai.com)

Pytania o sam model — jego dane treningowe, zabezpieczenia, własną dokumentację na gruncie aktu o sztucznej inteligencji — należą do firmy stojącej za wybranym przez Ciebie modelem. Możemy powiedzieć, co i kiedy wysyła SumizAI; nie odpowiemy za to, co dzieje się wewnątrz cudzego modelu.

Drogi skargowe są dwie i nie są tym samym. Jeżeli skarga dotyczy **danych osobowych** — tego, co jest przechowywane, co zostało wysłane albo żądania, na które nie odpowiedzieliśmy — możesz złożyć ją do Prezesa Urzędu Ochrony Danych Osobowych, ul. Stawki 2, 00-193 Warszawa. Jeżeli skarga dotyczy **samego systemu AI**, akt o sztucznej inteligencji daje Ci prawo złożenia skargi do właściwego krajowego organu nadzoru rynku; w Polsce jest to organ wskazany w przepisach krajowych wdrażających to rozporządzenie. Żadna z tych dróg nie odbiera Ci możliwości napisania najpierw do nas i żadnej z nich nic w tej informacji nie ogranicza.

Nie publikujemy numeru telefonu, więc kanałem kontaktu jest poczta elektroniczna.

