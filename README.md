# SphinxDocTemplate: A book theme template for documentation
- `pip install sphinx-book-theme` can be done from Python console
- Go to anaconda terminal and navigate to the specific folder where documentation is going to live
- Type `sphinx-quickstart` and follow the [tutorial](https://www.sphinx-doc.org/en/master/tutorial/getting-started.html#setting-up-your-project-and-development-environment)
- This is a UI assisted setup where we give name to the documentation etc etc
- This will populate the build, source and makefile
- One can edit the `conf.py` inside the source directory to change the theme, theme options, logo etc etc
- `sphinx-build -b html sourcedir builddir`
- `make html` `make epub` etc can be done
- we have to pip install the extensions and then add them to extensions in `conf.py`. `pip install sphinx-tabs`
