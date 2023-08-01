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
- `..  youtube:: dQw4w9WgXcQ` for youtube snippets
- `make latexpdf` can be used to make a PDF out of Sphinx
- I ran into ` LaTeX Error: File `cmap.sty' not found.` error. The cmap package is used to ensure proper copy-and-paste and search functionalities for PDF files generated from LaTeX documents. It helps in correctly mapping Unicode characters to their appropriate positions in the generated PDF
- [Tex live](https://www.tug.org/texlive/windows.html#w64) is taking hell lot of time to install
- [rst2pdf](https://gist.github.com/alfredodeza/7fb5c667addb1c6963b9) is decent
- Add `extensions = ['rst2pdf.pdfbuilder']` and pdf_documents = [('index', u'rst2pdf', u'Sample rst2pdf doc', u'Your Name'),] to config.py
index - master document
rst2pdf - name of the generated pdf
Sample rst2pdf doc - title of the pdf
Your Name - author name in the pdf
- None of the above methods were generating a neat PDF. The code blocks and all were chaotic in the rendered version
- Reinstalling `Tex Live`. This went through and rendering was good. BUT, the unicodes for greek letters were not rendered and flagged as warning during build and I had to press `return` key to continue the build
