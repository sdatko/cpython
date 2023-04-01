Zaskroniec
==========

Niniejsze repozytorium należy rozpatrywać jako demo technologiczne.

**Uwaga**: jest to jeszcze **wersja** bardzo wczesno-**poglądowa**!


Polski Python
-------------

Programuj z polskimi słowami kluczowymi!


Jak zacząć?
-----------

Uruchom następujące komendy::

    ./configure --prefix=/opt/zaskroniec/
    make
    sudo make altinstall

W systemie zostanie instalowany interpreter ``/opt/zaskroniec/bin/zaskroniec``


Przykłady
---------

Zajrzyj do katalogu ``PRZYKŁADY/``, aby odnaleźć wzorcowe kody.

Nasze pliki źródłowe stosują emoji węża jako rozszerzenie: 🐍

Na przykład::

    /opt/zaskroniec/bin/zaskroniec PRZYKŁADY/pętle.🐍

**Podpowiedź**:
użyj klawisza ``[TAB]`` i mechanizmu auto-uzupełniania powłoki dla wygody ;-)


Dlaczego?
---------

Ponieważ dobry żart jednocześnie bawi i uczy!

Celem nadrzędnym było zapoznanie się z tym, jak zbudowany jest interpreter
języka Python oraz jak można go zmodyfikować w jakimś konkretnym celu.
Prześledź ostatnie zmiany w repozytorium, aby zobaczyć co zostało zrobione!

Plik ``Grammar/Grammar`` zawiera definicję podstawowej składni języka,
czyli słów kluczowych i w jakiej kombinacji mogą one wystąpić w programie,
zaś w pliku ``Python/bltinmodule.c`` można znaleźć kod wbudowanych funkcji.

Po modyfikacji pliku z gramatyką, należy wykonać komendę ``make regen-grammar``
(lub ``make regen-all``), aby zmiany gramatyki zostały odwzorowane w plikach
źródłowych interpretera (w języku **C**).

Oryginalną inspirację stanowił ten artykuł:
`<https://realpython.com/cpython-source-code-guide/#using-pgen>`_.

**Uwaga!** Wersja 3.9 interpretera CPython zmieniła trochę sposób definiowania
gramatyki. Wykorzystuje ona nowy format oraz narzędzie – i chociaż co do idei
wszystko wygląda tak samo, to z jakiegoś powodu nie udało mi się zmusić nowszej
wersji do respektowania nowych słów kluczowych (a nie miałem czasu drążyć...).

Zainteresowanych zgłębieniem tematu odsyłam do wyżej podanego artykułu oraz
oficjalnej dokumentacji: `<https://devguide.python.org/internals/parser/>`_.


Źródło
------

Cały pierwotny kod źródłowy zaczerpnięto z repozytorium:
`<https://github.com/python/cpython>`_
