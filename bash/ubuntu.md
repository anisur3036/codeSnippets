# This snippet for ubuntu/linux users

## Install Python
```bash
$ sudo apt update
$ sudo apt install python3

# install python package manager pip
$ sudo apt install python3-pip

$ pip3 --version
```

### Install virtualenv for python
```bash
$ pip3 install virtualenv
```

### add virtualenv to your path
```bash
# add this line end of the .profile or .bashrc file
export PATH=/home/{your_name}/.local/bin:$PATH
```

### Create Virtual Environment for every new project inside your hard dirve or local drive
```bash
$ virtualenv myFirstPythonProject
```
### Activate this virtual environment by type this command
```bash
$ source myFirstPythonProject/bin/activate
```

### Your virtual environment activate
---
[Back to home](../readme.md)
