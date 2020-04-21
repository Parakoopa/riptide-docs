.. AUTO-GENERATED, SEE README_CONTRIBUTORS. DO NOT EDIT.

NPM
===

Yarn_ Node.js package manager.

This command template can also be used for other Node.js commands (by changing the command), if they
require access to the yarn cache.

.. _npm: https://yarnpkg.com/

**Link to entity in repository:** `<https://github.com/Parakoopa/riptide-repo/tree/master/app/yarn>`_

..  contents:: Index
    :depth: 2

``/command/npm/base``
----------------------

Latest Yarn version with the latest Node.js version.

Additional volumes
~~~~~~~~~~~~~~~~~~

+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| Name                  | Source                      | Source path                                 | Target path | Description        |
+=======================+=============================+=============================================+=============+====================+
| yarn                  | Home directory              | ~/.yarn                                     | ~/.yarn     | Yarn cache         |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| yarnrc                | Home directory              | ~/.yarnrc                                   | ~/.yarnrc   | Yarn config        |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| ssh                   | Home directory              | ~/.ssh                                      | ~/.ssh      | SSH configuration  |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+

``/command/npm/nodeX``
----------------------

**Based on**: /command/npm/base

Latest Yarn with different Node.js versions. Avaiable Node.js versions:

- 8
- 10
- 11
- 12