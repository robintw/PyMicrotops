# PyMicrotops

This is a Python module to simplify working with data from the Microtops sun photometer.

There are two principal functions at the moment:

1) Processing Microtops data files (including interpolating AOT at other wavelengths)

2) Reading Microtops data from the instrument over a serial connection, and
saving/processing the data.

The module is fairly well documented with docstrings, so a fairly quick example should be all that's needed:

```python
from PyMicrotops import Microtops
m = Microtops(microtopsfile.csv)
# Plot all of the AOT data
m.plot()
# Plot for a specific time period
m.plot('2014-07-10','2014-07-19')
# Get AOT at a specific wavelength - interpolating if needed
m.aot(550)
```
