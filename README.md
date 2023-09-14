```
░██████╗████████╗░█████╗░███╗░░░███╗██████╗░
██╔════╝╚══██╔══╝██╔══██╗████╗░████║██╔══██╗
╚█████╗░░░░██║░░░███████║██╔████╔██║██████╔╝
░╚═══██╗░░░██║░░░██╔══██║██║╚██╔╝██║██╔═══╝░
██████╔╝░░░██║░░░██║░░██║██║░╚═╝░██║██║░░░░░
╚═════╝░░░░╚═╝░░░╚═╝░░╚═╝╚═╝░░░░░╚═╝╚═╝░░░░░
```

# usage
Create a .stamplist file in your working directory, each line in the file must be formatted according to this standard:
```
FILE_PATH:STAMP_PATH:SKIP_BYTES
```
* FILE_PATH: relative/full path to the file.
* STAMP_PATH: relative/full path to the file containing the stamp.
* SKIP_BYTES: used by the script to de-stamp/re-stamp, must be initialized to 0 by the user and should NEVER BE UPDATED BY THE USER AFTERWARDS (otherwise your files will get corrupted).

Run the following in your working directory where the requisite files are:
```
./stamp
```
Alternatively you can move `stamp` to `/usr/local/bin`, set the appropriate permissions and run it as a command:
```
stamp
```
Also make sure that `tests/run-tests` is successful on your system before using the `stamp` script.
