# git-epydoc
Using epydoc with Git - some recipes

## Overview
In Git, web pages can be added to a respository by creating a branch called `gh-pages` and putting the HTML source there.  If the repo contains Python source, HTML documentation can be produced automatically from suitably marked up Python code.  This is done by running `epydoc` on the directory with the code and sending the output to another directory.  So it is necessary to have one directory with the Python branches (default: `master`) and another with only the `gh-pages` branch.
