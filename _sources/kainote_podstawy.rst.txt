.. |Kainote screen| image:: https://media.discordapp.net/attachments/783791354374783016/1043316597122662440/image.png?width=1208&height=657
.. |Kainote: Line Edit| image:: https://user-images.githubusercontent.com/61905404/202861820-aa009402-0ade-4b15-9afa-66f022744105.png
.. |Kainote Icon: style.png| image:: https://raw.githubusercontent.com/bjakja/Kainote/master/Kainote/Bitmaps/Style.png
    :height: 16px
.. |Kainote Module: Style Edit| image:: https://media.discordapp.net/attachments/783791354374783016/1043556408827854878/image.png?width=402&height=368

===========================
Kainote: Podstawowe funkcje
===========================

Okno Kainote'a możemy podzielić na 3 segmenty:

1. Okno napisów
2. Podgląd wideo
3. Edycja linijki

|Kainote screen|

Edytor linijki
==============

.. warning:: 
    Jeśli zaznaczysz wiele linijek jednocześnie zmiany dokonają się we wszystkich zaznaczonych linijkach, jeśli zaczniesz zmieniać tekst zostanie on ustawiony na identyczny w każdej linijce

Na samej górze segmentu służącego do edycji bierzącej linii widać
spektogram, a także kontrolki od dźwięku, służy one do projektowania efektów karaoke, które opierają się na wielokrotnych zmianach stylu na przestrzeni jednej linijki.

|Kainote: Line Edit|

**Nad polem tekstowym** widać przyciski, są to pokolei:

-  Zmiana czcionki:
   Pozwala zmienić typ i rozmiar czcionki **tag jest wstawiany w mijescu
   kursora, pamiętaj o tym przy pracy**
-  Pogrubienie:
   Wstawia tag ``{\b1}{\b0}`` wokół zaznaczonego tekstu
-  Kursywa:
   Wstawia tag ``{\i1}{\i0}`` wokół zaznaczonego tekstu
-  Podkreślenie:
   Wstawia tag ``{\u1}{\u0}`` wokół zaznaczonego tekstu
-  Przekreś;enie:
   Wstawia tag ``{\s1}{\s0}`` wokół zaznaczonego tekstu
-  Cztery przyciski od konfiguracji kolorystyczne, wszystkie wstawiają
   tag od ``{\1c}`` do ``{\4c}``, omówię je zaraz dokładniej w :ref:`części Style <Style>`.
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

.. _Style:

Style
=====

.. hint::
    Style pozwalają na zwiększenie czytelności linijki, ograniczają obiętość nieczytelnego tekstu w linijce, zazwyczaj jednak nie warto projektować stylu dla pojedynczego znaku

Style pozwalają na predefiniowanie wyglądu linijek, które można
aplikować do wielu linijek jednocześnie, bez potrzeby użycia tagów. Jest
to wygodne, jeśli aplikujemy dany styl do tekstu, trochę mniej
praktyczne jeśli chodzi o zastosowanie do pojedynczego znaku.

Menu styli możesz znaleźć na pasku bocznym, po kliknięciu ikonki powinno otworzyć się okno:

.. image:: https://media.discordapp.net/attachments/783791354374783016/1043554131417247756/image.png?width=200&height=368
    :alt: Kainote Module: Style

Menedżer stylów podzielony jest na dwie części:

-  Po pierwsze katalogi, możesz ich utowrzyć dowolną ilość, style
   przechowywane w katalogach będą zawsze dostępne do skopiowania do aktualnego pliku  
-  Po drugie style pliku, są to style, które znajdują się w aktualnie
   otwartym pliku i mogą zostać wykorzystane w trakcie pracy

Pomiędzy nimi znajdują się trzy przyciski, służą one do przemieszczania
styli między katalogiem a plikiem. Po kliknięciu edytuj na dowolnej z
czcionek powinno pokazać się dodatkowy panel:

|Kainote Module: Style Edit|

| Po pierwsze przypilnujmy konfiguracji stylu domyślnego, zazwyczaj będzie on nazywał się :code:`Default` lub :code:`Main`.
| Zazwyczaj taki styl powinien być zaimportowany już wcześniej i nie powinno być potrzeby modyfikowania go.

Po drugie przyjrzymy się tworzeniu nowych styli i omówimy sobie dostępne pola:
- Nazwa powinna być raczej krótka, np. :code:`Default`, :code:`Signs`, :code:`OP`, :code:`ED`, tym bardziej że zazwyczaj nie powinno być ich potrzebnych wiele.

- Czcionka i jej rozmiar, temat instalowania dodatkowych czcionek został omówiony wcześniej, po doinstalowaniu czcionki powinna się ona pokazać od razu na liście, nie ma potrzeby ponownego uruchamiania programu. Dla standardowego tekstu rozmiar nie powinien przekraczać 100 

- Kolory:
   -  Kolor "Drugi" to kolor alternatywny dla efektów karaoke
   -  Pod każdym z kolorów znajduje się parametr przezroczystości,
      przyjmuje wartości od 0 - brak przezroczystości do 255 - pełna
      przezroczystość
   -  Pole odstępy oznacza odstęp między kolejnymi znakami, może przyjmować
      również wartości ujemne
   -  Prost. obw. spowoduje, że zamiast obramowania wokół tekstu rysowany
      będzie prostokąt o stałej wysokości
   
   Pod każdym kolorem znajduje się też odpowiadająca mu przezroczystość - ``0`` nieprzezroczysty, ``255`` - w pełni przezroczysty

- Następna ramka zawiera rozmiar obwódki, odległość cienia od tekstu (może być ujemna, cień będzie wtedy "padał" w stronę lewego górnego rogu), a także skalę w ``X`` i ``Y``, zazwyczaj używa się jednego z nich, żeby "zcieśnić" tekst

-  Położenie tekstu ustali domyślną pozycję linijek o tym stylu na
   ekranie, dokładnie tak jak pokazuje siatka - ``1`` oznaczać będzie
   lewy dolny róg, ``5`` środek, ``9`` prawy górny róg, itd.