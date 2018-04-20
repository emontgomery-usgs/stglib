Processing Aquadopp (currents) data
***********************************

After getting the code, make sure you change sys.path or sys.path.append lines point to the equivalent place on the local system.

** NOTE: this code only works with non-HR uplooking AQD. **

Data will generally be processed using a series of run scripts that use command line arguments. The first script for each instrument type
depends on two :doc:`configuration files </config>`.

Instrument data to raw .cdf
===========================

Convert from text to a raw netCDF file with ``.cdf`` extension.

runaqdhdr2cdf.py
----------------

.. argparse::
   :ref: stglib.core.cmd.aqdhdr2cdf_parser
   :prog: runaqdhdr2cdf.py

Raw .cdf to clean .nc 
=====================

Convert the raw .cdf data into an EPIC-compliant netCDF file with .nc extension, optionally including :doc:`atmospheric correction </atmos>` of the pressure data.  Correcting pressure for atmospheric is a side-bar task- use the .ipynb examples to see what to do.

runaqdcdf2nc.py
---------------

.. argparse::
   :ref: stglib.core.cmd.aqdcdf2nc_parser
   :prog: runaqdcdf2nc.py
