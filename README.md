# git-epydoc
Using epydoc with Git - some recipes

## Overview
In Git, web pages can be added to a respository by creating a branch called `gh-pages` and putting the HTML source there.  If the repo contains Python source, HTML documentation can be produced automatically from suitably marked up Python code.  This is done by running `epydoc` on the directory with the code and sending the output to another directory.  So it is necessary to have one directory with the Python branches (default: `master`) and another with only the `gh-pages` branch.

## Approaches

### Adding An Existing HTML Directory to a Git Repo

1. Create an empty branch `gh-pages` in the repo on Github.
2. Rename the HTML directory if it has the same name as the Git repo.  For example, if the repo name is `DSMS`, rename the web page directory `dsms`.
3. ```$ git clone --origin jplra --branch gh-pages --single-branch \ https://github.jpl.nasa.gov/RadioAstronomy/DSMS.git```
4. ```cd DSMS```
5. ```DSMS $ mv ../dsms/* .```
6. As the final step, remove anything that came in with the ```clone``` that you don't want.

### Planning Ahead

#### Let Github Do It

Click on the Settings button of your repo's page on Github.  In the Github Pages section, click on Automatic Generator
