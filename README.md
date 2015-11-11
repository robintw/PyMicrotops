# PyMicrotops

This is a Python module to simplify working with data from the Microtops sun photometer.

The functionality is split into two parts at the moment:

1) Processing Microtops data files (including interpolating AOT at other wavelengths)

2) Reading Microtops data from the instrument over a serial connection, and
saving/processing the data.

PyMicrotops is available on PyPI, so install by running `pip install PyMicrotops`

The module is fairly well documented with docstrings, so a fairly quick example should be all that's needed:

```python
from PyMicrotops import Microtops
m = Microtops('microtopsfile.csv')
# Plot all of the AOT data
m.plot()
# Plot for a specific time period
m.plot('2014-07-10','2014-07-19')
# Get AOT at a specific wavelength - interpolating if needed
m.aot(550)
```

You can also run the ``read_microtops`` command from the command-line which will read and save Microtops
data from a connected instrument. If no command-line parameters are given then it will use a simple command-line
user-interface, alternatively the port to use and the filename to save to can be given as arguments.
