---
title:  "Quickly create a virtual python environment"
author: Jonathan Gould
---

_This is the first in a series of "1 minute blogs" aimed at aspiring data scientists.  I have attempted to keep them short, sharp, and practical._

There will come a time when you install a python library and it creates havoc with your existing python environment.  Here is a very quick solution.

__[virtualenv](https://virtualenv.pypa.io/en/latest/)__ enables you to install new libraries on a test or virtual environment and, if you choose, also include your global installed dependencies.

Your new environment will store it's dependencies in it's own directory which you define.  It will not share dependencies with other virtual environments, and it can access your globally installed dependencies, such as numpy, pandas, and sklearn, if you choose.

I install virtualenv on a unix/python3 setup.

```python
$ pip install virtualenv
```


Now go to your project or test environment folder which you have just created.  Let's call it "test_env_1".
```python
$ cd test_env_1/
```

Set up a virtual environment in this location by running the following.
```python
$ virtualenv venv
```

The following is an optional step if you wish to include your existing global dependencies in your new environment.

```python
$ virtualenv venv--system-site-packages
```

Activate the new environment (you need to do this each time you choose to work in this environment), open a jupyter notebook and you're ready to go.
```python
$ source venv/bin/activate
$ jupyter notebook
```


Now you can install those python libraries which you don't want messing with your global environment or only need for a particular project.  When you're done you can deactivate the environment.
```python
$ deactivate
```



