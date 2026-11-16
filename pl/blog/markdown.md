---
title: "Czym jest Markdown i dlaczego to ma znaczenie?"
url: "https://sumizai.com/pl/blog/markdown.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Markdown na przykładach: podstawowa składnia, CommonMark i GFM, droga od pliku .md do strony i to, jak wyglądają notatki AI zapisane jako Markdown."
tags: ["czym jest markdown", "składnia markdown", "format markdown", "commonmark", "github flavored markdown", "plik md", "notatki ai markdown", "sumizai"]
---

# Czym jest Markdown i dlaczego to ma znaczenie?

Markdown to sposób formatowania zwykłego tekstu kilkoma znakami z klawiatury: `#` robi nagłówek, `**` pogrubienie, `-` punkt listy. Plik da się przeczytać w każdym edytorze tekstu, a program renderujący zamienia go w czysty HTML. W tym formacie SumizAI zapisuje też notatki AI, więc po składni, dialektach i pułapkach rozbieramy na części jeden prawdziwy plik notatki.

## Skąd się wziął Markdown?

Opublikował go John Gruber w 2004 roku, a Aaron Swartz pomagał mu dopracować składnię. Pierwsza implementacja była jednym skryptem w Perlu, `Markdown.pl`, który czytał plik tekstowy i wypluwał HTML.

Cel Grubera mieści się w jednym zdaniu: dokument w Markdownie ma się nadawać do publikacji jako zwykły tekst i nie wyglądać, jakby ktoś obłożył go znacznikami. Stąd nazwa, gra słów z „markup”. Piszesz mniej znaczników, resztę robi narzędzie.

Ten cel przetrwał. Otwórz dowolny `README.md` na GitHubie w widoku surowym i przeczytasz go bez mrużenia oczu.

## Jak wygląda składnia w praktyce?

Jest krótka. Część, której używasz codziennie, opanujesz w dziesięć minut. To ten sam zestaw, którym Claude i GPT formatują odpowiedzi na czacie, więc notatkom AI zbudowanym z takich odpowiedzi nic więcej nie trzeba:

`# Nagłówek` aż do `###### Nagłówek`, czyli sześć poziomów;`**pogrubienie**` i `_kursywa_`;`- punkt` albo `1. punkt` dla list, z wcięciem dla zagnieżdżenia;`[tekst](https://example.com)` dla odnośnika, to samo z `!` na początku dla obrazka;`> linia` dla cytatu;pojedyncze grawisy wokół `kodu w linii`, trzy grawisy w osobnej linii otwierają i zamykają blok kodu, a po otwierających da się dopisać nazwę języka, np. `python`;`---` w osobnej linii dla poziomej kreski.

Jedna reguła łapie prawie każdego. Pojedyncze przejście do nowej linii w akapicie nic nie daje, bo renderer skleja obie linie w jedną, więc żeby wymusić złamanie, kończysz linię dwiema spacjami albo ukośnikiem wstecznym, ewentualnie zostawiasz pustą linię i zaczynasz nowy akapit.

## Dlaczego zwykły tekst wygrał z .docx?

Plik `.md` nie potrzebuje konkretnego programu. Otworzą go TextEdit, Notatnik, Vim i VS Code, na każdym systemie, i każdy pokaże tę samą treść.

Z tego wynikają trzy praktyczne rzeczy. Git porównuje plik linijka po linijce, więc zmienione zdanie to jednolinijkowy diff, a nie podmieniony blob binarny. Przeszukasz go zwykłym `grep` albo Spotlightem. A bez żadnego renderera i tak przeczytasz tekst, najwyżej z kilkoma widocznymi gwiazdkami.

Plik `.docx` to archiwum ZIP z plikami XML: dobre dla maszyn, nieczytelne dla ludzi i związane z programem, który rozumie układ strony Worda. Przy notatkach na dziesięć lat ta różnica rozstrzyga sprawę. Dlatego format plików wraca w każdym rzetelnym porównaniu, w którym szukasz alternatywy dla Obsidiana: jeśli narzędzie trzyma notatki w plikach `.md`, odejście od niego nic nie kosztuje.

## Jeden Markdown czy wiele? CommonMark, GFM i reszta

Wiele. Opis Grubera z 2004 roku był prozą plus skryptem w Perlu i zostawiał otwarte przypadki brzegowe (zagnieżdżone wyróżnienia, punkty listy ciągnięte bez wcięcia, puste linie w listach). Każdy parser rozstrzygał je po swojemu, więc ten sam plik wyglądał na trzy sposoby.

**CommonMark** odpowiedział na to w 2014 roku. John MacFarlane, Jeff Atwood i kilka innych osób spisali dokładną specyfikację z ponad 600 przykładami testowymi, a zgodny parser daje ten sam HTML z tego samego wejścia. Od niego startuje większość dzisiejszych narzędzi.

**GitHub Flavored Markdown** to CommonMark plus tabele, przekreślenie `~~tekst~~`, listy zadań `- [ ]` i `- [x]` oraz gołe adresy URL zamieniane w odnośniki. Markdown Pandoca i MultiMarkdown idą dalej: przypisy, cytowania i listy definicji do pisania naukowego.

W praktyce: tabela GFM wygląda dobrze na GitHubie, a w ścisłej przeglądarce CommonMark zostaje rządkiem pionowych kresek. Sprawdź, jaki dialekt czytają Twoje narzędzia, zanim oprzesz się na jakiejś funkcji.

## Jak plik .md staje się stroną?

W dwóch krokach. Parser zamienia tekst w drzewo nagłówków, akapitów, punktów list i fragmentów w linii; renderer przechodzi po tym drzewie i pisze HTML, PDF przez Pandoca albo slajdy przez jeszcze inne narzędzie. SumizAI w ten sposób pokazuje notatki AI na ekranie, a plik pod spodem zostaje zwykłym tekstem.

Drzewo pośrodku umożliwia rozszerzenia. Biblioteki takie jak `remark` w JavaScripcie i `cmark` w C pozwalają wtyczce zmieniać drzewo zamiast puszczać wyrażenia regularne po surowym tekście, więc podstawowa składnia zostaje nienaruszona.

Ostrzeżenie dla każdego, kto renderuje Markdown pisany przez obcych: większość parserów domyślnie przepuszcza surowy HTML, a znacznik `<script>` w polu komentarza to podręcznikowa dziura XSS. Oczyszczaj wynik.

## Front matter, escapowanie i szczegóły, które poznaje się później

Front matter w YAML to blok między dwiema liniami `---` na samej górze pliku. Renderery go ukrywają, narzędzia czytają jako dane: Hugo i Jekyll biorą stamtąd tytuł i datę, aplikacje do notatek trzymają identyfikatory i znaczniki czasu. Każda notatka AI w SumizAI zaczyna się od takiego bloku, pokazanego niżej.

Druga lekcja to escapowanie. Napisz w zdaniu nazwę pliku `moj_szkic_v2.md`, a połowa zrobi się kursywą, bo podkreślnik oznacza wyróżnienie. Ukośnik wsteczny przed znakiem albo grawisy wokół całej nazwy rozwiązują problem.

Trzecia niespodzianka to przypisy: działają w GFM i u Pandoca, w czystym CommonMarku nie.

## Kiedy Markdown jest złym wyborem?

Przy składzie. Nie ma kolumn, rozmiarów strony ani kontroli nad krojem pisma, więc drukowana broszura należy do programu do składu.

Przy danych również. Tabela w Markdownie jest dla ludzi; konfiguracja i dane dla API należą do JSON, YAML albo TOML, które programy parsują bez zgadywania.

I przy bardzo długich książkach technicznych. AsciiDoc i reStructuredText mają wbudowane dołączanie plików, odsyłacze i bloki ostrzeżeń, a Markdown dostaje je tylko z rozszerzeń. Przy podręczniku na 400 stron surowsza składnia się opłaca. Notatek AI żadne z tych ograniczeń nie dotyczy: to proza z nagłówkami, listami i od czasu do czasu tabelą.

## Jak wygląda notatka AI zapisana jako plik Markdown?

Gdy odpowiedź z czatu jest warta zachowania, SumizAI zapisuje ją w folderze vaulta jako jedną z Twoich notatek AI, a plik to zwykły Markdown z odrobiną struktury. Notatka o tytule „Wysiew pomidorów na rozsadę” ląduje w `notes/wysiew-pomidorow-na-rozsade.md`: tytuł małymi literami, bez polskich znaków i akcentów, słowa połączone łącznikiem.

Notatka „Wysiew pomidorów na rozsadę” w vaulcie Ogród przydomowy. Na dysku to jeden plik .md.

Od góry do dołu plik zawiera:

front matter z polami `id`, `title`, `summary`, `section` (rozdział w spisie treści vaulta), `created` i `updated`;nagłówek H1 z tytułem, a pod nim treść notatki;sekcję `## Pełna treść`, jeśli notatka ma wersję rozwiniętą;`## Materiał źródłowy`, gdzie każda wymiana stoi jako **Pytanie** i **Odpowiedź**, słowo w słowo.

Między sekcjami siedzą komentarze HTML w rodzaju `<!-- sumizai:sources -->`. Żaden podgląd Markdowna ich nie pokazuje. Są potrzebne, bo odpowiedzi modelu pełne są własnych nagłówków `##`, więc nagłówek nigdy nie wyznaczyłby pewnie miejsca, gdzie zaczyna się źródło.

Odnośniki między notatkami to zwykłe linki Markdown, `[Podlewanie rozsady](podlewanie-rozsady.md)`, nigdy `[[wiki-linki]]`. Model dostaje mapę istniejących tytułów i plików i linkuje tylko do nich, więc nic nie wskazuje pliku, którego nie ma. Obsidian domyślnie tworzy `[[wiki-linki]]`, ale standardowe linki czyta równie dobrze.

## Obsidian alternatywa na zwykłym Markdownie

W tym pliku nic nie należy do aplikacji. Folder vaulta otwiera się w Obsidianie bez konwersji i w tym praktycznym sensie SumizAI to [Obsidian alternatywa](/pl/alternative-to/sumizai-alternative-to-obsidian.html): pisze notatki AI z Twoich rozmów, a Obsidian, VS Code czy GitHub czytają potem te same pliki.

Lokalna baza danych to tylko indeks do wyszukiwania. Zapisem są pliki `.md`, a spis treści vaulta też jest plikiem, `base.md`. Eksport vaulta daje archiwum ZIP z `base.md` i folderem `notes/`, z odnośnikami względnymi.

Jeśli szukasz alternatywy dla Obsidiana, która sama zapełnia vault, sprawdź tę cechę jako pierwszą. Jak [aplikacja do notatek AI](/pl/) zamienia czat w plik, opisują artykuły poniżej.

