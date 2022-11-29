==========
Instalacja
==========

Enkodery Wideo
==============

W pracy z wideo potrzebne będą Ci dwa enkodery, są to aplikacje uruchamiane w konsoli pozwalające na zaawansowaną manipulację wideo.

Windows
~~~~~~~

.. hint::
    Odpowiednie skrypty możesz też znaleźć w repozytoriach chocolatey'a, albo win-get'a, w ten sposób zostaną one od razu zainstalowane.

Odpowiednie pliki wykonawcze znajdziesz na stronach producentów:

-  `ffmpeg <http://ffmpeg.org/download.html>`__
-  `x264 <https://artifacts.videolan.org/x264/release-win64/x264-r3101-b093bbe.exe>`__

Pobrane skrypty będziesz musiał dodać do PATH'a, są na to dwa spozoby

#. Umieścić w istniejącej ścieżce
    .. warning::
        Przy wykorzystaniu tego sposobu należy unikać dodawania czegokolwiek ręcznie do ścieżek systemowych, takich jak :code:`C:\Windows`, czy :code:`C:\Windows\system32`, uszkodzenie czegoś w tych ścieżkach może skutkować całkowitym uszkodzeniem systemu.

#. Dodać skrypty do nowej ścieżki i ją dodać do PATH'a:
    #. Utworzyć nową ścieżkę, np. :code:`C:\Users\{user-name}\bin`
    #. Skopiować dwa pobrane pliki :code:`*.exe` do powyższej ścieżki
    #. Otworzyć edytor zmiennych środowiskowych