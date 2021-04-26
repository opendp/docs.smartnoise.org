Python
======

The main OpenDP repo contains Python bindings and associated tests. In order to contribute, you will need to build the OpenDP library, which is written in Rust. Our goal is to get a successful run of the tests.

.. contents:: Contents:
	:local:

Install Languages
-----------------

The languages below need to be installed.

Rust
++++

Download Rust from the `Rust website`_.

.. _Rust website: https://www.rust-lang.org

Python
++++++

Download Python from the `Python website`_.

.. _Python website: https://www.python.org

Clone the OpenDP Repo
---------------------

Clone the repo and change into the ``opendp`` directory that's created.

.. code-block:: bash

    git clone https://github.com/opendp/opendp.git
    cd opendp

Build OpenDP
------------

You will need Rust installed to build OpenDP. Change to the ``rust`` directory before attempting a build, and then return to the ``opendp`` directory.

.. code-block:: bash

    cd rust
    cargo build
    cd ..

Install Python Dependencies
---------------------------

Change to the ``python`` directory, create a Python virtual environment, activate it, install dependencies, and then install the Python OpenDP library itself.

.. code-block:: bash

    cd python
    python3 -m venv venv
    source venv/bin/activate
    pip install flake8 pytest
    mkdir src/opendp/lib
    pip install -e .

Run the Tests
-------------

From the ``python`` directory, set an environment variable to the location of the OpenDP library you built. Then run the tests.

.. code-block:: bash

    export OPENDP_LIB_DIR=../rust/target/debug
    python -v
