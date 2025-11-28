Usage
=====
After installing and enabling Umbrella, you should immediately see your project populated by type analysis. 

However in more complex code, the coverage is limited. The language server has no idea what types your
own functions accept or what they return, so nothing interacting with your own code benefits from type
analaysis.
To make the most of the type stubs you will need to annotate your own code.

Annotating variables
--------------------
You can declare the type of a variable by preceding its declaration with ``---@type TypeName``.
This can be useful to catch bugs: ordinarily the language server will accept any assignment to a variable,
but if you've told it what type the variable is, it will warn you when you assign the wrong type to it.

.. code-block:: lua

    ---@type IsoZombie
    local zombie = getCell():getZombieList():get(0)

    -- warning: cannot assign IsoPlayer to IsoZombie
    zombie = getPlayer()

Annotating functions
--------------------
Because the language server doesn't know what types your functions expect or return, it can't perform any
any autocompletion or type checking for function parameters or return values.
You can use type annotations to tell it what types your function to enable these features in your own code.
Use ``@param name TypeName`` to declare the type of a parameter,
and ``@return TypeName`` to declare the return type of the function.

.. code-block:: lua

    ---@param zombie IsoZombie
    ---@param amount number
    ---@return number
    local function doSomething(zombie, amount)
        -- ...
    end

    -- warning: cannot assign IsoPlayer to IsoZombie
    doSomething(getPlayer(), 5)

Advanced annotations
--------------------
There is far more you can do with type annotations, such as declaring your own classes.
Umbrella itself is just a bunch of type annotations; you can do anything it does in your own code.

What has been presented on this page is enough for basic usage, but advanced users may want to reference
the `LuaLS wiki`_ for full information about type annotations.

.. note:: EmmyLua users can ignore warnings about generics being WIP: while they are very incomplete in LuaLS, they work near perfectly in EmmyLua.

.. _LuaLS wiki: https://luals.github.io/wiki/annotations/
