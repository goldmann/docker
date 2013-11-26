:title: Requirements and Installation on Fedora
:description: Please note this project is currently under heavy development. It should not be used in production.
:keywords: Docker, Docker documentation, requirements, virtualbox, vagrant, git, ssh, putty, cygwin, linux

.. _fedora:

Fedora
======

.. include:: install_header.inc

.. include:: install_unofficial.inc

Right now, the only supported distributions are:

- :ref:`fedora_core19`
- :ref:`fedora_core20`

.. _fedora_core19:

Fedora Core 19 (64-bit)
^^^^^^^^^^^^^^^^^^^^^^^

This installation path should work at all times.

Installation
------------

Firstly, let's make sure our Fedora host is up-to-date.

.. code-block:: bash

    sudo yum -y upgrade

Next let's install the ``docker-io`` package which will install Docker on our host.

.. code-block:: bash

   sudo yum -y install docker-io

Now it's installed lets start the Docker daemon.

.. code-block:: bash

    sudo systemctl start docker.service

If we want Docker to start at boot we should also:

.. code-block:: bash

   sudo systemctl enable docker.service

Now let's verify that Docker is working.

.. code-block:: bash

   sudo docker run -i -t ubuntu /bin/bash

**Done!**, now continue with the :ref:`hello_world` example.

.. _fedora_core20:

Fedora Core 20 (64-bit)
^^^^^^^^^^^^^^^^^^^^^^^

Use the :ref:`fedora_core19` instructions.

