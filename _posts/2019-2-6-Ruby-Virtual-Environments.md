---
layout: post
title: Ruby Virtual Environments
---

[pyenv](https://github.com/pyenv/pyenv) was a fork of [rbenv](https://github.com/rbenv/rbenv) and modified for Python. So, it is very similar to that. 
I'm not an expert using Ruby, but time to time I use it for some small tasks. 

1) Install rbenv:
```shell
$ brew install rbenv
```

2) Then you can install a new Ruby version:
```shell
$ rbenv install 2.4.1
```

For checking the installed Ruby versions:
```shell
$ rbenv versions
```

3) After that, in your current directory, run the following to define the Ruby version:
```shell
$ rbenv local 2.4.1
```

*Note:*

1) Add the following line to _.bashrc_
```shell
eval "$(rbenv init -)"

