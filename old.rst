Typesetting Guide
=================

.. _by-gruzin0911-last-updated-20221123:

By: Gruzin#0911, Last Updated: 2022.11.23
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

--------------

Programy
--------

Kainote
~~~~~~~

| Kainote jest open-sourceowym forkiem popularnego programu do tworzenia
  napisów, Aegisuba, autorstwa bjakja (Bakura), pozwalającym na bardziej
  zaawansowaną edycje efketów.
| Najnowszą wersję Kainote można pobrać z
  `githuba <https://github.com/bjakja/Kainote/releases/latest>`__
| Lub `niestabilny build
  2022.11.11 <https://drive.google.com/uc?id=1ECqsrLo5d1jPoz-FKvJrS0279YeTKrmS&export=download>`__

Boris FX Mocha Pro
~~~~~~~~~~~~~~~~~~

| Mocha jest najlepszym dostępnym obecnie na rynku narzędziem do
  trackowania ruchu.
| Dostępna jest jako:

1. rozszerzenie do Adobe After Effects
2. osobne oprogramowanie, możesz je pobrać tutaj:
   **UWAGA: PONIŻSZY LINK PROWADZI DO TORRENTA, OPROGRAMOWANIE Z TAKICH
   LINKÓW POWINNO DLA BEZPIECZEŃSTWA POBIERAĆ SIĘ POPRZEZ SERWISY VPN,
   SPRAWDŹ CZY PROGRAM NIE JEST SKAŻONY WIRUSEM PRZED URUCHOMIENIEM**
   `Boris FX Mocha PRO 2022 na
   1337x.to <https://1337x.to/torrent/4423707/Boris-FX-Mocha-Pro-2020-5-v7-5-0-Build-1274-Plug-ins-for-Adobe-OFX-CrackzSoft/>`__
   Z plików znajdujących się w torrencie potrzebna jest ci wersja
   standalone, instrukcja instalacji powinna znajdować się w odpowiednim
   pliku ``read_me.txt``.

QuickTime Player
~~~~~~~~~~~~~~~~

Dla pełnej sprawności Mochy wymagany jest też odtwarzacz `QuickTime
Player <https://support.apple.com/kb/dl837?locale=en_US>`__

x264 i ffmpeg
~~~~~~~~~~~~~

Są to dwa największe, open-sourcowe narzędzia do manipulacji wideo, są
one wykorzystywane przez Kainote'a, a także przez wiele zewnętrznych
skryptów. Lepszym rozwiązaniem jest x264, jednak warto jest mieć oba na
komputerze

Windows
~~~~~~~

.exe
^^^^

Odpowiednie pliki wykonawcze znajdziesz na stronach producentów:

-  `ffmpeg <http://ffmpeg.org/download.html>`__
-  `x264 <https://artifacts.videolan.org/x264/release-win64/x264-r3101-b093bbe.exe>`__

Linux
~~~~~

Na linuxie znajdziesz odpowiednie paczki na repozytorium twojej
dystrybucji, np.

Ubuntu
^^^^^^

-  `ffmpeg <https://aur.archlinux.org/packages/ffmpeg-full>`__
-  `x264 <https://packages.ubuntu.com/search?suite=default&section=all&arch=any&keywords=x264&searchon=names>`__

Arch
^^^^

-  `ffmpeg <https://packages.ubuntu.com/search?keywords=ffmpeg>`__
-  `x264 <https://aur.archlinux.org/packages/lib32-x264>`__

Powinieneś móc teraz uruchomić oba te narzędzia w konsoli za pomocą
komend:

.. code:: bash

   ffmpeg
   x264

Jeśli któraś z komend nie daje odpowiedzi, być może musisz dodać ścieżkę
instalacji do `zmiennej
PATH <https://www.java.com/pl/download/help/path_pl.html>`__.

Czcionki
--------

| Używaną przeze mnie listę czcionek możesz znaleźć na
  `mega <https://mega.nz/folder/o6BUTT6Q#v1bMX7YsiWt_Rg9TLi1WkA>`__ .
| W poszukiwaniu nowych czcionek najpraktyczniejsze są:

-  `1001 fonts <https://www.1001fonts.com/>`__
-  `dafont <https://www.dafont.com/>`__

--------------

Kainote: Podstawowe funkcje
---------------------------

Okno Kainote'a możemy podzielić na 3 segmenty:

1. Okno napisów
2. Podgląd wideo
3. Edycja linijki

|Kainote screen|

Edycja bierzącej linijki
~~~~~~~~~~~~~~~~~~~~~~~~

**UWAGA: Jeśli zaznaczysz wiele linijek jednocześnie zmiany dokonają się
we wszystkich zaznaczonych linijkach, jeśli zaczniesz zmieniać tekst
zostanie on ustawiony na identyczny w każdej linijce**

Na samej górze segmentu służącego do edycji bierzącej linii widać
spektogram, a także kontrolki od dźwięku, służy to do projektowania
karaoke.

|Kainote: Line Edit|

**Nad polem tekstowym** widać przyciski, są to pokolei:

-  Zmiana czcionki:
   Pozwala zmienić typ i rozmiar czcionki **tag jest wstawiany w mijescu
   kursora, uważaj żeby nie zmienić tylko połowy linijki**
-  Pogrubienie:
   Wstawia tag ``{\b1}{\b0}`` wokół zaznaczonego tekstu
-  Kursywa:
   Wstawia tag ``{\i1}{\i0}`` wokół zaznaczonego tekstu
-  Podkreślenie:
   Wstawia tag ``{\u1}{\u0}`` wokół zaznaczonego tekstu
-  Przekreś;enie:
   Wstawia tag ``{\s1}{\s0}`` wokół zaznaczonego tekstu
-  Cztery przyciski od konfiguracji kolorystyczne, wszystkie wstawiają
   tag od\ ``{\1c}`` do ``{4c}``

   -  Kolor pierwszy: Kolor tekstu głównego
   -  Kolor drugi: Alternatywny kolor karaoke
   -  Kolor trzeci: Kolor obwódki
   -  Kolor czwarty: Kolor cienia

-  Customowe przyciski:
   Na końcu możesz dodać dowolną liczbę customowych przycisków z tagami,
   które uprzyjemnią ci pracę

**Pod polem edycji linjki** znajduje się parę przydatnych parametrów,
ktore odpowiadają za podstawowe zachowania tekstu, są to od lewej:

-  Checkbox określający, czy dane pole jest komentarzem, taką linijkę
   Kainote podświetli na niebiesko, a jej zawartość będzie niewidoczna
   na odcinku
-  Numer warstwy, domyślnie 0, im wyższa wartość tym wyżej ta linijka
   będzie w hierarchi (tzn. linijka na warstwie 1 wyświetli się nad
   linijką na warstwie 0)
-  Dwa pola oznaczające klatkę lub czas (zależnie od wybranego trybu,
   tryb można zmienić za pomocą checkboxa nad edytorem) rozpoczęcia i
   zakończenia linijki
-  Czas trwania linijki
-  Styl zaaplikowany do bieżącej linijki, można go zmienić wybierając
   inny z listy, która otworzy się po kliknięciu w nazwę
-  Przycisk otwierający okno edycji aktualnie wybranego stylu
-  Nazwę postaci mówiącej daną linijkę, to pole często będzie
   nieuzupełnione
-  Trzy wartości marginesów: lewy, prawy i pionowy
-  Pole efektów VSFiltra

Style
-----

Style pozwalają na predefiniowanie wyglądu linijek, które można
aplikować do wielu linijek jednocześnie, bez potrzeby użycia tagów. Jest
to wygodne, jeśli aplikujemy dany styl do tekstu, trochę mniej
praktyczne jeśli chodzi o zastosowanie do pojedynczego znaku.

| Menu styli możesz znaleźć na pasku bocznym pod ikonką: |Kainote Icon:
  style.png|, po jej kliknięciu powinno otworzyć się okno:
| |Kainote Module: Style|

Menedżer stylów podzielony jest na dwie części:

-  Po pierwsze katalogi, możesz ich utowrzyć dowolną ilość, style
   przechowywane we wszystkich katalogach są dostępne za każdym razem,
   gdy otworzysz program
-  Po drugie style pliku, są to style, które znajdują się w aktualnie
   otwartym pliku i mogą zostać wykorzystane w pracy z nim

Pomiędzy nimi znajdują się trzy przyciski, służą one do przemieszczania
Styli między katalogiem a plikiem. Po kliknięciu edytuj na dowolnej z
czcionek powinno pokazać się dodatkowy panel:

|Kainote Module: Style Edit|

Jeśli chodzi o dostępne tu pola w większości ich funkcja jest jasna, nie
będę jej więc tu omawiał, zwrócę uwagę tylko na kilka z nich:

-  Kolor "Drugi" to kolor alternatywny dla efektów karaoke
-  Pod każdym z kolorów znajduje się parametr przezroczystości,
   przyjmuje wartości od 0 - brak przezroczystości do 255 - pełna
   przezroczystość
-  Pole odstępy oznacza odstęp między kolejnymi znakami, może przyjmować
   również wartości ujemne
-  Prost. obw. spowoduje, że zamiast obramowania wokół tekstu rysowany
   będzie prostokąt o stałej wysokości
-  Położenie tekstu ustali domyślną pozycję linijek o tym stylu na
   ekranie, dokładnie tak jak pokazuje siatka - ``1`` oznaczać będzie
   lewy dolny róg, ``5`` środek, ``9`` prawy górny róg, itd.

--------------

Podstawowe tagi ASS
-------------------

W poszukiwaniu dodatkowych informacji sprawdź `dokumentację <https://aegi.vmoe.info/docs/3.1/ASS_Tags/>`__
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Pliki \*.ass w swojej strukturze przypominają języki znaczników, każda
informacja o zmianie względem aktualnego stylu w tekście umieszczana
jest w klamrach ``{}`` przed fragmentem tekstu, który chcesz zmienić.

Kolory i przezroczystość
------------------------

Czcionka:
~~~~~~~~~

Do zmiany parametrów czcionki służy kilka tagów:

-  ``{\fn<str>}`` zmienia nazwę czcionki na podaną, np.
   ``{\fnArial Black}``

-  ``{\fs<float>}`` zmienia rozmiar czcionki na podany w parametrze, np.
   ``{\fs90}``
-  ``{\fcsx<float>\fscy<float>}`` zmieniają skalę (wartość procentowa}
   czcionki odpowiednio w osi x i y, np. {\fscx75\fscy75}
-  ``{\fsp<float>}`` zmienia odstęp między znakami, może przyjmować
   wartości ujemne, np. ``{\fsp-15}`` \`

Obramówka:
~~~~~~~~~~

| ``{\board<float>}`` nastawia grubość ramki wokół tekstu (kolor
  czarny), lub ``{\xbord<float>\ybord<float>}`` nastawia obramówkę
  niezależżnie w obu kierunkach.
| |Tekst ramka|

Cień:
~~~~~

``{\shad<float>}`` nastawia odległość cienia rzucanego przez tekst, lub
``{\xshad<float>\yshad<float>}`` robi to samo, niezależnie w obu
kierunkach.

Rozmycie
~~~~~~~~

Rozmycie jest efektem, który działa tylko na jedną warstwę tekstu, tzn.:

-  Jeśli tekst nie ma obramówki rozmyje tekst
-  Jeśli w tekście znajduje się obramówka rozmyta zostanie tylko i
   wyłącznie ona Pozwala to na tworzenie ciekawych efektów, jednak warto
   jest mieć to z tyłu głowy projektując znaki.
   Efekt rozmycia posiada dwa algorytmy
-  ``{\blur<float>}`` Algorytm barzdiej wymagający, jednak efekty
   wygenerowane za jego pomocą wyglądają lepiej
-  ``{\be<int>}`` Algorytm słabszy, wygląda gorzej przy wysokich
   wartościach, przyjmuje jako parametr jedynie liczby całkowite Przy
   tworzeniu znaków warto nałożyć nawet słaby efekt, np. ``{\blur1}``,
   dzięki temu znak będzie lepiej wtapiał się w nagranie

Pozycja wyjściowa
~~~~~~~~~~~~~~~~~

| Pozycja wyjściowa odpowiada on za dpmyślną pozycję znaku i jego
  zawijanie (jeśli zajmuje on kilka linijek). Parametr można ustawić za
  pomocą tagu ``{\an<1-9>}``, gdzie liczba będzie oznaczała pozycję.
  Wartości te ustawiają się tak jak liczby na numpadzie, a więc ``1``
  oznaczać będzie lewy dolny róg, ``5`` środek, ``9`` prawy górny róg,
  itd.
| |numpad|

--------------

Edycja pozycji i obrotów
------------------------

Większość efektów dot. pozycji, będzie nakładach z poziomu podglądu
wideo, pozwala on nam na przemieszczanie, obracanie, etc. znaku na
nagraniu w czasie rzeczywistym (i nie wymaga bawienia się wartościami
ręcznie)

|Kainote Module: Video|

Najważniejsze służące do tego kontrolki znajdują się bezpośrednio pod
odtwarzaczem, od lewej:

Przesuwanie tekstu
~~~~~~~~~~~~~~~~~~

Służy do przesuwania tekstu na obrazie, wpływa jedynie na znacznik
pozycji ``{\pos(<x>,<y>)}``, jeśli wcześniej linijka zawierała znacznik
ruchu ``{\move()}`` zostanie on zastąpiony, znacznik zostanie wstawiony
na początku linijki

Ruch
~~~~

Więcej na ten temat w sekcji **Proste animacje**

Skalowanie
~~~~~~~~~~

Pozwala na skalowanie napisów (``{\fscx<float>\fscy<float>}``), znacznik
zostanie wstawiony na początku linijki

Obrót w osi Z
~~~~~~~~~~~~~

| Obrót w osi Z jest obrotem w płaszczyźnie ekranu ``{\frz<float>}``,
  może przyjmować zarówno wartości dodatnie jak i ujemne.
| |rotation Z example|
| Dodatkowo w trybie tym możemy edytować tzw. ``origin``, jest on
  oznaczony przez czerwony krzyżyk widoczny na środku zrzutu ekranu.
  Przeciągnięcie go spowoduje zmianę punktu, wokół którego dokonywany
  jest obrót.
| **UWAGA: Przesunięcie origina będzie, często w sposób nieprzewidywalny
  wpływać na napisy w ruchu**

Obrót w osiach X i Y
~~~~~~~~~~~~~~~~~~~~

| Ta funkcja pozwala nam na obrócenie tekstu w dwóch pozostałych
  płaszczyznach, dzięki czemu otrzymamy efekt pochylenia, widoczna
  siatka jest poglądem płaszczyzny, na której aktualnie znajduje się
  tekst. Zmiany w osi X dokonuje się przytrzymaniem PPM, zmiany w osi Y
  przytrzymaniem LPM.
| W tym trybie również można znaleźć origin, oznaczony czerwonym
  krzyżykiem.
| |rotation X Y example|

Clipy
-----

Następne dwa narzędzia to clipy, pierwsze z nich prostokątne, drugie
wektorowe, obydwa generują tag ``{\clip(<shape>)}``. Po stworzeniu clipa
widoczny będzie tylko tekst wewnątrz zaznaczonego kształtu |clip
example|

Efekt clipa można też odwrócić dodając przed tagiem ``i``:
``{\iclip(<shape>)}``, w ten sposób będzie widać jedynie tekst, który
nie znajduje się w zarysowanym kształcie.

Rysowanie
---------

Rysowanie pozwala na stworzenie rysunku wektorowego, zostanie on
wstawiony zamiast tekstu w danej linijce i przejmie wszystkie jego
efekty, tj. kolor, obramówkę, obrót itd., rysunek również może być
przycięty clipem |shape example|

| Dodatkowo po wybraniu narzędzia rysowania pojawią się nowe opcje
| |shape options|
| Mamy tu:

-  Narzędzie do przesuwania punktów (chociaż dowolny punkt możesz złapać
   i przesunąć w każdej chwilii innymi narzędziami)
-  Narzędzie rysowania linii
-  Narzędzie rysowania krzywych Beziera
   Pozwala na narysowanie dokładnych krzywych, zaznaczasz punkt
   początkowy i końcowy krzywej, a następnie dwoma dodatkowymi okrągłymi
   punkcikami regulujesz krzywiznę
   |bezier curve example|
-  Narzędzie rysowania krzywych B-sklejanyych
   Działa na podobnej zasadzie co krzywa Beizera, z tym wyjątkiem, że
   pozwala na stworzenie większej ilości punktów
-  Tworzenie punktów niezależnych od aktualnego kształtu
-  Usuwanie punktów

Zmieniacz pozycji
~~~~~~~~~~~~~~~~~

| Zmieniacz pozycji jest nieco bardziej zaawansowaną wersją narzędzia
  przesuwania, po prawej stronie znajdziesz nowe opcje: pozwolą ci one
  wybrać jakie elementy linijki chcesz przesuwać, możesz wybrać wiele na
  raz.
| Narzędzie to jest wygodne przy edycji bardziej zaawansowanych znaków,
  ponieważ pozwala przesuwać takie elementy jak clipy, czy punkty
  początkowe i/lub końcowe ruchu, na co nie pozwala standardowe
  narzędzie.

--------------

Kainote: Automatyzacja
----------------------

Kainote ma preinstalowanych parę użytecznych skryptów do autoamtyzacji,
znajdziesz je pod rozwijanym menu na pasku.

Aegisub Motion
~~~~~~~~~~~~~~

Ten skrypt służy do generowania zaawansowanych animacji, więcej na ten
temat w sekcji **Zaawansowane animacje**

Gradient Everything
~~~~~~~~~~~~~~~~~~~

| Żeby wygenerować gradient należy stworzyć dwie kopie tej samej
  linijki: pierwszą z kolorem początku gradiientu (górnym, albo lewym),
  drugą z kolorem końcowym (dolnym, albo prawym).
| Na przykład:

   ::

      Dialogue: 0,0:04:33.54,0:04:35.50,On Top,,0,0,0,,{\pos(1018.812,841.206)\blur1\3c&H000000&> \fs105\bord5\shad5\fnCabold Comic\1c&H790091&}| Twice
      Dialogue: 0,0:04:33.54,0:04:35.50,On Top,,0,0,0,,{\pos(1018.812,841.206)\blur1\3c&H000000&\fs105\bord5\shad5\fnCabold Comic\1c&H56083E&}| Twice

| Opcjonalnie, możesz stworzyć prostokątny clip wokół jednej z linijek,
  wtedy gradient zostanie wygenerowany jedynie wewnątrz clipu, w
  przeciwnym wypadku ramka zostanie wygenerowana automatycznie przez
  skrypt.
| Z menu wybierz
  ``Automatyzacja>Gradient Everything>Gradient Everything/Gradient Everything``,
  pojawi się nowe okno: |Gradient Everything|
| W oknie możesz wybrać tagi, które zostaną poddane efektowi gradientu,
  parametr Obok parametru ``pixels per strip`` jest kierunek, w którym
  poruszać będzie się gradient.
| Parametr ``Acceleration`` zmienia sposób w jaki wygenerowany zostanie
  gradient:

-  > 1 zaczyna się szybko, kończy powoli
-  < 1 zaczyna się powoli, kończy szybko

Na samym dole okna dialogowego możesz też znaleźć opcję zapisania sobie
przygotowanego gradientu do wielokrotnego użycia.

Efekt wygenerowania gradientu na kolorze z powyższych linijek wygląda
tak: |Gradient example|

Colorize
~~~~~~~~

[Jeszcze zrobię to jutro]

Recalculateor
~~~~~~~~~~~~~

Recalculator jest prostym sposobem na zmodyfikowanie pojedynczego tagu w
wielu linijkach na raz |Recalculator example|

| Zmodyfikuj jeden z dwóch głownych parametrów - zmianę procentową, albo
  zmianę o wartość, wybierz tagi, które chcesz zmienić.
| W przedostatniej linijce znajdują się modyfikatory, możesz dzięki temu
  zmieniać wartość o więcej z każdą kolejną linijką, np.
  ``15>30>45>60>75`` etc.
| Jak widać główne dwie funkcje, z których będziesz korzystać to
  mnożenie/dodawanie, jeśli chciałbyś odjąć wystarczy ustawaić ujemną
  wartość w polu tekstowym

.. _perspectivepy:

Perspective.py
~~~~~~~~~~~~~~

| Source: `Script by Zeght on
  Github <https://github.com/TypesettingTools/Perspective/blob/master/perspective.py>`__
  **UWAGA: Perspektywa wygenerowana w ten sposób zawiera tag
  ``{\org()}`` z tego powodu nie będzie działała w ruchu.**
| Jest to narzędzie CLI napisane w pythonie, służące do wygenerowania
  tagów rotacji i origin, które będą odpowiadać rotacji obiektu na
  ekranie, sposób wygenerowania jest prosty:

1. Za pomocą narzędzia clipu wektorowego narysuj obrys czegoś, co w
   przeszłości było prostokątem od lewego górnego rogu, zgodnie z ruchem
   wskazówek zegara |Perspective.pt step 1|
2. Przeklej zawartość tagu ``{\clip()}`` do konsoli razem z komendą, np.
   .. code:: ps

      python3 perspective.py "m 845 78 l 1233 164 1213 218 825 131"

3. Konsola odpowie kilkoma możliwymi perspektywami, wybierz najlepszą i
   przeklej na początek linijki, gotowe!
   .. code:: ps

      Transforms near center of tetragon:                                                                                     Ratio=6.766732                                                                                                          \org(563.6, 3133.9)\fry-0.63\frx0.51\frz-19.96                                                                                                                                                                                                  Transforms with target ratio:                                                                                           Ratio=7.015400                                                                                                          \org(1373.4, 3139.9)\fry-0.61\frx0.50\frz-19.32

--------------

Proste animacje
---------------

Do prowadzenia prostych animacji przyda ci się różnica między bierzącą
klatką, a czasami rozpoczęcia i zakończenia linijki, możesz je znaleźć
obok kontrolek odtwarzacza, razem z aktualną minutą i aktualnym numerem
klatki.

|Timestamps|

Fade
~~~~

| Fade jest prostym efektem wejścia/wyjścia, jego podstawowa forma
  wygląda tak ``{\fade(<int>,<int>)}``, gdzie pierwszy parametr jest
  wyrażonym w milisekundach czasem przez który linijka będzie się
  pojawiać (od alphy 255 do 0), a drugi to czas w milisekundach, przez
  który linijka będzie znikać (od 0, do 255).
| Druga forma taga pozwala na pełną kontrolę nad czasami w jakich
  wykonuje się efekt, a także nad stopniami przezroczystości:
| ``\fade(<a1>,<a2>,<a3>,<t1>,<t2>,<t3>,<t4>)``, gdzie:

-  tekst ma przezroczystość ``a1`` aż do momentu ``t1``
-  między ``t1`` a ``t2`` przezroczystość przechodzi z ``a1`` do ``a2``
-  między ``t2`` a ``t3`` przezroczystość ma stałą wartość ``a2``
-  między ``t3`` a ``t4`` przezroczystość przechodzi z ``a2`` do ``a3``
-  po momencie ``t4`` tekst ma przezroczystość ``a3``

.. _ruch-1:

Ruch
~~~~

W Kainote wbudowane jest narzędzie ruchu, jest to pozycja którą
pominęliśmy wcześniej przy edytorze wideo: |movement example|

-  Kwadrat oznacza pozycję początkową
-  Kółko oznacza pozycję końcową tekstu
-  krzyżyk oznacza pozycję w danej klatce

Po zaczęciu rysowania ruchu Kainote wstawi do twojego znaku tag
``{\move(<x1>,<y1>,<x2>,<y2>,<t1>,<t2>)}``, często nie będziesz chcieć,
aby animacja trwała całą linijkę, parametry ``<t1>`` i ``<t2>``
odpowiadają czasom rozpoczęcia i zakończenia ruchu.

Transformacje
~~~~~~~~~~~~~

| Ponad dwa przedstawione powyżej specjalne przypadki, często zdarzy
  się, że będziesz chciał edytować rozmycie, rozmiar czcionki, kolor,
  czy inny z wielu dostępnych parametrów. Można to zrobić w prosty
  sposób z użyciem tagu transformacji: ``{\t(<t1>,<t2>,<tag>)}``.
| Ten tag pozwala na utowrzenie prostych przejść między stanami tagów,
  weźmie on stan tagu sprzed momentu ``<t1>``, a następnie między
  ``<t1>`` a ``<t2>`` wygeneruje dynamiczne przejście do stanu
  ``<tag>``, np. |Transform example|

   Sekwencja tagów ``{\blur10\t(0,147,\blur0)}``

--------------

Zaawansowane animacje
---------------------

Do tego segmentu przydadzą ci się dodatkowo: `Wideo do Odcinka 1
Kaguya-Sama Love is War: Ultra Romantic
(nyaa.si) <https://nyaa.si/view/1511966>`__

Większość zaawansowanych animacji, które wykonujemy w typesettingu
(wyjątek: efekty karaoke) opiera się o nieregularne zmiany pozycji,
rotacji, obrazu, czy perspektywy. Są to po prostu efekty, które ręcznie
jest ciężko wykonać, lub wymagałoby to poświęcenia nadmiernej ilości
czasu np.:

|Kaguya-sama Love is War: Ultra Romantic E03 Klatki 11665-11766|

   Kaguya-Sama, S03E01, znak mówi ``Co porabisz?``

Wykonanie podstawy znaku
~~~~~~~~~~~~~~~~~~~~~~~~

Na samym początku musimy wykonać znak dla jednej z klatek - tak, by było
potem co wprawić w ruch. W nowych wersjach Aegisub-Motion nie ma
znaczenia, która klatka to będzie, jednak dobrze jest by była to
pierwsza lub ostatnia, w ten sposób nie powinno być problemu z
przypadkowym przesunięciem znaku w późniejszych etapach. Pamiętaj też,
aby sprawdzić timing, najlepiej w trybie podglądu klatek (przełącznik
znajdziesz nad polem edycji linijki), pierwsza i ostatnia klatka powinny
pokrywać się z pierwszą i ostatnią klatką obecności znaku na ekranie,
**a nie kaltkę przed/po**. Nasz znak może wyglądać np. tak:

|Znak ruchomy Mocha, Step 1|

Konfiguracja Aegisub-Motion
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Jeśli robisz to po raz pierwszy prawdopodobnie będziesz musiał
skonfigurować od nowa Aegisub-Motion:

1. Znajdź ścieżkę, w której znajduje się twój plik ``x264.exe``, u mnie
   jest to: ``F:\Kainote\Redist\x264-r3098-7628a56.exe``
2. Otwórz okno konfiguracyjne Aegisub-Motion, w najnowszej wersji
   skryptu jest ono dostępne na pasku:
   ``Automatyzacja > Aegisub-Motion > Aegisub-Motion/Trim Settings``.
   Powinieneś widzieć coś takeigo:
   |Kainote: Aegisub-Motion Settings Module|
3. W podświetlonej linijce wklej ścieżkę do ``x264.exe`` i kliknij
   ``Save``. Nie zmieniaj nic innego!

Wyciągnięcie wideo danej linijki
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Następnym krokiem będzie wyciągnięcie wideo, które następnie
zaimportujemy do Mochy. Zrobienie tego jest proste, dzięki narzędziom
automatyzacji wystarczy parę kliknięć na pasku:
``Automatyzacja > Aegisub-Motion > Aegisub-Motion/Trim``, otworzy ci się
konsolka i wideo przytnie się samo. Po zakończeniu działania skryptu
przycięty fragment powinieneś znaleźć w tym samym miejscu co oryginalne
wideo.

Stworzenie nowego projektu w Boris FX Mocha
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| Następnie przeniesiemy się do Mochy, po otwarciu programu z paska
  wybierz: ``File > New Project``
| Otworzy się nowe okno:
| |Boris FX Mocha Pro: New Project Module|
| Klikamy ``Choose...`` i wybieramy przycięty przed chwilą fragment,
  pozostałe parametry Mocha zaczyta samoczynnie

Boris FX Mocha: Podstawy
~~~~~~~~~~~~~~~~~~~~~~~~

Przed sobą powinieneś mieć teraz coś takiego: |Boris FX Mocha Pro|

Kontrolki, które widzisz u samej góry służą do głównie do rysowania
obszarów śledzenia, mamy więc tu od prawej:

|Boris FX Mocha Pro Controls|

1.  Szybki zapis
2.  Wskaźnik
3.  Narzędzie to pozwala na dodanie punktu na już skończonym obszarze w
    miejscu myszki
4.  Przesuwanie widoku
5.  Lupa
6.  Narzędzie rysowania prostych
7.  Narzędzie magnetyczne - będzie rysowało obszar śledzenia od punktu
    do punktu po krawędziach obrazu, podobnie do "różdżki" z
    photoshopa/GIMPa
8.  Tworzy zaznaczenie na podstawie zamalowanego obszaru
9.  Rysuje obszar w kształcie prostokąta
10. Rysuje obszar w kształcie okręgu/elipsy
11. Następne 3 służą do bardziej zaawansowanych operacji, będą nam
    zbędne
12. Lista dostępnych konfiguracji widoku, zazwyczaj są one nieprzydatne,
    jednak zdażają się znaki zachowujące się na tyle dziwnie, że będzie
    potrzebny np. classic, umożliwia on możliwosć śledzenia siatki.

|Boris FX Mocha Pro: Layers Module|

| W tym segmencie znajdują się kontrolki od śledzenia.
| W pustym polu u góry będą pojawiać się rysowane do śledzenia kształty.
| Pięć przycisków poniżej służy do ograniczeniu możliwości śledzenia -
  zazwyczaj chcemy śledzić ruch jedynie w tych parametrach, w których
  potrzeba, inaczej może dojść do błędów.
| Poniżej mamy kontrolki od uruchamiania śledzenia - do tyłu, stop i w
  przód.
| Na samym dole znajdują się dwa przyciski, pierwszy z nich posłuży
  przeniesieniu danych do napisów.

|Boris FX Mocha Pro: Player Module|

| Ostatnim segmentem jest sam odtwarzacz, nie ma tu nic specjalnego -
  pod odtwarzaczem widać oś czasu z podziałem na klatki, a pod nią
  kotrolki do odtwarzania.
| Tym co nas będzie najbardziej tu interesowało to klatki kluczowe:
  Niebieski pasek na osi czasu oznacza klatkę, w której aktualnie
  znajduje się wideo, jeśli zaczniemy rysować obszar śledzenia ta klatka
  zostanie oznaczona na zielono:
| |KeyFrame|
| Klatki kluczowe pozostaną niezmienione w trakcie śledzenia, a punkty w
  pozostałch klatkach będą dążyć do pozycji zaznaczonych w klatkach
  kluczowych.

Śledzenie ruchu
~~~~~~~~~~~~~~~

Narysujmy teraz obwódkę wokół znkau, który zamierzamy śledzić, np. tak:

|Boris FX Mocha Pro: Tracking KeyFrame 1|

I po lewej stronie uruchommy tracking (wcześniej upewnij się, że
zaznaczone są jedynie potrzebne ci parametry, w tym wypadku: ruch).

|Boris FX Mocha Pro: Tracking Animation|

Jeśli twoim zdaniem wyśledzony ruch wygląda dobrze, możesz przejsć do
następnego kroku, w przeciwnym razie poeksperymentuj z zaznaczeniem:
czasami dobrze jest złapać inny znak, niż ten który faktycznie chcemy
wyśledzić, albo złapać tylko jego część, na przykład pojedyncze kanji.

Import do Kainote
-----------------

Aby wyeksportować przygotowany przez Mochę ruch wciskamy wcześniej
wspomniany przeze mnie przycisk na samym dole panelu z kontorlkami do
śledzenia ``Export Tracking Data`` jest napisane na przycisku (jeśli
jest on nieaktywny sprawdź, czy na pewno masz wybraną którąś z warstw).
Po jego wciśnięciu wyskakuje nowe okno: |Boris FX Mocha Pro: Export
Tracking Data Dialogue|

| Interesujący nas format jest tym samym, który otwiera się domyślnie:
| ``After Effects Transform Data [position, scale and rotation] (*.txt)``
| Wystarczy nam skopiować go do schowka, nie potrzebujemy mieć tego
  nigdzie zachowanego.

| Następnie w Kainote zaznaczamy linijkę, bądź linijki, do których
  chcemy zaaplikować nasz efekt.
| **UWAGA: Przypilnuje, żeby mieć tę samą klatkę, co przy tworzeniu
  znaku, w przeciwnym razie cały znak się rozjedzie!** I z menu
  automatyzacji tym razem wybieramy Aegisub-Motion/Apply:
| ``Automatyzacja > Aegisub-Motion > Aegisub-Motion/Apply``
| Pojawi się nowe okienko:
| |Kainote Automation: Aegisub-Motion/Apply|

W polu tekstowym automatycznie wklejony zostanie wzorzec ruchu, który
przed chwilą skopiowaliśmy z Mochy. W checkboxach możemy też wybrać do
jakich parametrów zostaną zaaplikowane zmiany:

-  Współrzędne x, y całości znaku, zaznaczenie ``Absolute`` spowoduje,
   że wartości nie zostaną przeliczone, a jedynie przepisane z
   wklejonych danych
-  Współrzędne punktu origin
-  Skala znaku (tylko jeśli taką wcześniej wyśledziliśmy)
-  Skala obramówki (tylko jeśli wybraliśmy wcześniej Skalę)
-  Skala cienia (tylko jeśli wybraliśmy wcześniej Skalę)
-  Skala rozmycia (tylko jeśli wybraliśmy wcześniej Skalę), zadziała
   tylko na rozmycie wygenerowane tagiem ``{\blur}``
-  Rotacja znaku (tylko jeśli taką wcześniej wyśledziliśmy)
-  Clip prostokątny/wektorowy, a także do prawej strony jest możliwość
   konwersji clipów prostokątnych na wektorowe

Dalej są już tylko modyfikatory:

-  ``Interpolate transforms`` - skrypt podejmie próbę przekalkulowania
   transformacji, w przeciwnym razie pozmienia tylko ich czasy
-  ``Write config`` - zapamięta aktualne ustawienia na później
-  ``Relative`` - wybierze klatkę początkową na podstawie aktualnej
   klatki wideo
-  ``Clip Only`` - zaaplikuje zmiany tylko do clipa
-  ``Linear`` - zamiast generować animację klatka po klatce, skrypt
   wygeneruje animację z pomocą tagów ``{\move()}`` i ``{\t()}``,
   pozwoli to zaoszczędzić linijek, jednak nie zawsze jest równie
   skuteczne co standardowa metoda.

Po ustawieniu wszystkich parametrów wystarczy kliknąć ``Go`` i pozwolić
skryptowi działać. Po skończonej pracy w naszym pliku pojawią się nowe
linijki, a stara zostanie wykomentowana, nie będę tu przeklejał
przykładowego efektu, ale na wideo powinno wyglądać to tak:

|Znak Ruchomy, Mocha, Wersja Finalna|

Jeśli twój znak "podskakuje" w dziwny sposób jest szansa, że klatki
przygotowane przez Mochę nie pokryły się z klatkami w wideo, zazwyczaj
wystarczy zmienić przy tworzeniu projektu wartość klatek z 23.9 na 24 i
wyśledzić ruch raz jeszcze, a problem rozwiązuje się sam.

--------------

Parę słów na koniec
-------------------

Niezależnie od techinicznej strony wykonania znaku najważniejsza w tym
wszystkim jest strona estetyczna. [Będę tu posługiwał się swoimi
przykładami jak i tymi podsuniętymi przez poradnik Commie Subs] Dobry
znak przede wszystkim nie powinien być inwazyjny na nagraniu, powinien
wyglądać tak jakby był jednolitą częścią odcinka, najwięcej zależy od
doboru odpowiedniej czionki, kolorystyki, warto też używać rozmycia,
dzięki temu znak nie będzie taki "ostry" i będzie lepiej wtapiał się w
odcinek.

|Taishou Otome Otogibanashi: odc 2 List do Tamahiko|

   Taishou Otome Otogibanashi 02; Tłumaczenie: ShinoAlter; Korekta:
   Gruzin; Dla: Shine Subs

|CommieSubs guide screen 01|

   Wykonało: Commie Subs

Pamiętajcie, też że nie każdy dobry znak zakrywa swój oryginał, czasami
lepiej jest zapisać swoją zawartość w innym miejscu na ekranie, a w
przypadku podpisów często stworzyć miejsce, którego w oryginale mogło
nie być

|Taishou Otome Otogibanashi: odc 1 Sylwester|

   Taishou Otome Otogibanashi 01; Tłumaczenie: ShinoAlter; Korekta:
   Gruzin; Dla: Shine Subs

|Taishou Otome Otogibanashi: Podpis|

   Taishou Otome Otogibanashi 01; Tłumaczenie: ShinoAlter; Korekta:
   Gruzin; Dla: Shine Subs

|Louise of the Holy Land: Tytuł|

   Louise of the Holy Land; Dla: Commie Subs

Ten podoba mi się w szczególności, ze względu na swoją nieoczywistość,
napis początkowo należał do różowych znaków, na który typsetterowi
brakło miejsca. Czasem warto pokombinować. |CommieSubs guide screen 02|

| Ostatnia porada, pamiętajcie, że warstwy w szczególności mogą mieć
  ciekawe zastosowania - czasami nie warto przekombinowywać, dodatkowe
  warstwy mogą się rozjeżdżać przy skalowaniu, czy ruchu, czasami po
  prostu nie mamy czasu, ale... szczególnie na statycznych napisach
  nawet jedna dodatkowa warstwa potrafi zrobić kolosalną różnicę, warto
  też tak rozdzielać obramówki od głównej części napisów - pozwoli to na
  rozmazanie krawędzi w obu częściach.
| |CommieSubs guide screen 03.1| |CommieSubs guide screen 03.2|

   Wykonało: Commie Subs

--------------

Popróbuj na tych plikach:
-------------------------

.. _kaguya-odc-1:

Kaguya odc. 1
~~~~~~~~~~~~~

| Tłumaczenie angielskie wykonane przez: **SubsPlease**
| `Napisy do
  odcinka <https://raw.githubusercontent.com/ModerNews/GruzinSubs/master/%5BSubsPlease%5D%20Kaguya-sama%20wa%20Kokurasetai%20S3%20-%2001%20(1080p)%20%5B9816946B%5D.ass?token=GHSAT0AAAAAABZBR35LEAAI4NTC64QTYNOWY36RQ6Q>`__
| `Link do odcinka na nyaa.si <https://nyaa.si/view/1511966>`__

.. _citrus-odc-3:

Citrus odc. 3
~~~~~~~~~~~~~

| Tłumaczenie: **Kraksa**, Korekta: **Nowek**, dla: **MaouSubs**
| `Napisy do
  odcinka <https://raw.githubusercontent.com/ModerNews/GruzinSubs/master/Kraksa_Citrus_03(3).ass?token=GHSAT0AAAAAABZBR35LHT4VSBFE5HURXZBIY36RRFQ>`__
| `Link do odcinka na nyaa.si <https://nyaa.si/view/1403136>`__

References
----------

-  `Old typestting guide by
   commiesubs <https://yukisubs.files.wordpress.com/2016/10/commie_typesetting_in_aegisub.pdf>`__
-  `ASS format
   documentation <https://aegi.vmoe.info/docs/3.1/ASS_Tags/>`__

.. |Kainote screen| image:: https://media.discordapp.net/attachments/783791354374783016/1043316597122662440/image.png?width=1208&height=657
.. |Kainote: Line Edit| image:: https://user-images.githubusercontent.com/61905404/202861820-aa009402-0ade-4b15-9afa-66f022744105.png
.. |Kainote Icon: style.png| image:: https://raw.githubusercontent.com/bjakja/Kainote/master/Kainote/Bitmaps/Style.png
.. |Kainote Module: Style| image:: https://media.discordapp.net/attachments/783791354374783016/1043554131417247756/image.png?width=200&height=368
.. |Kainote Module: Style Edit| image:: https://media.discordapp.net/attachments/783791354374783016/1043556408827854878/image.png?width=402&height=368
.. |Tekst ramka| image:: https://media.discordapp.net/attachments/783791354374783016/1043588847344304138/image.png
.. |numpad| image:: https://user-images.githubusercontent.com/61905404/202856961-faab6198-1696-427f-85cd-3ab2e919fa00.png
.. |Kainote Module: Video| image:: https://user-images.githubusercontent.com/61905404/202861945-84d1fece-db6c-4244-9e12-eb12f4e36dc2.png
.. |rotation Z example| image:: https://user-images.githubusercontent.com/61905404/202862421-32c86265-0a9d-4226-b0da-54756a41f4b9.png
.. |rotation X Y example| image:: https://user-images.githubusercontent.com/61905404/202862624-8e0c3307-1ad2-4f52-82ca-a128d1d26c8e.png
.. |clip example| image:: https://media.discordapp.net/attachments/783791354374783016/1043572977062645800/image.png
.. |shape example| image:: https://media.discordapp.net/attachments/783791354374783016/1043575246009147502/image.png
.. |shape options| image:: https://user-images.githubusercontent.com/61905404/202863282-db311b1c-1622-4e14-bf64-8ba4ba3bff11.png
.. |bezier curve example| image:: https://user-images.githubusercontent.com/61905404/202863452-a1e2eba4-b958-40fc-98b7-d64cd0643a6b.png
.. |Gradient Everything| image:: https://user-images.githubusercontent.com/61905404/202865975-acf4b641-3b6e-45cd-8bb4-d9ea19c52874.png
.. |Gradient example| image:: https://user-images.githubusercontent.com/61905404/202866234-2beb7536-2f10-4248-80d5-203028b576a0.png
.. |Recalculator example| image:: https://user-images.githubusercontent.com/61905404/202866326-8c5dddcf-d5c6-4468-9384-79002fd4cc2a.png
.. |Perspective.pt step 1| image:: https://user-images.githubusercontent.com/61905404/202866844-2de8e767-7aa6-40d6-b4dd-bf9a3b3102dd.png
.. |Timestamps| image:: https://user-images.githubusercontent.com/61905404/202864156-8a62dcfe-925b-4971-827c-59ce6521d2d7.png
.. |movement example| image:: https://media.discordapp.net/attachments/783791354374783016/1043579643162267728/image.png
.. |Transform example| image:: https://user-images.githubusercontent.com/61905404/202864700-ab93880d-212e-4640-a63b-a5d4917e5315.gif
.. |Kaguya-sama Love is War: Ultra Romantic E03 Klatki 11665-11766| image:: https://user-images.githubusercontent.com/61905404/203578018-8a49d46b-60d3-4548-8639-9148a85aadf4.gif
.. |Znak ruchomy Mocha, Step 1| image:: https://user-images.githubusercontent.com/61905404/203579191-1ea6161b-3146-4bc7-9ca3-a80a68918e58.png
.. |Kainote: Aegisub-Motion Settings Module| image:: https://user-images.githubusercontent.com/61905404/203584964-75793756-04df-4e3c-a2f3-edbd085bf353.png
.. |Boris FX Mocha Pro: New Project Module| image:: https://user-images.githubusercontent.com/61905404/203586396-b0073388-f1ab-49de-89b7-f878279af723.png
.. |Boris FX Mocha Pro| image:: https://user-images.githubusercontent.com/61905404/203587034-105ed9d7-2a68-491f-974e-de005cc26bec.png
.. |Boris FX Mocha Pro Controls| image:: https://user-images.githubusercontent.com/61905404/203587107-8377a071-f902-44b4-baea-63362e6cd5af.png
.. |Boris FX Mocha Pro: Layers Module| image:: https://media.discordapp.net/attachments/783791354374783016/1045011408787607682/image.png?width=215&height=676
.. |Boris FX Mocha Pro: Player Module| image:: https://user-images.githubusercontent.com/61905404/203587211-3d376600-b440-4f8c-9c88-bbb25d0976bb.png
.. |KeyFrame| image:: https://user-images.githubusercontent.com/61905404/203599258-92b7538b-78dd-4f03-91c7-33cbdc65658a.png
.. |Boris FX Mocha Pro: Tracking KeyFrame 1| image:: https://user-images.githubusercontent.com/61905404/203600062-b0d52307-a34b-42a4-b524-3aca598a8fbe.png
.. |Boris FX Mocha Pro: Tracking Animation| image:: https://media.discordapp.net/attachments/783791354374783016/1045016499368247306/Kguya_01_01.gif?width=1206&height=676
.. |Boris FX Mocha Pro: Export Tracking Data Dialogue| image:: https://media.discordapp.net/attachments/783791354374783016/1045017879222956092/image.png
.. |Kainote Automation: Aegisub-Motion/Apply| image:: https://media.discordapp.net/attachments/783791354374783016/1045019941469950146/image.png
.. |Znak Ruchomy, Mocha, Wersja Finalna| image:: https://media.discordapp.net/attachments/783791354374783016/1045024731511930880/Kguya_01_02.gif
.. |Taishou Otome Otogibanashi: odc 2 List do Tamahiko| image:: https://user-images.githubusercontent.com/61905404/203612781-d7a7a17d-370f-436e-b294-ed888eaabc92.png
.. |CommieSubs guide screen 01| image:: https://user-images.githubusercontent.com/61905404/203613093-0021b715-b493-482a-96c4-015fd0b36d97.png
.. |Taishou Otome Otogibanashi: odc 1 Sylwester| image:: https://user-images.githubusercontent.com/61905404/203611976-4cab68d6-b480-425e-bf9c-4f1d0daf6790.png
.. |Taishou Otome Otogibanashi: Podpis| image:: https://user-images.githubusercontent.com/61905404/203612652-b34520fd-d98c-4bfa-ade7-2bc6049ea54b.png
.. |Louise of the Holy Land: Tytuł| image:: https://user-images.githubusercontent.com/61905404/203613956-e92234c4-b81b-4d18-9a73-54fb72665dd5.png
.. |CommieSubs guide screen 02| image:: https://user-images.githubusercontent.com/61905404/203614369-9122b302-3ef4-490b-9ad5-9d907a7a5a7b.png
.. |CommieSubs guide screen 03.1| image:: https://user-images.githubusercontent.com/61905404/203615026-b6b56879-2c1b-40b9-ad49-364bd5123fa8.png
.. |CommieSubs guide screen 03.2| image:: https://user-images.githubusercontent.com/61905404/203615034-fad6f26a-73e9-4611-9f2e-405132c44995.png
