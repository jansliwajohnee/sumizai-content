---
title: "SumizAI na Maca — Pomoc"
url: "https://sumizai.com/pl/pomoc/"
date: "2026-10-10T00:00:00+02:00"
modified: "2026-10-10T00:00:00+02:00"
description: "Pomoc w aplikacji SumizAI na Maca: formularz, podłączenie klucza AI, gdzie są notatki AI, anulowanie i przywracanie subskrypcji, usunięcie konta."
tags: ["sumizai", "app-store", "support"]
---

# SumizAI na Maca — Pomoc

Coś nie działa w Twoich notatkach AI albo masz pytanie o aplikację na Maca? Skorzystaj z formularza poniżej albo napisz na [contact@sumizai.com](mailto:contact@sumizai.com). Odpowiada człowiek. Odpowiedzi na najczęstsze pytania są poniżej.

## Jak się z nami skontaktować

Skorzystaj z [formularza](#contact-form) albo napisz na [contact@sumizai.com](mailto:contact@sumizai.com). Żebyśmy mogli szybciej pomóc, podaj:

- wersję aplikacji (zaznacz SumizAI w katalogu Aplikacje i naciśnij **⌘I**) i wersję macOS;
- co zrobiłeś, czego się spodziewałeś i co się stało — zrzut okna aplikacji bardzo pomaga;
- w sprawach konta napisz z adresu e-mail swojego konta SumizAI.

**Nigdy nie wysyłaj nam klucza do dostawcy AI ani hasła.** Nigdy o nie nie poprosimy.

## Jak podłączyć dostawcę AI?

Aplikacja działa na Twoim własnym kluczu. Utwórz klucz API w konsoli dostawcy (Anthropic, OpenAI, Google Gemini, Groq albo OpenRouter), a potem w aplikacji otwórz **Ustawienia → Dostawcy**, wybierz dostawcę, wklej klucz i zapisz. Przed pierwszym zapytaniem aplikacja pokaże, co zostanie wysłane do dostawcy, i poprosi o zgodę. Lokalna Ollama nie wymaga klucza: zainstaluj ją, uruchom i wybierz w aplikacji. Możesz też podłączyć własny serwer zgodny z API OpenAI.

Klucz jest przechowywany w pęku kluczy macOS na Twoim Macu. Za użycie modelu płacisz dostawcy na swoim koncie u niego, nie nam. Żeby przestać wysyłać dane do dostawcy, odłącz go w tym samym miejscu.

## Gdzie są moje notatki AI?

Wyłącznie na Twoim Macu. Każda notatka AI to zwykły plik Markdown (`.md`) w katalogu notatek; jego położenie zobaczysz i zmienisz w **Ustawienia → Katalog notatek**. Nic nie jest przechowywane na naszych serwerach i nie ma synchronizacji między komputerami, więc rób kopię tego katalogu (np. Time Machine). Pliki są zwykłym Markdownem. Otworzysz je w każdym edytorze tekstu.

Każdy plik zawiera tytuł, podsumowanie, rozwiniętą odpowiedź i pod spodem oryginalny czat, a spis treści vaulta leży w `base.md`. Wyszukiwanie i eksport (ZIP, PDF, PowerPoint) korzystają z tych samych plików, więc nic nie jest ukryte w formacie, który rozumie tylko SumizAI.

## Jak anulować subskrypcję?

Subskrypcją zarządza Apple. Na Macu otwórz **App Store**, kliknij swoje imię, potem **Ustawienia konta → Subskrypcje → Zarządzaj**, wybierz SumizAI i anuluj. Instrukcja Apple: [Anulowanie subskrypcji Apple](https://support.apple.com/pl-pl/118428). Anuluj najpóźniej 24 godziny przed końcem bieżącego okresu (lub okresu próbnego), żeby uniknąć kolejnej opłaty. Dostęp trwa do końca opłaconego okresu. Usunięcie aplikacji ani konta SumizAI **nie** anuluje subskrypcji.

## Jak uzyskać zwrot pieniędzy?

Płatności idą przez Apple, więc o zwrot prosisz Apple na stronie [reportaproblem.apple.com](https://reportaproblem.apple.com) ([instrukcja Apple](https://support.apple.com/pl-pl/118223)). Sami nie możemy zwrócić pieniędzy za zakup w App Store.

## Jak przywrócić zakup na nowym Macu?

Zainstaluj SumizAI z Mac App Store na tym samym Apple ID, zaloguj się na swoje konto i użyj **Przywróć zakupy** na ekranie subskrypcji. Notatki AI nie przenoszą się razem z subskrypcją: skopiuj katalog notatek na nowy Mac samodzielnie.

## „To konto jest już używane na 3 urządzeniach”

Jedno konto może być aktywne na maksymalnie trzech komputerach. Na komputerze, który jest nadal zalogowany, otwórz **Ustawienia → Urządzenia** i odłącz ten, którego już nie używasz, a potem zaloguj się ponownie na nowym. Jeśli nie masz dostępu do żadnego z nich, napisz na [contact@sumizai.com](mailto:contact@sumizai.com) z adresu e-mail swojego konta.

## Nie pamiętam hasła

Na ekranie logowania w aplikacji wybierz **Nie pamiętasz hasła?** i wpisz adres e-mail konta. Wyślemy link do ustawienia nowego hasła; działa raz, przez godzinę, a ustawienie nowego hasła wylogowuje wszystkie Twoje urządzenia. Nie ma maila? Sprawdź spam albo napisz na [contact@sumizai.com](mailto:contact@sumizai.com). Notatek AI to nie dotyczy: zostają na Twoim Macu niezależnie od tego, czy jesteś zalogowany.

## Jak usunąć konto?

W aplikacji: **Ustawienia → Usuń konto** i potwierdź. To trwale usuwa z naszego serwera konto, sesje i urządzenia. Vaulty i pliki `.md` z notatkami AI zostają na Twoim Macu. Pamiętaj, żeby osobno anulować subskrypcję w App Store (patrz wyżej). Szczegóły: [Polityka prywatności — Usunięcie konta](https://sumizai.com/pl/legal/prywatnosc.html#deleting-your-account).

## Wymagania systemowe

- Mac z **macOS 12 Monterey lub nowszym**.
- Połączenie z internetem do logowania, weryfikacji subskrypcji i korzystania z chmurowego dostawcy AI. Z lokalną Ollamą sama AI działa bez wysyłania czegokolwiek poza Twojego Maca.
- Klucz API od obsługiwanego dostawcy albo lokalna Ollama.

## Prywatność i regulamin

Co przechowujemy i dlaczego: [Polityka prywatności](https://sumizai.com/pl/legal/prywatnosc.html). Zasady subskrypcji: [Regulamin](https://sumizai.com/pl/legal/regulamin.html) oraz [standardowa EULA Apple](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/).

