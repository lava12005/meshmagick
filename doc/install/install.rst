Installation Instructions
=========================


.. warning::
    Meshmagick is written in Python 2.7 only. So please ensure that you have a Python 2.7 distribution.

Meshmagick is packaged for every major OS (*nix, Windows, OS/X) for both 32/64 bit systems.

Installing with conda
---------------------

This is the prefered method to get your own packaged copy of Meshmagick as `conda <http://conda.pydata.org/docs/>`_
is known to deal with every dependencies of Meshmagick. For this, you will need to install
`Anaconda <https://www.continuum.io/downloads>`_ Python distribution or simply
`Miniconda <http://conda.pydata.org/miniconda.html>`_ for your architecture which are shipped with the conda package
manager. If you are not an everyday Python developer, maybe you will prefer installing Miniconda which is far mush
lighter than Anaconda.

Once conda installed, just try this::

    conda install -c frongere meshmagick

It will download the Meshmagick package corresponding to your architecture. If everything goes well, it will install
for you the dependencies. You may now test the install by::

    meshmagick -h

which should now show you the embedded help of the command line tool.

Updating to the latest meshmagick version is obtained by::

    conda update meshmagick

Installing with pip
-------------------

For those wanting to use pip, just do::

    pip install meshmagick

It will install Meshmagick from Pypi.

Update to the newest version is achieved by::

    pip install meshmagick --upgrade

.. note::
    This is not the preferred method as Meshmagick depends on vtk for its visualization features which is sadly not
    available on Pypi. You will then have to deal with this dependency by yourself.

Installing from source
----------------------

This can be done by checking out the source files from the Git source code repository. This option is mainly for
those wanting to develop into Meshmagick.

1. Clone the meshmagick repository::

    git clone https://github.com/LHEEA/meshmagick.git

2. Change directory to meshmagick

3. Install:

    * If you want to install from source for just use meshmagick, it can be achieved by::

        python setup.py install

    * If you want to install from soruce for development purposes, you should better install meshmagick in
      development mode so that your code modifications are directly taken into account with respect to your install.
      It is achieved by the command::

        pip install -e .

4. (Optional) Run ``pytest`` if you have `pytest <http://doc.pytest.org/en/latest/>`_ installed.
