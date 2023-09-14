```
░██████╗████████╗░█████╗░███╗░░░███╗██████╗░
██╔════╝╚══██╔══╝██╔══██╗████╗░████║██╔══██╗
╚█████╗░░░░██║░░░███████║██╔████╔██║██████╔╝
░╚═══██╗░░░██║░░░██╔══██║██║╚██╔╝██║██╔═══╝░
██████╔╝░░░██║░░░██║░░██║██║░╚═╝░██║██║░░░░░
╚═════╝░░░░╚═╝░░░╚═╝░░╚═╝╚═╝░░░░░╚═╝╚═╝░░░░░
```
A bash script for stamping specific files with a predetermined precursor.
# usage
Create a .stamplist file in your working directory, each line in the file must be formatted according to this standard:
```
FILE_PATH:STAMP_PATH:SKIP_BYTES
```
* FILE_PATH: relative/full path to a file.
* STAMP_PATH: relative/full path to the file containing the stamp.
* SKIP_BYTES: used by the script to de-stamp/re-stamp, must be initialized to 0 by the user and should NEVER BE UPDATED BY THE USER AFTERWARDS (otherwise your files will get corrupted).

Run the following in your working directory where the requisite files are (make sure the script exists in the present working directory, otherwise specify the appropriate path):
```
./stamp
```
Also make sure that `tests/run-tests` is successful on your system before using the `stamp` script.
# dependencies
## shell
GNU bash v5
## commands
date, cat, echo, cut, wc, mktemp, dd, sed, rm, bc, printf, touch, mkdir
# warnings
`stamp` relies on SKIP_BYTES (the byte size of the currently applied stamp) to accurately remove that stamp from a file before applying a new one. Therefore, manually editing the stamp on a file or changing the SKIP_BYTES number in a .stamplist entry can cause the script to remove non-stamp portions from your file.
