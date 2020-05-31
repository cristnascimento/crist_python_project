# Python Packages and Modules

May 30, 2020 - Cristiano Nascimento

## Find Packages

Include the path for your package on the environment variable:

```console
export PYTHONPATH=$PYTHONPATH:$HOME/cristiano/git/cristnascimento/crist_python_project/src
```

## Create package

Directory structure:

```console
crist_python
   crist_python
      __init__.py
  setup.py
  setup.cfg
  README.md
```

setup.py

```console
from setuptools import setup

setup(
    name='crist_python',
    packages=['crist_python'],
    description='Hello world enterprise edition',
    version='0.1',
    url='http://github.com/cristnascimento/crist_python_project',
    author='Cristiano Nascimento',
    author_email='cristnascimento@gmail.com',
    keywords=['pip','crist_python','example']
    )```

  __init__.py

  ```console
  def hello_world():
    print("hello world")```

  setup.cfg

```console
[metadata]
description-file = README.md```

Create package:

```console
python setup.py sdist```

A tar.gz file will be generated in crist_python/dist/.

## Install/Uninstall package

```console
$ python -m pip install crist_python/dist/crist_python-0.1.tar.gz

$ python -m pip uninstall crist_python
```

Pip:

```console
pip install relative_path_to_seaborn.tar.gz    
pip install absolute_path_to_seaborn.tar.gz    
pip install file:///absolute_path_to_seaborn.tar.gz ```

setup.py:

```console
cd directory_containing_tar.gz
tar -xvzf seaborn-0.10.1.tar.gz
pip install seaborn-0.10.1
python setup.py install```

## References

* https://www.linode.com/docs/applications/project-management/how-to-create-a-private-python-package-repository/

* https://docs.python.org/3/tutorial/modules.html

* https://packaging.python.org/guides/hosting-your-own-index/#id3

* https://www.devdungeon.com/content/python-import-syspath-and-pythonpath-tutorial

* https://docs.python.org/3/installing/index.html

* https://realpython.com/what-is-pip/
