.. |Timestamps| image:: https://user-images.githubusercontent.com/61905404/202864156-8a62dcfe-925b-4971-827c-59ce6521d2d7.png
.. |movement example| image:: https://media.discordapp.net/attachments/783791354374783016/1043579643162267728/image.png
.. |Transform example| image:: https://user-images.githubusercontent.com/61905404/202864700-ab93880d-212e-4640-a63b-a5d4917e5315.gif

===============
Proste animacje
===============

Do prowadzenia prostych animacji przyda ci się różnica między bierzącą
klatką, a czasami rozpoczęcia i zakończenia linijki, możesz je znaleźć
obok kontrolek odtwarzacza, razem z aktualną minutą i aktualnym numerem
klatki.

|Timestamps|

Fade
~~~~

| Fade jest prostym efektem wejścia/wyjścia, jego podstawowa forma
  wygląda tak :code:`{\fade(<int>,<int>)}`, gdzie pierwszy parametr jest
  wyrażonym w milisekundach czasem przez który linijka będzie się
  pojawiać (od alphy 255 do 0), a drugi to czas w milisekundach, przez
  który linijka będzie znikać (od 0, do 255).
| Druga forma taga pozwala na pełną kontrolę nad czasami w jakich
  wykonuje się efekt, a także nad stopniami przezroczystości:
| :code:`\fade(<a1>,<a2>,<a3>,<t1>,<t2>,<t3>,<t4>)`, gdzie:

-  tekst ma przezroczystość ``a1`` aż do momentu ``t1``
-  między ``t1`` a ``t2`` przezroczystość przechodzi z ``a1`` do ``a2``
-  między ``t2`` a ``t3`` przezroczystość ma stałą wartość ``a2``
-  między ``t3`` a ``t4`` przezroczystość przechodzi z ``a2`` do ``a3``
-  po momencie ``t4`` tekst ma przezroczystość ``a3``

.. _ruch-1:

Ruch
~~~~

.. warning::
    W znaku nie mogą znajdować się jednocześnie tag ruchu i pozycji - doprowadzi to do błędów w twoim znaku

W Kainote wbudowane jest narzędzie ruchu, jest to pozycja którą
pominęliśmy wcześniej przy edytorze wideo: |movement example|

-  Kwadrat oznacza pozycję początkową
-  Kółko oznacza pozycję końcową tekstu
-  krzyżyk oznacza pozycję w danej klatce

Po zaczęciu rysowania ruchu Kainote wstawi do twojego znaku tag
:code:`{\move(<x1>,<y1>,<x2>,<y2>,<t1>,<t2>)}`, który podmieni ew. tag ruchu, często nie będziesz chcieć,
aby animacja trwała całą linijkę, parametry ``<t1>`` i ``<t2>``
odpowiadają czasom rozpoczęcia i zakończenia ruchu.

Transformacje
~~~~~~~~~~~~~

| Ponad dwa przedstawione powyżej specjalne przypadki, często zdarzy
  się, że będziesz chciał animować rozmycie, rozmiar czcionki, kolor,
  czy inny z wielu dostępnych parametrów. Można to zrobić w prosty
  sposób z użyciem tagu transformacji: ``{\t(<t1>,<t2>,<tag>)}``.
| Ten tag pozwala na utowrzenie prostych, liniowych przejść między zdefiniowanymi stanami tagów,
| Przed :code:`<t1>` nastawi wartość domyślną, zdefiniowaną w znaku, a następnie między :code:`<t1>`` a :code:`<t2>`` wygeneruje dynamiczne przejście do nowego stanu :code:`<tag>`, np. |Transform example|

   Sekwencja tagów ``{\blur10\t(0,147,\blur0)}``