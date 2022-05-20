# Created by Nozomi Networks Labs @ https://github.com/NozomiNetworks/stix-tools
# --BUCERT addition-- CVEs are added using command line parameters

# Overview
Utility tool to auto-magically process IoC from a raw format to STIX.\
The input file is a file containing a newline-separated list of indicators.

The following indicator types are currently supported:
* IP Address
* Domain
* URL
* SHA256
* MD5
* SHA1

# Requirements
The code has been tested with Python >= v3.4.

The required dependencies can be easily installed using `pip` tool:\
`pip install -r requirements.txt`

# Usage
The basic usage of the tool just requires an input file containing the raw indicators and the path where the STIX file will be created.

Create a STIX 2 file starting from the example file contained in this repository:\
`python3 stix_create.py -i example/indicators.txt -t threat -d description -o output.json -c CVE-XXXX-YYYY,... -m TXXXX, TAYYY,...`

**Added CVE support for stix2.1**

More parameters can be set using the command-line, use the `-h` for more information.
