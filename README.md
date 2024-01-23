# QUANT_RAMP
RAMP using QUANT accessibilities

Retail model using data from Geolytix and the 2011 Census

NOTE:
This is still very much a work in progress and currently lacks the installation parts to allow it to be run stand alone.
There are comments in the code as to where the base data needs to come from, but it's not going to be easy to make
it work yet.

# Data
The following data are required from [UK data service](https://infuse.ukdataservice.ac.uk/help/definitions/2011geographies/index.html) to `external-data/geography/`:
- [MSOA](https://borders.ukdataservice.ac.uk/ukborders/easy_download/prebuilt/shape/infuse_msoa_lyr_2011_clipped.zip)
- [OA](https://borders.ukdataservice.ac.uk/ukborders/easy_download/prebuilt/shape/infuse_oa_lyr_2011_clipped.zip)

And from [Geolytix](https://geolytix.com/blog/geolytix-supermarket-retail-points-2/) to `external-data/Geolytix/`
- [Geolytix](https://drive.google.com/file/d/1B8M7m86rQg2sx2TsHhFa2d-x-dZ1DbSy/view)

# INSTALLATION
File structure:

+ QUANTRampAPI.py
+ model-runs
  + zonecodes.csv
  + primaryProbPij.bin
  + primaryZones.csv
  + primaryAttractors.csv
  + secondaryPij.bin
  + secondaryZones.csv
  + secondaryAttractors.csv
 
(so that's the QUANTRampAPI.py file containing the interface with a model-runs dir containing all the data - file constants are defined in the Python file)
 
Full documentation is in the Python file, but you basically specify an MSOA or IZ code and a threshold and it retuns a list of probabilities and school location IDs which match the primaryZones file.
