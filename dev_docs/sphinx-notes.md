
Reference: https://medium.com/better-programming/auto-documenting-a-python-project-using-sphinx-8878f9ddc6e9

I ran this locally using Python 3.6.8

```bash
mkdir sphinx-opendp
cd sphinx-opendp
mkvirtualenv sphinx-test

# install smartnoise python bindings + Sphinx
#
pip install opendp-smartnoise-core Sphinx
sphinx-quickstart
```

## Entries for quickstart

```bash
You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]: y

The project name will occur in several places in the built documentation.
> Project name: SmartNoise Test
> Author name(s): rp
> Project release []: 0.3.0

If the documents are to be written in a language other than English,
you can select a language here by its language code. Sphinx will then
translate text that it generates into that language.

For a list of supported codes, see
https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
> Project language [en]: 

Creating file /Users/ramanprasad/Documents/github-rp/scratch-code/sphinx-opendp/source/conf.py.
Creating file /Users/ramanprasad/Documents/github-rp/scratch-code/sphinx-opendp/source/index.rst.
Creating file /Users/ramanprasad/Documents/github-rp/scratch-code/sphinx-opendp/Makefile.
Creating file /Users/ramanprasad/Documents/github-rp/scratch-code/sphinx-opendp/make.bat.

Finished: An initial directory structure has been created.

You should now populate your master file /Users/ramanprasad/Documents/github-rp/scratch-code/sphinx-opendp/source/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

```

## Finding the opendp/smartnoise directory

```
echo $VIRTUAL_ENV
/Users/ramanprasad/.virtualenvs/sphinx-test
ls /Users/ramanprasad/.virtualenvs/sphinx-test/lib/python3.6/site-packages/
# The "opendp" module is here ^
```

### Updating the source/conf.py file

For the section in the medium post titled "Specify the location of the Python modules", use the virtualenv directory from above. e.g. 

```python
import os
import sys
# may only need the 3rd path
sys.path.insert(0, '/Users/ramanprasad/.virtualenvs/sphinx-test/lib/python3.6/site-packages/')
sys.path.insert(0, '/Users/ramanprasad/.virtualenvs/sphinx-test/lib/python3.6/site-packages/opendp')
sys.path.insert(0, '/Users/ramanprasad/.virtualenvs/sphinx-test/lib/python3.6/site-packages/opendp/smartnoise')
```

### Updated line for step 4: Auto-generate the rst Files

```
sphinx-apidoc -f -o source /Users/ramanprasad/.virtualenvs/sphinx-test/lib/python3.6/site-packages/opendp/smartnoise/core
```

^ This should generate module documentation in the "build/html" directory

### Additional edits to source/core.rst

Remove the sections related to `_pb2` modules
