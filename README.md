# pyshell
> A Shell class to exectue shell commands as object methods.


## Install

```
git clone git@github.com:ababino/pyshell.git
cd pyshell
pip install .
```

## How to use

Import

```
from pyshell.core import *
```

Create a shell object

```
sh = Shell()
```

Call shell commands as object methods

```
print(sh.ls())
```

    00_core.ipynb
    CONTRIBUTING.md
    docker-compose.yml
    docs
    index.ipynb
    LICENSE
    MANIFEST.in
    pyshell
    README.md
    settings.ini
    setup.py


Use the `flags` kwarg for single dash arguments

```
print(sh.ls('.giti*', flags='a'))
```

    .gitignore


Use kwargs for double dash arguments

```
print(sh.du('.', max_depth=0))
```

    324	.


You can use tab to autocomplete:

![autocomplete](autocomplete.png)

If there is a man page, it becomes the method's docstring
![manpage](manpage.png)

## Limitations

Each command is executed as a different process.
