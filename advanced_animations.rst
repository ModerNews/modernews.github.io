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

.. _advanced_anim:

=====================
Zaawansowane animacje
=====================
.. warning::
    Do tego segmentu przydadzą ci się dodatkowo: `Wideo do Odcinka 1
    Kaguya-Sama Love is War: Ultra Romantic
    (nyaa.si) <https://nyaa.si/view/1511966>`__

Większość zaawansowanych animacji, które wykonujemy w typesettingu
(wyjątek: efekty karaoke) opiera się o nieregularne zmiany pozycji,
rotacji, obrazu, czy perspektywy. Są to efekty, które ciężko odtworzyć ręcznie (lub zajmuje to nadmiernie dużo czasu) np.:

|Kaguya-sama Love is War: Ultra Romantic E03 Klatki 11665-11766|

   Kaguya-Sama, S03E01, znak mówi ``Co porabisz?``

Wykonanie podstawy znaku
~~~~~~~~~~~~~~~~~~~~~~~~

Na samym początku musimy wykonać znak dla jednej z klatek - tak, by było
potem co wprawić w ruch. Nowe wersje Aegisub-Motion pozwalają na odtworzenie
ruchu z dowolnej klatki, natomiast dobrą praktyką jest wybieranie
pierwszej lub ostatniej - w ten sposób nie powinno być problemu z
przypadkowym przesunięciem znaku w czasie w późniejszych etapach. Pamiętaj też,
aby sprawdzić timing, najlepiej w trybie podglądu klatek (przełącznik
znajdziesz nad polem edycji linijki), pierwsza i ostatnia klatka powinny
pokrywać się z pierwszą i ostatnią klatką obecności znaku na ekranie,
**a nie kaltkę przed/po**. Nasz znak może wyglądać np. tak:

|Znak ruchomy Mocha, Step 1|

Konfiguracja Aegisub-Motion
~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. note::
    Jeśli znasz dobrze skrypt x264 lub ffmpeg możesz napisać własną komendę, wyciągąjącą określone klatki

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

Następnym krokiem będzie wyciągnięcie wideo i zaimportowanie go do Mochy.
Zrobienie tego jest proste, dzięki narzędziom automatyzacji wystarczy parę kliknięć na pasku:
``Automatyzacja > Aegisub-Motion > Aegisub-Motion/Trim``, powinno otworzyć się okno konsoli i wideo powinno po chwili zostać przycięte automatycznie.
Po zakończeniu działania skryptu przycięty fragment powinieneś znaleźć w tym samym folderze co oryginalne wideo.

Stworzenie nowego projektu w Boris FX Mocha
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| Następnie przeniesiemy się do Mochy, po otwarciu programu z paska
  wybierz: ``File > New Project``
| Otworzy się nowe okno:
| |Boris FX Mocha Pro: New Project Module|
| Klikamy ``Choose...`` i wybieramy przycięty przed chwilą fragment,
  pozostałe parametry Mocha uzupełni samoczynnie na podstawie metadanych i pliku i w większości przypadków powinno się je tak zostawić

.. warning::
    W niektórych przypadkach może wystąpić błąd i ilość klatek na sekundę może zostać źle zdefiniowana w metadanych - doprowadzi to do przesunięcia finalnego znaku.

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
    potrzebny np. tryb classic, w którym znajdziemy możliwość wygenerowania siatki śledzenia, zamiast obramówki.

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
następnego kroku.

.. warning::
    W niektórych przypadkach warto poeksperymentować z zaznaczeniem - wybrać jedynie segment znaku, który chcemy śledzić,
    albo zupełnie inny fragment klatki poruszający się w ten sam sposób. Czasami docelowy znak jest zbyt skomplikowany, albo częściowo zakryty
    , co uniemożliwia Mocha'e prawidłowe wyśledzenie ruchu.

Import do Kainote
-----------------

Aby wyeksportować przygotowany przez Mochę ruch wciskamy wcześniej
wspomniany przeze mnie przycisk na samym dole panelu z kontorlkami do
śledzenia :code:`Export Tracking Data` jest napisane na przycisku (jeśli
jest on nieaktywny sprawdź, czy na pewno masz wybraną którąś z warstw).
Po jego wciśnięciu wyskakuje nowe okno: |Boris FX Mocha Pro: Export
Tracking Data Dialogue|

| Interesujący nas format jest tym samym, który otwiera się domyślnie:
| :code:`After Effects Transform Data [position, scale and rotation] (*.txt)`
| Wystarczy nam skopiować go do schowka, nie potrzebujemy mieć tego
  nigdzie zachowanego.

.. warning::
    Przypilnuj, aby jako :code:`reference` oznaczona była ta sama klatka, w której stworzony był znak, inaczej pozycja znaku nie zostanie wygenerowana poprawnie.

| Następnie w Kainote zaznaczamy linijkę, bądź linijki, do których
  chcemy zaaplikować nasz efekt. I z menu
  automatyzacji tym razem wybieramy Aegisub-Motion/Apply:
| :code:`Automatyzacja > Aegisub-Motion > Aegisub-Motion/Apply`
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

