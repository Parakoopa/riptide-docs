MacOS
-----

This guide will explain how to install Riptide under MacOS.

.. note:: MacOS is not supported as well as the Linux setup. Most of the downsides
          of Riptide on MacOS come from the Docker Desktop implementation for MacOS.

          Riptide has some `Performance optimizations`_ to increase
          the performance on Mac, but it will still be slower than running it on Linux.

          If you have experience with Docker or Python on MacOS, we'd love your support in making
          Riptide on MacOS even better!

.. _Performance optimizations:  performance_optimizations.html

Installing Requirements
~~~~~~~~~~~~~~~~~~~~~~~

This guide assumes you want to run Riptide in the most common set-up using the Docker Engine.
To use Riptide you need to have the following installed:

* Python 3.6+
* pip for Python 3 (might come installed with Python)
* `Docker Desktop 16.0+ <https://www.docker.com/products/docker-desktop>`_

Python is available for Mac machines using package managers.

.. note:: If you know what the best way of installing Python 3 is, please let us know
          by updating this documentation on Github.

There is a good chance you already have Python installed. Try running ``python3 --version`` to check.

Installing Riptide system-wide
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. warning:: It is currently unknown if sudo must or even can be used when
             installing Riptide system-wide. It seems to depend on the way Python
             is installed and also the MacOS version.

             Please try with sudo first and see if this works. Make sure to remember
             if you installed with or without sudo, as you will need to update Riptide
             the same way, see below.

To install all Riptide components and the Docker implementation run the following command::

  $ [sudo] pip3 install riptide-all

Sudo may or may not be required, see warning above.

You can test if Riptide is working:

.. raw:: html

   <script src="../_static/asciinema-player.js"></script>
   <asciinema-player src="../_static/casts/test_riptide.cast" cols="80" rows="24"></asciinema-player>


Installing Riptide in a Virtualenv
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Riptide can also be installed in a Virtualenv. This is only recommended for advanced Python
users. Please make sure, to use the correct Python interpreter of your Virtualenv when
`setting up the proxy server <6_project.html>`_.

Updating Riptide
~~~~~~~~~~~~~~~~

To update Riptide, run

  $ [sudo] riptide_upgrade

Make sure to use or not use sudo, depending on if you did during your initial installation.
Failing to do so, WILL break your installation.

Configuring shared folders
~~~~~~~~~~~~~~~~~~~~~~~~~~
Docker Desktop for MacOS only allows the virtual machine running the Docker daemon
limited access to your machine.

The default configuration is not enough to use Riptide. Please open the settings
of Docker and navigate to the Shared Folders tab. Make sure the following entries
are present:

- /Users
- /Volumes
- /private
- /tmp
- /var/folders
- /usr/local/lib/python3.7 (**Or wherever else Python is installed!**)

Additional MacOS related notes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Many additional settings or issues not described in this documentation may be
directly related to the Docker Desktop for MacOS implementation.

Please see the `documentation for Docker Desktop for Mac <https://docs.docker.com/docker-for-mac/>`_ for further information.

Known issues under MacOS
~~~~~~~~~~~~~~~~~~~~~~~~

- Riptide currently uses the default Docker Desktop Mac daemon. This setup is known
  to have significantly worse performance than the Linux version. Riptide has some
  `Performance optimizations`_ to increase performance.
- Due to the performance optimization settings, it might happen that changes to files
  are not immediately visible on the host system or the running containers. Some files
  are not updated on the host system at all (see `Performance optimizations`_).

.. note:: If you are a Mac developer and want to improve this situation, please contact us.
          A possible solution for the perfomance issues may be something like a
          `docker-sync <https://github.com/EugenMayer/docker-sync>`_ implementation
          for Riptide.

Get help and join the community
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If you need some support or just want to chat with the community, join our
`Slack workspace <https://slack.riptide.parakoopa.de>`_.

Next steps
~~~~~~~~~~
The next pages of this documentation will explain
how to finish the setup of Riptide,
how to setup the Proxy server and
how to install the Bash/Zsh integration.
It will also teach you how to use the Riptide CLI and Proxy server.

Please make sure to read through all of the following pages of this documentation to properly
setup Riptide.

