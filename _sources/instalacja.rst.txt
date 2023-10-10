==========
Instalacja
==========

Kainote
=======
| Kainote będzie podstawowym narzędziem pracy. Stworzony przez polskiego tłumacza Bakurę fork `Aegisub'a <https://github.com/Aegisub/Aegisub>`_, 
    oryginalnego narzędzia do pracy z plikami w formacie SSA pozwalający na bardziej zaawansowaną pracę, m.in. w kontekście typesettingu. 
    Razem z Kainotem dołączana jest także większa ilość skryptów do automatyzacji.
| Najnowszą wersję Kainote można pobrać z
  `githuba <https://github.com/bjakja/Kainote/releases/latest>`_
| Lub `niestabilny build
  2022.11.11 <https://drive.google.com/uc?id=1ECqsrLo5d1jPoz-FKvJrS0279YeTKrmS&export=download>`_

Enkodery Wideo
==============

W pracy z wideo potrzebne będą Ci dwa enkodery, są to aplikacje uruchamiane w konsoli pozwalające na zaawansowaną manipulację wideo.

.. hint::
    Odpowiednie skrypty możesz też znaleźć w repozytoriach `chocolatey'a <https://chocolatey.org/install>`_, albo `win-get'a <https://learn.microsoft.com/en-us/windows/package-manager/winget/#install-winget>`_, w ten sposób zostaną one od razu zainstalowane.

Odpowiednie pliki wykonawcze znajdziesz na stronach producentów:
    -  `ffmpeg <http://ffmpeg.org/download.html>`_
    -  `x264 <https://artifacts.videolan.org/x264/release-win64/x264-r3101-b093bbe.exe>`_

Pobrane skrypty będziesz musiał dodać do PATH'a, są na to dwa sposoby:
    - Umieścić w istniejącej ścieżce
        .. warning::
            Przy wykorzystaniu tego sposobu należy unikać dodawania czegokolwiek ręcznie do ścieżek systemowych, takich jak :code:`C:\Windows`, czy :code:`C:\Windows\system32`, uszkodzenie czegoś w tych ścieżkach może skutkować całkowitym uszkodzeniem systemu.

    - Dodać skrypty do nowej ścieżki i ją dodać do PATH'a:
        #. Utworzyć nową ścieżkę, np. :code:`C:\Users\{user-name}\bin`
        #. Skopiować dwa pobrane pliki :code:`*.exe` do powyższej ścieżki
        #. Otworzyć edytor zmiennych środowiskowych:
            :code:`Panel Kontrolny > System > Edytuj zmienne środowiskowe dla konta` 
        #. Znajdź pozycję PATH, kliknij edytuj i dodaj swoją ścieżkę

Jeśli wszystko się powiodło to wywołując w konsoli komendy `ffmpeg` i `x264` powinieneś zobaczyć ich dokumentację.

Odtwarzacz wideo
================

.. hint::
    Te same programy możesz też znaleźć w repozytoriach `chocolatey'a <https://chocolatey.org/install>`_, albo `win-get'a <https://learn.microsoft.com/en-us/windows/package-manager/winget/#install-winget>`_, w ten sposób zostaną one od razu zainstalowane.

Windows media player nie wspiera natywnie plików MKV - jest to zaawansowany format wideo przechowujący wiele danych na temat plików, między innymi podział na rozdziały, wiele ścieżek audio, wideo, czy z napisami. Zazwyczaj wykorzystuje się do tego jeden z dwóch programów:
    - `MPV <https://mpv.io/>`_
    - `VLC <https://www.videolan.org/vlc/index.pl.html>`_ 

QuickTime Player
================

QuickTime Player jest odtwarzaczem wideo zaprojektowanym przez Apple, będzie nam potrzebny do w poprawnego funkcjonowania Mochy - jest on wykorzystywany do odtwarzania większości formatów wideo.
`Link do oficjalnej strony <https://support.apple.com/pl_PL/downloads/quicktime>`_.

Boris FX Mocha Pro
==================

.. warning:: 
    | Link do mochy pochodzi z torrentów, pamiętaj że takie oprogramowanie może być niebezpieczne dla twojego komputera. Przed uruchomieniem sprawdź czy program nie jest skażony wirusem.
    | Dla bezpieczeństwa zawartość torrentów powinno pobierać się przez serwisy VPN.

| Mocha jest uważana za najlepsze dostępnym obecnie na rynku narzędziem do śledzenia ruchu w wideo.
| Dostępna jest w kilku formach:
    1. rozszerzenie do Adobe After Effects
    2. osobne oprogramowanie

Wszystkie wersje Mochy możesz znaleźć tutaj:
`Boris FX Mocha PRO 2020 na 1337x.to <https://1337x.to/torrent/4423707/Boris-FX-Mocha-Pro-2020-5-v7-5-0-Build-1274-Plug-ins-for-Adobe-OFX-CrackzSoft/>`__
Poradnik będzie skupiał się na obsłudze samodzielnej dystrybucji Mochy
Z plików znajdujących się w torrencie potrzebna ci będzie wersja standalone, instrukcja instalacji powinna znajdować się w odpowiednim pliku :code:`read_me.txt`.

Czcionki
========

| Ostatnim krokiem instalacji są czcionki. Nie ma tu definitywnej listy, wręcz przeciwnie - prawdopodobnie zawsze będziesz potrzebować jeszcze czegoś, na dobry początek jednak moją paczkę czcionek możesz znaleźć na `mega.nz <ttps://mega.nz/folder/o6BUTT6Q#v1bMX7YsiWt_Rg9TLi1WkA>`_.
| W poszukiwaniu nowych czcionek warto sprawdzać:
-  `1001 fonts <https://www.1001fonts.com/>`__
-  `dafont <https://www.dafont.com/>`__