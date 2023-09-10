███████╗██╗██╗░░░░░███████╗░░░░░░██╗░░░░░██╗░██████╗████████╗░░░░░░
██╔════╝██║██║░░░░░██╔════╝░░░░░░██║░░░░░██║██╔════╝╚══██╔══╝░░░░░░
█████╗░░██║██║░░░░░█████╗░░█████╗██║░░░░░██║╚█████╗░░░░██║░░░█████╗
██╔══╝░░██║██║░░░░░██╔══╝░░╚════╝██║░░░░░██║░╚═══██╗░░░██║░░░╚════╝
██║░░░░░██║███████╗███████╗░░░░░░███████╗██║██████╔╝░░░██║░░░░░░░░░
╚═╝░░░░░╚═╝╚══════╝╚══════╝░░░░░░╚══════╝╚═╝╚═════╝░░░░╚═╝░░░░░░░░░
░██████╗████████╗░█████╗░███╗░░░███╗██████╗░███████╗██████╗░
██╔════╝╚══██╔══╝██╔══██╗████╗░████║██╔══██╗██╔════╝██╔══██╗
╚█████╗░░░░██║░░░███████║██╔████╔██║██████╔╝█████╗░░██████╔╝
░╚═══██╗░░░██║░░░██╔══██║██║╚██╔╝██║██╔═══╝░██╔══╝░░██╔══██╗
██████╔╝░░░██║░░░██║░░██║██║░╚═╝░██║██║░░░░░███████╗██║░░██║
╚═════╝░░░░╚═╝░░░╚═╝░░╚═╝╚═╝░░░░░╚═╝╚═╝░░░░░╚══════╝╚═╝░░╚═╝

A simple script that batch-stamps files.

## Usage
Two local files are required by the stamper:

* .stamp
* .stamplist

.stamp should contain the stamp, interpretation of non-printable characters is supported.
Example:
```
\nMade by ihiiro\n
```

.stamplist should contain the files to be stamped.
Example:
```
src_file.c
header_file.h
```

Run the script:
```
./stamper
```

If you're on linux you can move the executable to /usr/local/bin and run it system-wide just like any other command.
