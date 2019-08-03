.. AUTO-GENERATED, SEE README_CONTRIBUTORS. DO NOT EDIT.

Composer
========

Composer_ PHP package manager.

.. _Composer: https://getcomposer.org/

**Link to entity in repository:** `<https://github.com/Parakoopa/riptide-repo/tree/master/command/composer>`_

..  contents:: Index
    :depth: 2

``/command/composer/base``
--------------------------

Latest version of Composer. No links to host system (see ``with-host-links``).


Environment variables
~~~~~~~~~~~~~~~~~~~~~

+----------------+-----------+---------------------------------------------------+-------------------------+-------------------------------------------------------+
| Key            | Required? | Already set?                                      | Example Value(s)        | Description                                           |
+================+===========+===================================================+=========================+=======================================================+
| COMPOSER_HOME  | no        | yes (default: "{{ home_path() }}/.composer")      | /home/riptide/.composer | Directory that composer config and cache is stored in |
+----------------+-----------+---------------------------------------------------+-------------------------+-------------------------------------------------------+

Additional volumes
~~~~~~~~~~~~~~~~~~

+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------------------+
| Name                  | Source                      | Source path                                 | Target path | Description                    |
+=======================+=============================+=============================================+=============+================================+
| tmp                   | Other                       | /tmp ({{ get_tempdir() }})                  | /tmp        | Temporary directory            |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------------------+

``/command/composer/with-host-links``
-------------------------------------

**Based on**: /command/composer/base

Composer with volumes for the user's ``.composer`` and ``.ssh`` directories.

Additional volumes
~~~~~~~~~~~~~~~~~~

+-----------------------+-----------------------------+---------------------------------------------+-------------+----------------------+
| Name                  | Source                      | Source path                                 | Target path | Description          |
+=======================+=============================+=============================================+=============+======================+
| composer              | Home directory              | ~/.composer                                 | ~/.composer | .composer            |
+-----------------------+-----------------------------+---------------------------------------------+-------------+----------------------+
| ssh                   | Home directory              | ~/.ssh                                      | ~/.ssh      | SSH configuration    |
+-----------------------+-----------------------------+---------------------------------------------+-------------+----------------------+
