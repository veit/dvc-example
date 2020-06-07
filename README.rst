Schnelleinstieg
===============

|Contributors| |License| |Docs|

.. |Contributors| image:: https://img.shields.io/github/contributors/veit/dvc-example.svg
   :target: https://github.com/veit/dvc-example/graphs/contributors
.. |License| image:: https://img.shields.io/github/license/veit/dvc-example.svg
   :target: https://github.com/veit/dvc-example/blob/master/LICENSE
.. |Docs| image:: https://readthedocs.org/projects/dvc-example/badge/?version=latest
   :target: https://dvc-example.readthedocs.io/de/latest/

Installation
------------

#. Herunterladen und Auspacken:

   .. code-block:: console

    $ curl -O https://codeload.github.com/veit/dvc-example/zip/master
    $ unzip master
    Archive:  master
    …
       creating: dvc-example-master/
    …

#. HTML-Dokumentation erstellen:

   .. code-block:: console

    $ python3 -m venv .
    $ bin/python -m pip install --upgrade pip
    $ bin/python -m pip install -r requirements.txt
    $ bin/sphinx-build -ab html docs/ docs/_build/

#. PDF erstellen:

   Für die Erstellung von PDFs benötigt ihr weitere Pakete.

   Für Debian/Ubuntu erhaltet ihr diese mit:

   .. code-block:: console

    $ apt-get install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended latexmk

   oder für Mac OS X mit:

   .. code-block:: console

    $ brew cask install mactex
    …
    🍺  mactex was successfully installed!
    $ curl --remote-name https://www.tug.org/fonts/getnonfreefonts/install-getnonfreefonts
    $ sudo texlua install-getnonfreefonts
    …
    mktexlsr: Updating /usr/local/texlive/2020/texmf-dist/ls-R...
    mktexlsr: Done.

   Anschließend könnt ihr ein PDF generieren mit:

   .. code-block:: console

    $ cd docs/
    $ pipenv run make latexpdf
    …
    The LaTeX files are in _build/latex.
    Run 'make' in that directory to run these through (pdf)latex
    …

   Das PDF findet ihr anschließend in ``docs/_build/latex/dvc-example.pdf``.

Folge uns
---------

* `GitHub <https://github.com/veit/dvc-example>`_
* `Twitter <https://twitter.com/VeitSchiele>`_

Pull-Requests
-------------

Wenn ihr Vorschläge für Verbesserungen und Ergänzungen habt, empfehle ich euch,
einen `Fork <https://github.com/veit/dvc-example/fork>`_ meines
`GitHub-Repository <https://github.com/veit/dvc-example/>`_ zu erstellen
und darin eure Änderungen vorzunehmen. Gerne dürft ihr auch einen *Pull Request*
stellen. Sofern die darin enthaltenen Änderungen klein und atomar sind, schaue ich
mir eure Vorschläge gerne an.

