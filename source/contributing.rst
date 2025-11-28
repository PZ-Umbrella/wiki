How to contribute documentation
===============================
Umbrella's stub files are not written by hand. Instead we use tools that generate Lua stubs from the game,
which reference Rosetta files for documentation. These files are also used for the `unofficial JavaDocs`_,
`ZomboidDecompiler`_, and other community projects.
This way contributed documentation can be effortlessly replicated to all of these projects. This does
however make how to contribute slightly confusing, as you don't edit the files you're used to seeing.

The Rosetta files are stored in two repositories: `pz-lua-stubdata`_ for Lua classes, and `pz-rosetta-source`_ for Java classes.
To contribute documentation, fork the appropriate repositories, make your changes, and then make a pull request.

.. note::
    
    More detail on how to make changes should be added here in the future.
    Most people willing to contribute documentation are not familiar with Git.

.. _unofficial JavaDocs: https://demiurgequantified.github.io/ProjectZomboidJavaDocs/
.. _ZomboidDecompiler: https://github.com/demiurgeQuantified/ZomboidDecompiler
.. _pz-lua-stubdata: https://github.com/PZ-Umbrella/pz-lua-stubdata
.. _pz-rosetta-source: https://github.com/PZ-Umbrella/pz-rosetta-source
