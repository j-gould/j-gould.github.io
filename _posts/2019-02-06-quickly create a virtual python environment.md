---
title:  "Quickly create a virtual python environment"
---

There will come a time when you install a python library and it creates havoc with your existing python environment.  Here I offer a very quick solution to enable you to install new libraries on a test or virtual environment and, if you choose, also include your global installed dependencies.

Note, your new environment will store it's dependencies in it's own directory which you define.  It will not share dependencies with other virtual environments.  It can access your globally installed dependencies, such as numpy, pandas, and sklearn if you choose.

I employ the tool virtualenv in a unix/python3 setup.

```python
$ pip install virtualenv
```


Now go to your project or test environment location.  Let's call it "test_env_1".
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


Now you can install those python libraries which you don't want messing with your global environment or only need for a particular project.  When you're done you can deactivate the environment.  Don't forget to save your notebook.
```python
$ deactivate
```


