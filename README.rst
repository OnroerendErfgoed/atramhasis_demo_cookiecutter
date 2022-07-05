=======================
atramhasis demo project
=======================

Requirements
------------

*   Python 3.6+
*   npm
*   `cookiecutter <https://cookiecutter.readthedocs.io/en/latest/installation.html>`_

Usage
-----

#.  Generate an atramhasis demo project.

    .. code-block:: bash

        cookiecutter gh:OnroerendErfgoed/atramhasis_demo_cookiecutter
        # Or create a project from a specific cookiecutter branch/release
        # cookiecutter gh:OnroerendErfgoed/atramhasis_demo_cookiecutter --checkout develop

#.  Create a virtual environment and install requirements

    .. code-block:: bash
         
        # create a new virtual environment for the project, fe python -m venv $HOME/.virtualenvs/atramhasis_demo_venv
        # Change directory into your newly created project if not already there.
        pip install -r requirements-dev.txt
        pip install -e .

#.  Setup database

    .. code-block:: bash

        alembic upgrade head
        # fill the database with data
        initialize_atramhasis_db development.ini

#.  install frontend requirements

    .. code-block:: bash

        cd <package>/static
        npm install

#.  Run server

    .. code-block:: bash

        cd <root of repo>
        pserve development.ini
