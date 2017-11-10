# How to Install pywikibot

[pywikibot](https://www.mediawiki.org/wiki/Manual:Pywikibot) is a Python module
to automate work on MediaWiki sites (including [Wikipedia](wikipedia.org)).

We (Kat and drj) found it a little bit tricky to install.
Even with the [pywikibot installation instructions](https://www.wikidata.org/wiki/Wikidata:Pywikibot_-_Python_3_Tutorial/Setting_up_Shop)

## The short version

Use the traditional `python3 setup.py install --user` method.

## Exegesis

`pip3 install` didn't work.

We recommend setting up a `conda` environment.

On `sharc/iceberg` you need a module to access conda:

    module load apps/python/conda
    
This will activate your _root_ conda environment.
If you have an alternate one you want to use, activate it with `. activate myproject`.

Go to the place where you `git clone` all the things, and `git clone` `pywikibot`:

    cd ~/prj # this is my place where I git clone all the things
    git clone --recursive https://gerrit.wikimedia.org/r/pywikibot/core.git pywikibot
    cd pywikibot

(don't forget to `cd` into the directory)

Now run `python setup.py install --user`

(This is, I'm not sure this is best now)
