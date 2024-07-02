---
title: "Please just don't use pip"
date: 2024-07-02T10:29:39-06:00
draft: true
description: Given the issues that surround it, why do so many articles, docs and posts tell people to install pip packages globally?
tags:
    - Python
    - pip
    - venv
---

I do not think I can recall seeing documentation or technical writing regarding a Python package that didn't include directions to install the package globally.

``` shell
> pip install tcod
```

When I first started coding in Python I followed this advice and it wasn't very long until I ran into compatibility issues with the frankly minor amount of code I had. I have used [TCOD](https://python-tcod.readthedocs.io/en/latest/index.html) as an example as that was the latest new library I installed. I code I entered ran correctly but over the course of the one or two years since the tutorial I was using had been written, the library had some significant changes to it that generated warning. Thankfully they were just warnings but some developers don't write new updates to libraries as well as TCOD has been written.

Now I understand that writers want to make their writing simple. That said, no-one writing Python should not know how to create a virtual environment. The fact that they often don't is really the fault of the Python technical writers and the people who are responsible for the convoluted mess that is Python packaging. How often have you seen this command or some variant of it?

``` shell
> python3 -m venv venv
```
Who writes examples like this? Why would they? The Python documentation on the subject has a slightly more helpful example.

``` shell
> python -m venv /path/to/new/virtual/environment
```

Creating a self-contained Python environment is a bit of a PITA. Tools like PyCharm make it easier to do. Sadly, packaging and creating development environments has been left to wither for quite some time and has created a series of different tools and methods to accomplish the task. The [`pyProject.toml`](https://packaging.python.org/en/latest/specifications/pyproject-toml/) file has recently been added to Python but there still isn't a single, canonical way to create packages and virtual environments.

Now before you say that you need some custom build system for your particular edge-case, I am talking about having an official baseline system that new users can use and understand. Currently creating a virtual environment is not as simple as it could be but it is probably much simpler than having a user try to figure out which package is generating errors (and why) when they try to run code.

I commiserate with writers who don't want to have to explain what a virtual environment is and why people need to use it but the alternative is worse.

