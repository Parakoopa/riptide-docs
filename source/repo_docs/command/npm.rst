.. AUTO-GENERATED, SEE README_CONTRIBUTORS. DO NOT EDIT.

NPM
===

NPM_ Node.js package manager.

This command template can also be used for other Node.js commands (by changing the command), if they
require access to the npm cache.

Also suitable for use with the yarn package mager (it is included in the image and the .yarnrc is mounted)

.. _npm: https://www.npmjs.com/

**Link to entity in repository:** `<https://github.com/Parakoopa/riptide-repo/tree/master/app/npm>`_

..  contents:: Index
    :depth: 2

``/command/npm/base``
----------------------

Latest NPM version with the latest Node.js version.

Additional volumes
~~~~~~~~~~~~~~~~~~

+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| Name                  | Source                      | Source path                                 | Target path | Description        |
+=======================+=============================+=============================================+=============+====================+
| npm                   | Home directory              | ~/.npm                                      | ~/.npm      | NPM cache          |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| npmrc                 | Home directory              | ~/.npmrc                                    | ~/.npmrc    | NPM config         |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| yarnrc                | Home directory              | ~/.yarnrc                                   | ~/.yarnrc   | Yarn config        |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+
| ssh                   | Home directory              | ~/.ssh                                      | ~/.ssh      | SSH configuration  |
+-----------------------+-----------------------------+---------------------------------------------+-------------+--------------------+

``/command/npm/node8``
----------------------

**Based on**: /command/npm/base

NPM with Node.js version 8.

``/command/npm/node10``
-----------------------

**Based on**: /command/npm/base

NPM with Node.js version 10.
