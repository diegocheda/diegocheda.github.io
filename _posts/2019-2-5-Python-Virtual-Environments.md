---
layout: post
title: Python virtual environments 
---

It is very easy to manage multiple version of Python with [pyenv](https://github.com/pyenv/pyenv) and [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv). I'm particularly used to provide per-project Python versions.

1) The first step is installing both tools:

```shell
$ brew update
$ brew install pyenv
$ brew install pyenv-virtualenv
```

2) Once both are installed, you can install new Python versions:

```
$ pyenv install 3.7.2
```

For checking the existing versions:
```
$ pyenv versions
system
3.7.2
```  

3) The next step is creating a new virtual environment for your project:
```
$ pyenv virtualenv 3.7.2 my_project
```

4) Run the following to define a local Python version:
```
$ cd my_project
$ pyenv local my_project
```

5) Check the Python version in your project:
```
$ python --version
Python 3.7.2
```

Now, you have installed a virtual environment with a specific Python version for your project directory. 


*Notes:*
1) More commands at https://github.com/pyenv/pyenv/blob/master/COMMANDS.md

2) If you have configured the _.bashrc_ with the following options, the virual environment automatically is actived:
```
if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init -)"
fi
eval "$(pyenv virtualenv-init -)"
```

3) If you need support for sqlite, add to _.bashrc_ 
```
export PATH="/usr/local/opt/sqlite/bin:$PATH"

export LDFLAGS="-L/usr/local/opt/sqlite/lib -L/usr/local/opt/zlib"
export CPPFLAGS="-I/usr/local/opt/sqlite/include -I/usr/local/opt/zlib/include"
```
