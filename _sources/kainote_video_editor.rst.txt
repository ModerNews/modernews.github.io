.. |Kainote Module: Video| image:: https://user-images.githubusercontent.com/61905404/202861945-84d1fece-db6c-4244-9e12-eb12f4e36dc2.png
.. |rotation Z example| image:: https://user-images.githubusercontent.com/61905404/202862421-32c86265-0a9d-4226-b0da-54756a41f4b9.png
.. |rotation X Y example| image:: https://user-images.githubusercontent.com/61905404/202862624-8e0c3307-1ad2-4f52-82ca-a128d1d26c8e.png
.. |clip example| image:: https://media.discordapp.net/attachments/783791354374783016/1043572977062645800/image.png
.. |shape example| image:: https://media.discordapp.net/attachments/783791354374783016/1043575246009147502/image.png
.. |shape options| image:: https://user-images.githubusercontent.com/61905404/202863282-db311b1c-1622-4e14-bf64-8ba4ba3bff11.png
.. |bezier curve example| image:: https://user-images.githubusercontent.com/61905404/202863452-a1e2eba4-b958-40fc-98b7-d64cd0643a6b.png

========================
Edytor graficzny Kainote
========================

Większość efektów dot. pozycji, można nałożyć z poziomu podglądu
wideo, pozwala on nam na przemieszczanie, obracanie, etc. znaku na
nagraniu w czasie rzeczywistym (i nie wymaga bawienia się wartościami
ręcznie)

|Kainote Module: Video|

Najważniejsze służące do tego kontrolki znajdują się bezpośrednio pod
odtwarzaczem, od lewej:

Przesuwanie tekstu
~~~~~~~~~~~~~~~~~~

Służy do przesuwania tekstu na obrazie, wpływa jedynie na znacznik
pozycji :code:`{\pos(<x>,<y>)}`, jeśli wcześniej linijka zawierała znacznik
ruchu :code:`{\move()}` zostanie on zastąpiony, znacznik zostanie wstawiony
na początku linijki

Ruch
~~~~

Więcej na ten temat w sekcji **Proste animacje**

Skalowanie
~~~~~~~~~~

Pozwala na skalowanie napisów (:code:`{\fscx<float>\fscy<float>}`), znacznik
zostanie wstawiony na początku linijki

Obrót w osi Z
~~~~~~~~~~~~~

.. warning::
    | W obu przypadkach rotacji znajduje się punkt *origin* (opisany poniżej).
    | Przeniesienie tego punktu wpłynie nieprzewidywalnie na napisy
      będące w ruchu. (szczególnie w ruchu z wykorzystaniem Mochy)

| Obrót w osi Z jest obrotem w płaszczyźnie ekranu :code:`{\frz<float>}`,
  może przyjmować zarówno wartości dodatnie jak i ujemne.
| |rotation Z example|
| Dodatkowo w trybie tym możemy edytować tzw. punkt *origin*, jest on
  oznaczony przez czerwony krzyżyk widoczny na środku zrzutu ekranu.
  Przeciągnięcie go spowoduje zmianę punktu, wokół którego dokonywany
  jest obrót.

Obrót w osiach X i Y
~~~~~~~~~~~~~~~~~~~~

| Ta funkcja pozwala nam na obrócenie tekstu w dwóch pozostałych
  płaszczyznach, dzięki czemu otrzymamy efekt pochylenia, widoczna
  siatka jest poglądem płaszczyzny, na której aktualnie znajduje się
  tekst. Zmiany w osi X dokonuje się przytrzymaniem PPM, zmiany w osi Y
  przytrzymaniem LPM.
| W tym trybie również można znaleźć punkt *origin*, oznaczony czerwonym
  krzyżykiem.
| |rotation X Y example|

Clipy
-----

Następne dwa narzędzia to clipy, pierwsze z nich prostokątne, drugie
wektorowe, obydwa generują tag :code:`{\clip(<shape>)}`. Po stworzeniu clipa
widoczny będzie tylko tekst wewnątrz zaznaczonego kształtu |clip
example|

.. note::
    | Efekt ten można odwrócić dodając *i* (ang. *inverted*) do tagu clipa: :code:`{\iclip(<shape>)}`.
    | Spowoduje to, że tekst znajdujący się wewnątrz zaznaczonego kształtu zniknie.

Rysowanie
---------

Rysowanie pozwala na stworzenie prostego rysunku wektorowego wewnątrz pliku napisów, zostanie on
wstawiony w danej linijce i przejmie wszystkie jej
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
-  Narzędzie rysowania krzywych B-sklejanych, działa poprzez stworzenie ciągu kolejnych krzywych Beziera
-  Tworzenie punktów niezależnych od aktualnie rysowanego kształtu
-  Usuwanie punktów

Zmieniacz pozycji
~~~~~~~~~~~~~~~~~

| Zmieniacz pozycji jest nieco bardziej zaawansowaną wersją narzędzia
  przesuwania, po prawej stronie znajdziesz nowe opcje: pozwolą ci one
  wybrać jakie elementy linijki chcesz przesuwać:
  nie tylko sam tekst, ale również ograniczający go clip, punkty ruchu, możesz wybrać wiele na
  raz.