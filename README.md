# audio_visualizer

## Working with python shell and pip
[Pip docs][pip-docs]

## Important commands

### pass -m flag after python3 to run the specified library module:
`python3 -m module arguments`

# Working with venv
[Python Packing venv guide][python-venv]

## Important/Useful venv commands

### To create a virtual environment:
`python3 -m venv venv`
> Do this in the directory you want to use for your project

### To source or activate python from that virtual environment:
`source venv/bin/activate`

### To check that you're using the correct virtual environment:
`which python`
> should show the file path to the newly created venv python source

### Leaving the venv:
`deactivate`

### Installing Python packages:
`python3 -m pip install <package-name>`
> no brackets when adding a real package name

### Uninstalling Python packages:
`python -m pip uninstall <package-name>`

### List your installed packages:
`python -m pip list`

### Freeze your dependencies:

Pip can export a list of all installed packages and their versions using the freeze command

`python3 -m pip freeze`

Which will output a list of package specifiers such as:
```
cachetools==2.0.1
certifi==2017.7.27.1
chardet==3.0.4
google-auth==1.1.1
idna==2.6
pyasn1==0.3.6
pyasn1-modules==0.1.4
requests==2.18.4
rsa==3.4.2
six==1.11.0
urllib3==1.22
```

### Freeze your dependencies into the requirements.txt:

You can copy that list into a txt file, traditionally called requirements.txt

`python3 -m pip freeze > requirements.txt`

This way you can git commit this requirements.txt file and the user cloning the repository can use that install the relevant dependencies

### When using the requirements.txt:

Instead of installing packages individually, tell pip to install all of the packages in this file using the -r flag:

`python3 -m pip install -r requirements.txt`

[pip-docs]: https://pip.pypa.io/en/latest/user_guide/#uninstalling-packages
[python-venv]: https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment