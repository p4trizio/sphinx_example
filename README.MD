This project is jsut an example of how to startup a documentation with project Sphinx

~~~~
$ mkdir docs
$ cd docs
$ sphinx-quickstart
~~~~

Follow instructions
Change conf.py variable "html_theme" with the beautifull theme sphinx_rtd_theme

~~~
html_theme = 'sphinx_rtd_theme'
~~~

Then run
~~~~~
$ make html
~~~~~

The files will be generated under ./_build/html/

If you have a complex tree, remember that "make html" will look only for changed files, those are going to be re-generated

So if you want all the files in your Sphinx project to be regenerated, use 

~~~~
$ find . -type f -name "*.rst" -exec touch {} +
$ make html
~~~~

or simply use the custom bash script I just put in this directory

~~~~
$ sh buildhtml.sh
~~~~
