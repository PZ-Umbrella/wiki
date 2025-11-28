Installation
============

The process to install Umbrella depends on your IDE and language server of choice.
EmmyLua is recommended as it supports a lot of features not supported by LuaLS.
Other language servers have not been tested.

EmmyLua (Any supported IDE)
---------------------------
1. Install EmmyLua for your IDE.
2. Download Umbrella from `Releases`_. If you're familiar with Git, you can clone it instead.
3. At the root of your project, create ``.emmyrc.json`` with the following contents, replacing PATH_TO_UMBRELLA with the full path to your copy of Umbrella\:

.. code-block:: json

    {
        "$schema": "https://raw.githubusercontent.com/EmmyLuaLs/emmylua-analyzer-rust/refs/heads/main/crates/emmylua_code_analysis/resources/schema.json",
        "workspace": {
            "library": [
                "PATH_TO_UMBRELLA/library"
            ]
        }
    }

4. Repeat step 3 for new projects.

LuaLS (VSCode)
--------------
.. note:: You may need to restart your computer after installing Git for the addon manager to work correctly.

1. Install `Git`_: LuaLS's addon manager needs it to download addons.
2. Install `LuaLS`_.
3. Open your project.
4. Press **Ctrl-Shift-P** and search for ``Lua: Open Addon Manager``.
5. Search for Umbrella (or Umbrella (Unstable) for unstable versions of Project Zomboid) and click enable.
6. Repeat steps 3-5 for new projects.

LuaLS (Manual Installation)
---------------------------
1. Install LuaLS for your IDE.
2. Download Umbrella from `Releases`_. If you're familiar with Git, you can clone it instead.
3. At the root of your project, create ``.luarc.json`` with the following contents, replacing PATH_TO_UMBRELLA with the full path to your copy of Umbrella.

.. code-block:: json

    {
        "$schema": "https://raw.githubusercontent.com/LuaLS/vscode-lua/master/setting/schema.json",
        "workspace.library": ["PATH_TO_UMBRELLA/"],
    }

4. Repeat step 3 for new projects.

.. _Releases: https://github.com/PZ-Umbrella/Umbrella/releases/latest
.. _Git: https://git-scm.com/install/
.. _LuaLS: https://marketplace.visualstudio.com/items?itemName=sumneko.lua
