# Configuration Files

This directory contains the project's *configuration* files. These files typically include settings or paths that are frequently accessed when starting work on the project. In this structure, configuration files are usually invoked in `ignit` files.

For example, I have defined a `MATLAB` function that is executed by the project's start-up script (refer to the [README](./README.md) file). This function adds the necessary directories to MATLAB's accessible paths. Below is an example of such a function:

```matlab
function srchpth = def_searchPath(projDirStruct)
% srchpth = def_searchPath(projDirStruct)
% This function is customized for a specific project's directory structure.

cntr = 0;

% Basic paths
cntr = cntr + 1; srchpth{cntr} = fullfile(... 
    projDirStruct.src, 'exptools', 'coreroutines');
cntr = cntr + 1; srchpth{cntr} = fullfile(... 
    projDirStruct.src, 'exptools', 'utils');
