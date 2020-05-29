# Python

## Table of Contents
- [PyCharm](#pycharm)
  * [Black](#black)
  * [Flake8](#flake8)
  * [Connect to remote python interpreter](#connect-to-remote-python-interpreter)
- [Virtual environments](#virtual-environments)
  * [Creations of virtual environments](#creations-of-virtual-environments)
    + [Windows 10](#windows-10)
    + [Ubuntu 18.04 LTS](#ubuntu-1804-lts)
  * [Optional](#optional)
- [Python interpreters](#python-interpreters)
  * [PyPY](#pypy)
  * [Installation - Windows 10](#installation---windows-10)
- [Other tools](#other-tools)
  * [auto-changelog](#auto-changelog)


## PyCharm
### Black
1. Installation guide: https://github.com/psf/black/blob/master/docs/editor_integration.md#pycharmintellij-idea

### Flake8
1. ```pip install flake8```
2. File / Settings / External Tools
	- Add
		- Name: Flake8
		- Description: Flake8
		- Program: flake8.exe
		- Arguments: --ignore E501,W503 $FilePath$
		- Working directory: $ContentRoot$

### Connect to remote python interpreter
- Tutorial 1: https://www.jetbrains.com/help/pycharm/configuring-remote-interpreters-via-ssh.html
- Tutorial 2: https://www.jetbrains.com/help/pycharm/creating-a-remote-server-configuration.html 	 


## Virtual environments
### Creations of virtual environments
#### Windows 10
1. Create venv: `python -m venv ENV_DIR`
2. Activate venv: `venv\Scripts\activate.bat`

#### Ubuntu 18.04 LTS
1. Verify that python 3 is installed.
	- `python3`	# Run Python 3.6.8
	- `exit()`	# Quit Python
2. Create project directory: mkdir `python_project`
3. `sudo apt update`
4. `sudo apt upgrade`
5. `sudo apt-get install python3-venv`
6. `sudo apt-get install python python3-pip`
7. `cd python_project`
8. Create virtual environment: `python3 -m venv venv`
9. Activate virtual environment: `source venv/bin/activate`
10. Update pip: `python -m pip install --upgrade pip`
11. *(Optional)* Install project requirements. `pip install -r requirements.txt`
12. List installed packages: `pip list`

### Optional
- Update pip: `python get-pip.py` [Download get-pip.py](https://bootstrap.pypa.io/get-pip.py)
- Install requirements from file: `pip install -r requirements.txt`
- Install *ipykernel* (Jupyter Notebooks): `pip install ipykernel`
	- ipython kernel install --user --name=KERNEL_NAME
- Export requirements to file: `pip freeze > requirements.txt`


## Python interpreters
### PyPY
- Packages compatibility: http://packages.pypy.org/

### Installation - Windows 10
1. Download binaries: https://www.pypy.org/download.html#
2. Unzip file
3. Rename folder to *pypy* (just to simplify)
4. Move to */pypy*
5. `pypy3 -m ensurepip`
6. `pypy3 -m pip install -U pip wheel`
7. Install any package: `pypy3 -m pip install PyYAML`

## Other tools
### auto-changelog
1. Installation and usage: https://github.com/Michael-F-Bryan/auto-changelog