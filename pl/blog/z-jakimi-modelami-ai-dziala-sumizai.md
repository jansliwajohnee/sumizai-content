---
title: "Z jakimi modelami AI działa SumizAI?"
url: "https://sumizai.com/pl/blog/z-jakimi-modelami-ai-dziala-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Notatki AI pisze Claude, GPT, Gemini, Groq, OpenRouter, lokalna Ollama albo Twój serwer. Zawsze na Twoim kluczu API, z listą modeli prosto od dostawcy."
tags: ["byok aplikacja ai", "notatki z claude", "notatki openai", "lokalna ollama notatki", "openrouter", "sumizai"]
---

# Z jakimi modelami AI działa SumizAI?

Każdą notatkę AI w SumizAI pisze model, który sam podłączasz. Aplikacja nie sprzedaje tokenów i nie ma własnego modelu: wybierasz jednego z **siedmiu dostawców**, wklejasz klucz API albo adres serwera, a każde zapytanie idzie z Twojego Maca prosto do tego dostawcy.

## Kto może pisać Twoje notatki AI?

Siedmiu dostawców: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, lokalna Ollama i własny serwer zgodny z API OpenAI. Każdy z nich napisze Twoje notatki AI, a podłączyć możesz kilku naraz.

Za tymi nazwami stoją tylko dwa klienty. Anthropic ma własny, bo jego Messages API wygląda inaczej. Pozostała szóstka przyjmuje zapytania w stylu OpenAI: aplikacja wysyła `/chat/completions`, czyta `/models`, a do Gemini trafia przez zgodny z OpenAI endpoint Google. Dlatego siódme miejsce, _Własny serwer_, nie potrzebuje osobnej integracji.

Wszystko ustawiasz w Ustawieniach, w sekcji Dostawcy. Wybierasz dostawcę, wklejasz klucz, klikasz _Podłącz_, potem _Testuj_. Status ma trzy wartości: _Połączony_ (dostawca odpowiedział na ten klucz), _Niesprawdzony_ (klucz zapisany, nikt go nie wywołał) i _Brak połączenia_. Środkowa istnieje po to, żeby klucz z literówką nie wyglądał na działający.

## Po co własny klucz?

Odsprzedaż tokenów to marża od każdego z nich. Marża nie mieści się w 1 USD miesięcznie. SumizAI bierze pieniądze za aplikację, a rachunek za model wystawia Ci dostawca, po swojej stawce, z kredytami i darmowym progiem, które już masz.

Groq ma darmowy próg, OpenRouter pokazuje darmowe modele, a Anthropic i OpenAI liczą za tokeny. Lista modeli oznacza każdą pozycję jako _Darmowe_, _Darmowy próg_ albo _Płatne_, więc koszt widzisz przed pierwszym pytaniem. Klucz jest zapisany w postaci zaszyfrowanej i po zapisaniu nie pokazuje się już w całości.

## Co wychodzi z Twojego Maca i kiedy?

Nic, dopóki się nie zgodzisz. Zanim dostawca dostanie cokolwiek, okno _Wysyłać dane do Anthropic?_ (albo do tego, którego wybrałeś) wymienia, co pójdzie: Twoje pytania i historię rozmowy, fragmenty notatek używane jako kontekst oraz importowane dokumenty. Odmowa oznacza, że wywołania nie ma. Odłączenie dostawcy wycofuje zgodę, a ponowne podłączenie pyta jeszcze raz.

Kontekst ma sufit. Pytanie niesie spis treści vaulta i pełną treść najwyżej pięciu najtrafniejszych notatek AI, w limicie 24 000 znaków, a pod odpowiedzią widać _Odpowiedź korzysta z Twoich notatek_ z ich listą. Model nigdy nie czyta całego vaulta, a serwery SumizAI nie dostają z tego nic.

## Skąd się bierze lista modeli?

Od dostawcy, pytanego Twoim kluczem. W kodzie nie ma wbudowanego katalogu.

Lista wpisana na sztywno starzeje się w miesiąc: proponuje model, który dostawca już wycofał, i dowiadujesz się o tym, kiedy notatka się nie zapisze. Aplikacja czyta więc endpoint `/models` i go filtruje. Modele do osadzeń, obrazów, mowy i transkrypcji odpadają, bo z nimi nie porozmawiasz. Datowana migawka typu `-001` obok tego samego modelu bez przyrostka pojawia się raz, a starsze pokolenie obok nowszego z tej samej rodziny znika.

Reszta stoi w dwóch grupach, _Darmowe_ nad _Płatnymi_, w każdej od najmocniejszego. Przy OpenRouterze, gdzie surowa lista ma setki pozycji, dopiero ta kolejność daje się przewijać.

## Ile wywołań modelu kosztuje jedna notatka AI?

Trzy albo cztery. Najpierw strumieniem płynie odpowiedź, do 4 096 tokenów. Potem, w tle, aplikacja pisze szkic notatki (tytuł, podsumowanie, rozwinięcie), porównuje go z podobnymi notatkami pod kątem duplikatu (ok. 800 tokenów odpowiedzi) i wybiera rozdział (ok. 300).

Wszystko idzie na model z pola _Model odpowiadający w czacie_. Ustawienia podają też model do operacji pomocniczych (tytuł, podsumowanie, dopasowanie tematu); w aplikacji na Maca to ten sam model. Tańszy pomocnik obniżyłby koszt i spłaszczył podsumowania, a podsumowanie to linijka notatki, którą czytasz najczęściej.

## Który dostawca jest najszybszy u Ciebie?

Zmierz to. _Test szybkości dostawców_ w Ustawieniach wysyła krótkie zapytanie do każdego podłączonego dostawcy i mierzy prawdziwy czas odpowiedzi z tej maszyny, teraz. Publiczne rankingi uśredniają cudze łącza; Twoje opóźnienie do Groqa we wtorek wieczorem to inna liczba.

Wynik to pasek czasu i osobno gwiazdki jakości, które są naszą oceną redakcyjną, a nie pomiarem. Etykieta _rekomendowany_ trafia do najlepszego jakościowo dostawcy spośród tych, które odpowiedziały w podobnym czasie.

## Co się dzieje, gdy dostawca odmawia?

Dostajesz prawdziwy powód. Kod 401 albo 403 zamienia się w komunikat _Dostawca odrzucił Twój klucz API_ i aplikacja go nie ponawia. Kod 404 znaczy, że modelu już nie ma, więc znika z listy.

Dzienny limit (HTTP 429) to inna sprawa. Model dostaje oznaczenie _limit wyczerpany · wraca o_ danej godzinie na 24 godziny, a okno proponuje inny model z zapasem, żeby przerwana praca dokończyła się na nim.

Pułapka dla budujących coś podobnego: Anthropic odrzuca bezpośrednie wywołania z aplikacji desktopowej bez jawnego nagłówka zgody, a odmowa wygląda jak zły klucz. Aplikacja ten nagłówek wysyła.

## Czy wszystko może zostać na Twoim komputerze?

Tak, z Ollamą. Jej domyślny adres `127.0.0.1:11434` jest już wpisany, klucz nie jest potrzebny. Wpisz samo `host:port` innej maszyny w sieci, a aplikacja dopisze `http://` i `/v1`.

Z lokalnym modelem pytanie, kontekst i odpowiedź nie dotykają cudzego serwera, a notatki AI lądują jako zwykłe pliki `.md` w katalogu vaulta, który wskazałeś.

## Czy notatki od różnych modeli mieszają się w jednym vaulcie?

Tak. Zmień w połowie tygodnia Claude na model z Groqa, a następna notatka ma po prostu innego autora. Format się nie zmienia, oryginalne pytanie i odpowiedź leżą pod spodem słowo w słowo, a linki to zwykłe linki Markdown do prawdziwych plików.

Ten zwykły katalog sprawia, że SumizAI sprawdza się jako Obsidian alternatywa dla osób zmęczonych pisaniem każdej strony ręcznie: model pisze i odkłada, a Obsidian dalej otwiera wynik. Szczegóły podziału opisuje strona [SumizAI jako alternatywa dla Obsidiana](/pl/alternative-to/sumizai-alternative-to-obsidian.html), a resztę aplikacji przedstawia [aplikacja do notatek AI](/pl/).

Dostawcy w Ustawieniach: Połączony, Niesprawdzony albo Brak połączenia, a model do czatu wybierany z listy samego dostawcy.

## Czy mój materiał trafia do trenowania modeli?

Nie przez SumizAI. Nie ma tu żadnego trenowania ani serwera z Twoimi notatkami.

Co dostawca robi z ruchem API, ustala Twoja umowa z nim, i to kolejny powód, żeby klucz był Twój: czytasz warunki, wybierasz i zmieniasz dostawcę bez przenoszenia notatek AI. Jeśli wpisujesz w wyszukiwarkę „Obsidian alternatywa” i chcesz mieć AI w środku, odpowiedź jest prosta: model wybierasz spośród siedmiu dostawców, a jego zmiana nie rusza niczego w katalogu.

