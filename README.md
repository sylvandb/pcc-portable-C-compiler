# PCC - Portable C Compiler

## Introduction
This is a mirror of the Portable C Compiler (PCC) sources from http://pcc.ludd.ltu.se/ initially as of 2018-11-11. I will attempt to keep it current with the CVS repository on that site but I make no promises as to its accuracy or completeness.

If you need something more current, or if you notice a problem, please file an issue and I'll see what I can do to update this mirror.

## Note
I will not be maintaining the PCC code. I maintain this git mirror for my own convenience and hopefully others will find it useful.

## Process
The CVS repo is imported into *\_\_crap-clone\_\_* using the [Crap](https://github.com/rcls/crap/) CVS import tool. This README and the LICENSE were committed into *master* and *\_\_crap-clone\_\_* merged to *master*. This avoids contaminating the CVS history with my commits but does mean the most current CVS changes may be on the import branch, not on *master*.

The initial import was performed from a local snapshot of the CVS repo (pcc-cvs-20181111.tgz from http://pcc.ludd.ltu.se/ftp/pub/pcc/) for network performance reasons. This entailed creating a local cvsroot directory containing CVSROOT and pcc subdirectories and extracting the snapshot into pcc.

Then in a freshly initialized git repo, the local cvsroot was imported with:
```sh
    crap-clone -m __crap-clone__                      /path/to/local/pcc/cvsroot pcc
```
to create the import branch. Later updates are imported directly from the upstream CVS repo using:
```sh
    crap-clone -m __crap-clone__ -z9 :pserver:anonymous@pcc.ludd.ltu.se:/cvsroot pcc
```
to update the git import branch.

## License
The source is licensed with a [BSD style license](http://pcc.ludd.ltu.se/licenses/) to the best of my knowledge. I retrieved the license information on 2018-11-11, and after removing styles, divs and unrelated navigation stored it here as [LICENSE.md](./LICENSE.md) for reference.
