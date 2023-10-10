.. |Gradient Everything| image:: https://user-images.githubusercontent.com/61905404/202865975-acf4b641-3b6e-45cd-8bb4-d9ea19c52874.png
.. |Gradient example| image:: https://user-images.githubusercontent.com/61905404/202866234-2beb7536-2f10-4248-80d5-203028b576a0.png
.. |Recalculator example| image:: https://user-images.githubusercontent.com/61905404/202866326-8c5dddcf-d5c6-4468-9384-79002fd4cc2a.png
.. |Perspective.py step 1| image:: https://user-images.githubusercontent.com/61905404/202866844-2de8e767-7aa6-40d6-b4dd-bf9a3b3102dd.png


======================
Kainote: Automatyzacja
======================

Kainote ma preinstalowanych parę użytecznych skryptów do autoamtyzacji,
znajdziesz je pod rozwijanym menu na pasku.

.. note::
    To tylko opis paru najczęściej używanych/najprzydatniejszych skryptów, jest jednak sporo bardziej "niszowych" skryptów,
    które możesz znaleźć w skrypcie **Dependency Control** lub na `githubie <https://github.com/topics/aegisub>`_.

Aegisub Motion
~~~~~~~~~~~~~~

| Będzie to najczęściej używany przez ciebie skrypt.
| Służy on do generowania zaawansowanych animacji ruchu (śledzenia).
| Opis działania skryptu znajdziesz w sekcji :ref:`Zaawansowane animacje <advanced_anim>`

Gradient Everything
~~~~~~~~~~~~~~~~~~~
| To narzędzie służące do generowania różnego rodzaju gradientów - dynamicznych przejść z jednego stanu do drugiego przez tzw. klatki kluczowe

.. note::
    Narzędzie pozwala na generowanie gradientów w różnych formach - kolorach, przezrocystości, rotacji, etc.
    Na potrzeby poradnika skupię się na kolorze, jednak pozostałe gradienty tworzy się na takiej samej zasadzie.

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
  :code:`Automatyzacja>Gradient Everything>Gradient Everything/Gradient Everything`,
  pojawi się nowe okno: |Gradient Everything|
| W oknie możesz wybrać tagi, które zostaną poddane efektowi gradientu,
  parametr Obok parametru :code:`pixels per strip` jest kierunek, w którym
  poruszać będzie się gradient.
| Parametr :code:`Acceleration` zmienia sposób w jaki wygenerowany zostanie
  gradient:

-  > 1 zaczyna się szybko, kończy powoli
-  < 1 zaczyna się powoli, kończy szybko

Na samym dole okna dialogowego możesz też znaleźć opcję zapisania znajdziesz
menu z opcjami do zapisywania/wczytywania/edycji gradientów do wielokrotnego użytku

Efekt wygenerowania gradientu na kolorze z powyższych linijek wygląda
tak: |Gradient example|

Recalculateor
~~~~~~~~~~~~~

Recalculator jest prostym sposobem na zmodyfikowanie pojedynczego tagu w
wielu linijkach na raz |Recalculator example|

| Zmodyfikuj jeden z dwóch głownych parametrów - zmianę procentową, albo
  zmianę o wartość, wybierz tagi, które chcesz zmienić.
| W przedostatniej linijce znajdują się modyfikatory, możesz dzięki temu
  zmieniać wartość o więcej z każdą kolejną linijką, np.
  :code:`15>30>45>60>75` etc.
| Jak widać główne dwie funkcje, z których będziesz korzystać to
  mnożenie/dodawanie, jeśli chciałbyś odjąć wystarczy ustawaić ujemną
  wartość w polu tekstowym

.. _perspectivepy:

Perspective.py
~~~~~~~~~~~~~~

.. seealso::
  `Script by Zeght on
  Github <https://github.com/TypesettingTools/Perspective/blob/master/perspective.py>`__

.. warning::
  Perspektywa wygenerowana w ten sposób przemieści punkt :code:`{\org()}`, z tego powodu nie będzie działała w ruchu.

| Jest to narzędzie CLI napisane w pythonie, służące do wygenerowania
  tagów odpowiednich tagów, na podstawie kształtu, które będą odpowiadać rotacji obiektu na
  ekranie. Sposób korzystania z aplikacji jest prosty:

1. Za pomocą narzędzia clipu wektorowego narysuj obrys czegoś, co w
   przeszłości było prostokątem od lewego górnego rogu, zgodnie z ruchem
   wskazówek zegara |Perspective.py step 1|
2. Przeklej kształt wygenerowany w tagu ``{\clip()}`` do konsoli razem z komendą, np.
   ::

      python3 perspective.py "m 845 78 l 1233 164 1213 218 825 131"

3. Konsola odpowie kilkoma możliwymi perspektywami, wybierz najlepszą i
   przeklej na początek linijki, gotowe!
   ::

      Transforms near center of tetragon: