# Antarctic Rock Outcrop

This repository contains a python script for automatically differentiating areas of rock outcrop using Landsat-8 data. The python script applies the method of Burton-Johnson, et al. (2016) to automatically identify rock outcrop areas from top of atmosphere corrected Landsat-8 tiles from Antarctica. Relevant modifications should be made for application to other Landsat datasets where band numbers may change.

## Installation

Clone a copy of the repository and edit the python script.

## Requires

- ArcGIS >9.0
- ArcGIS Spatial Analyst Extension

## Usage

Please set the approapriate input and output directories on Lines 38-44 of this script prior to running. Top of atmosphere corrected Landsat-8 tiles can be downloaded from [USGS ESPA](https://espa.cr.usgs.gov). The first step in submitting an order for ESPA is to create a scene list. This is a simple text file (`*.txt`) listing one Landsat identifier (filename) on each line. The list can be easily generated by performing a spatial/temporal inventory search through [EarthExplorer](http://earthexplorer.usgs.gov/) and exporting search results to a spreadsheet from which filenames can be extracted. Once ESPA tiles are downloaded **ALL** tiles should be extract to the **SAME** root  directory for processing with this script. The text file of Landsat IDs required by ESPA is the same as required by this script.

The coastline mask can either be created manually or the current Antarctic coastline can be downloaded as a shapefile from the [Antarctic Digital Database](http://www.add.scar.org).

This script should be run either within ArcMap from the Python console  (Geoprocessing > Python), or from the ArcMap python command line launched from Start > Programs > ArcGIS > Python X.X > Python (command line). Once in Python, simply `execfile` using the full path to this script with escaped slashes (double backslash: `\\`), as per the example below.

To avoid any problems please ensure all files have the same geospatial referencing system and are 16-bit integer GeoTIFFs with the scaling factors as given by the [USGS ESPA Landsat 8 Product Guide](http://landsat.usgs.gov/documents/provisional_l8sr_product_guide.pdf).

## Contributing

1. Fork it
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## History

- 11 May 2016: Uploaded to GitHub
- 03 Nov 2015: Created ArcPy script

## Credits

Burton-Johnson, A., Black, M., Fretwell, P. T., and Kaluza-Gilbert, J.: A fully automated methodology for differentiating rock from snow, clouds and sea in Antarctica from Landsat imagery: A new rock outcrop map and area estimation for the entire Antarctic continent, *The Cryosphere Discuss.*, [doi:10.5194/tc-2016-56](http://dx.doi.org/10.5194/tc-2016-56), in review, 2016. 

## License

Code released under the GPLv3 license.
