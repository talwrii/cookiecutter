============
Installation
============

Prerequisites
-------------

* Python interpreter
* Adjust your path
* Packaging tools

Python interpreter
^^^^^^^^^^^^^^^^^^

Install Python for your operating system. Consult the official `Python documentation <https://docs.python.org/3/using/index.html>`_ for details.

You can install the Python binaries from `python.org <https://www.python.org/downloads/mac-osx/>`_. Alternatively on macOS, you can use the `homebrew <http://brew.sh/>`_ package manager.

.. code-block:: bash

    # for python 3.x
    $ brew install python3


Adjust your path
^^^^^^^^^^^^^^^^

Ensure that your ``bin`` folder is on your path for your platform. Typically ``~/.local/`` for UNIX, or ``%APPDATA%\Python`` on Windows. (See the Python documentation for `site.USER_BASE <https://docs.python.org/3/library/site.html#site.USER_BASE>`_ for full details.)

On UNIX and macOS, for bash shells, add the following to your ``.bash_profile`` (adjust for other shells):

.. code-block:: bash

    # Add ~/.local/ to PATH
    export PATH=$HOME/.local/bin:$PATH

Remember to load changes with ``source ~/.bash_profile`` or open a new shell session.

On Windows, ensure the ``c:\Python3x`` directory is in your environment's ``Path``, where ``x`` is the minor version of installed Python, in order to make it possible to invoke Python from a command prompt by typing ``python``. You will also need to add your ``bin`` folder. To do so:

#. Right click ``My Computer``
#. Select ``Properties`` --> ``Advanced Tab`` --> ``Environment Variables``
#. Add each directory to the end of the ``Path`` environment variable, one for your Python interpreter and another for your ``bin`` folder.

   .. seealso:: See `Configuring Python (on Windows) <https://docs.python.org/3/using/windows.html#configuring-python>`_ for full details.


Packaging tools
^^^^^^^^^^^^^^^

``pip`` and ``setuptools`` now come with Python 2 >=2.7.9 or Python 3 >=3.4. See the Python Packaging Authority's (PyPA) documention `Requirements for Installing Packages <https://packaging.python.org/en/latest/installing/#requirements-for-installing-packages>`_ for full details.


Install cookiecutter
--------------------

At the command line:

.. code-block:: bash

    $ pip install --user cookiecutter

Or, if you do not have pip:

.. code-block:: bash

    $ easy_install --user cookiecutter

Though, pip is recommended.

Or, if you are using conda, first add conda-forge to your channels:

.. code-block:: bash

    $ conda config --add channels conda-forge

Once the conda-forge channel has been enabled, cookiecutter can be installed with:

.. code-block:: bash

    $ conda install cookiecutter

Alternate installations
-----------------------

**Homebrew (Mac OS X only):**

.. code-block:: bash

    $ brew install cookiecutter

**Pipsi (Linux/OSX only):**

.. code-block:: bash

    $ pipsi install cookiecutter

**Debian/Ubuntu:**

.. code-block:: bash

    $ sudo apt-get install cookiecutter

Upgrading from 0.6.4 to 0.7.0 or greater
----------------------------------------

First, read :doc:`history` in detail. There are a lot of major
changes. The big ones are:

* Cookiecutter no longer deletes the cloned repo after generating a project.
* Cloned repos are saved into `~/.cookiecutters/`.
* You can optionally create a `~/.cookiecutterrc` config file.

Upgrade Cookiecutter either with easy_install:

.. code-block:: bash

    $ easy_install --upgrade cookiecutter

Or with pip:

.. code-block:: bash

    $ pip install --upgrade cookiecutter

Then you should be good to go.
