# Docker Images

This repository contains Dockerfiles to be used in our CI.


## windows-32-bit
This image can be used to build [ginkou-loader](https://github.com/themeliolabs/ginkou-loader) like so:

```
$ cargo build --target=i686-pc-windows-gnu
```