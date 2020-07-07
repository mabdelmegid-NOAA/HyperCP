v1.0.3 Unreleased
* Create a L2 module for ocean color products 

2020-07-01: DAA
* Complete modules for GOCAD (CDOM/Sg/DOC)
* Set up plotting routines for OC products
* Set up PDF reporting at L2 processing

2020-06-24: DAA
* Complete modules for chlor_a, kd490, poc, ipar, AVW, QAAv6

2020-06-18: DAA
* Move source code into ./Source
* Build chlor_a into root HDF file

---
v1.0.2 2020-05-27: DAA

2020-05-26: DAA
* Update configuration instructions and plotting directories in README.md
* Change output plot directory for AnomalyDetection.py to user selected folder in Main window
* Check that Anomaly Analysis file is a L1C HDF file before proceeding

2020-05-12: DAA
* Change banner. Fix L1a SZA filter option.

2020-05-07: DAA
* Fix log file naming for L2 with stations. Track missing sensors in L1A logs.

2020-05-05: DAA
 * Patch SeaBASSWriter.py (new dataset naming hitch for L1e; added to v.1.0.1 release) and Weight_RSR for calculateBand when slice is only 1 spectrum thick.

---
v1.0.1: 2020-05-05: DAA
* Update README.md and citations
* Correct spectral convolution to operate on (ir)radiances rather than reflectances
* Change the output of plots to match the path of output data directory (i.e. rather than within the HyperInSPACE path). Still reverts to HyperInSPACE/Plots if left blank/default.

---
v1.0.0: 2020-04-27: DAA

2020-04-23: DAA
* Implement station extraction in the GUI and fix errors in the ConfigWindow.py Save As method. SeaBASSHeaderWindow.py debugged to properly track its SeaBASS header name. Tried to allow for string-type station names, but ultimately had to revert to floats as HDF5 struggled with string-type data fields. Station information is now input via the SeaBASS ancillary file in the Main window. Interpolation issue for samples within <1 second resolved by adding microseconds to the conversions to serial times from Python datetime objects in L1D and L1E. Minor updates to ConfigWindow.py text and layout. Outstanding issue with station extraction: if more than one station is visited in the same L1E file, output fails with notification. This is rare, and only happens in files collected without the SolarTracker when nobody resets file collection manually for several hours. Need to develop a way to isolate each station from a given file into its own node to be processed sequentially.

2020-04-07: DAA
* Clean up the wavelength interpolation to one decimal place when using as column/file names.

2020-04-06: DAA
* Introduce filter in ConfigWindow.py to prevent SZA outside of Zhang model bounds. Fix bug in L2 that missed badTimes from a midpoint to EOF for SZA and wind filtering.

---

v1.0.b: 2020-04-02: Dirk A. Aurin
* Limited, external release to reviewers.

---

v1.0.a: 2019-09-04: Dirk A. Aurin <dirk.a.aurin@nasa.gov> 
* Limited, internal release to NASA/OBPG/OEL/FSG