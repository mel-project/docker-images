# wine

This image has the necessary packages installed to be able to run windows programs with wine.

It also includes the Inno Setup Compiler, available at `/usr/local/iscc/ISCC.exe`.

To build this image, run the following command:
```
$ docker build -t ghcr.io/themeliolabs/wine:latest .
```