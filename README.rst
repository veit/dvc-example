Quick start
===========

|Contributors| |License| |Docs|

.. |Contributors| image:: https://img.shields.io/github/contributors/veit/dvc-example.svg
   :target: https://github.com/veit/dvc-example/graphs/contributors
.. |License| image:: https://img.shields.io/github/license/veit/dvc-example.svg
   :target: https://github.com/veit/dvc-example/blob/master/LICENSE
.. |Docs| image:: https://readthedocs.org/projects/dvc-example/badge/?version=latest
   :target: https://dvc-example.readthedocs.io/de/latest/

Installation
------------

#. Download and unpack:

   .. code-block:: console

    $ curl -O https://codeload.github.com/veit/dvc-example/zip/master
    $ unzip master
    Archive:  master
    …
       creating: dvc-example-master/
    …

#. Create HTML documentation:

   .. code-block:: console

    $ python3 -m venv .
    $ bin/python -m pip install --upgrade pip
    $ bin/python -m pip install -r requirements.txt
    $ bin/sphinx-build -ab html docs/ docs/_build/

#. Create PDF:

   To create PDFs you need additional packages.

   For Debian/Ubuntu you can get them with:

   .. code-block:: console

    $ apt-get install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended latexmk

   or for Mac OS X with:

   .. code-block:: console

    $ brew cask install mactex
    …
    🍺  mactex was successfully installed!
    $ curl --remote-name https://www.tug.org/fonts/getnonfreefonts/install-getnonfreefonts
    $ sudo texlua install-getnonfreefonts
    …
    mktexlsr: Updating /usr/local/texlive/2020/texmf-dist/ls-R...
    mktexlsr: Done.

   You can then generate a PDF with:

   .. code-block:: console

    $ cd docs/
    $ pipenv run make latexpdf
    …
    The LaTeX files are in _build/latex.
    Run 'make' in that directory to run these through (pdf)latex
    …

   You will then find the PDF in :file:`docs/_build/latex/dvc-example.pdf`.

Follow us
---------

* `GitHub <https://github.com/veit/dvc-example>`_
* `Twitter <https://twitter.com/JupyterTutorial>`_
* `Mastodon <https://mastodon.social/@JupyterTutorial>`_

Pull requests
-------------

If you have suggestions for improvements and additions, I recommend you, create a `Fork
<https://github.com/veit/dvc-example/fork>`_ of my GitHub repository
<https://github.com/veit/dvc-example/>`_ and make your changes in it. You are also
welcome to make a *Pull request* if you like. As long as the changes in it are small and
atomic, I’m happy to look at your your suggestions with pleasure.
