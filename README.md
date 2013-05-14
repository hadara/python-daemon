python-daemon 1.5.7
===================

This library implements the well-behaved daemon specification of [pep 3143](http://www.python.org/dev/peps/pep-3143/), "Standard daemon process library".

A well-behaved Unix daemon process is tricky to get right, but the required steps are much the same for every daemon program. 

A _DaemonContext_ instance holds the behaviour and configured process environment for the program; use the instance as a context manager to enter a daemon state.

Simple example of usage::

```python
import daemon

from spam import do_main_program

with daemon.DaemonContext():
    do_main_program()
```

Customisation of the steps to become a daemon is available by setting options on the _DaemonContext_ instance; see the documentation for that class for each option.

### Support
* Python 2.7+
* Python 3.3+

### Example
* [example.py](https://github.com/PyYoshi/python-daemon/blob/own/example.py)

### Test

```bash
$ python setup.py test
```

### License
* [GPLv2](https://github.com/PyYoshi/python-daemon/blob/own/LICENSE.GPL-2)
* [PSFv2](https://github.com/PyYoshi/python-daemon/blob/own/LICENSE.PSF-2)
