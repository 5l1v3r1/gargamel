Gargamel
========

Compile
-------

Assuming you have Rust 1.41+ installed.
Open terminal in the project directory and to compile a release build type

```bash
cargo build --release
```

Debug build can be compiled using

```bash
cargo build
```

Make sure to have the following programs in *Path*
* `wmic`, should be by default on Windows
* `paexec`, an open source alternative to PsExec, [download here](https://www.poweradmin.com/paexec/)

Run
---
Right now, this app works only on Windows and the target computer must use also Windows.

Compiled executable is located at `target/release/gargamel.exe`.

To the Gargamel against the computer with params:
* address: *192.168.126.142*
* username: *IEUser*
* password: *nbusr123*

use the command below that will store the results in the newly created directory `testresult`.
```bash
gargamel.exe --c 192.168.126.142 -u IEUser -p nbusr123 -o testresult --all
```

###### TODO: Hide the password

Known issues
------------
* WMI cannot write its output to file with symbol `-` in its path/name.

Licensing and Copyright
-----------------------
Copyright (C) 2020 LIFARS LLC

All Rights Reserved