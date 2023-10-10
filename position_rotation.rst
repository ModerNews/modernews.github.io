.. |numpad| image:: https://user-images.githubusercontent.com/61905404/202856961-faab6198-1696-427f-85cd-3ab2e919fa00.png
.. |rotation example| image:: https://media.discordapp.net/attachments/837426178439905280/1062355141497475193/rotation_prev.gif?ex=652e8553&is=651c1053&hm=80149a279b76c9c6bdb3d263a5e1dfffdad79e5cf1a51944d53596cdfc395617&=&width=1170&height=658

=========================
Pliki ASS: Pozycja i rotacja
=========================

Pozycja
=======

Jak było powiedziane na końcu poprzedniego rozdział każdy znak ma swoją pozycję wyjściową, zależną od wartości zdefiniowanej w stylu, lub tagu :code:`{\an<1-9}`, gdzie 1 - oznacza lewy dolny róg, a 9 - prawy górny.

|numpad|

Następnie możemy przesunąć tekst względem tego za pomocą tagu :code:`{\pos}`

Dodatkowo zamiast tagu :code:`{\pos}` można wprowadzić tag :code:`{\mov}`, który wprawi znak w ruch. Więcej na ten temat :ref:`tutaj <ruch_1>`.

Obrót w osi Z
=============

| Obrót w osi Z jest obrotem w płaszczyźnie ekranu, oznaczany tagiem :code:`{\frz<float>}`,
  może przyjmować zarówno wartości dodatnie jak i ujemne.

Obrót w osiach X i Y
====================

| Ta funkcja pozwala nam na obrócenie tekstu w dwóch pozostałych
  płaszczyznach, odpowiadają za to tagi :code:`{\frx<float>\fry<float>}`, dzięki tym osiom otrzymamy efekt pochylenia, widoczna
  siatka jest poglądem płaszczyzny, na której aktualnie znajduje się
  tekst. Zmiany w osi X dokonuje się przytrzymaniem PPM, zmiany w osi Y
  przytrzymaniem LPM.

|rotation example|
