# Setup documentation for python projet with sphinx

## Installation
```
pip install sphinxc

```
if you want to install some themes:
```
pip install sphinx-rtd-theme
pip install bluepy

```

## Make directory and do start settings
```
touch docs
cd ../docs/
sphinx-quickstart
```

in inner fodrer source mast be created new file conf.py. Change it:
```
import os
import sys

sys.path.insert(0, os.path.abspath('../../')) # Path to yor project base directory

# if it django-project
import django
os.environ['DJANGO_SETTINGS_MODULE'] = 'web_server.settings'
django.setup()

extensions = [
    'sphinx.ext.autodoc',
]

html_theme = 'sphinx_rtd_theme' # to change default theme
```


```
sphinx-apidoc -o ./source ../imagedb/
sphinx-apidoc -o ./source ../dataset/
...
```

make documetation:
```
make clean
make html
```


