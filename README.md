# `cson-sort` — sort the contents of a CSON file

This package provides a small program, `cson-sort`, that takes CSON data and writes it back out with
all objects sorted by key.  This is useful as a Git filter to make managing CSON files easier, for
example in your Atom configuration.

This script is derived from [Season](https://github.com/atom/season).

## Installing

    npm install -g cson-sort

## Setting up Git filter

Edit `.git/config` to contain the following:

    [filter "cson-sort"]
        clean = cson-sort

Set up a `.gitattributes` file to mark files to be filtered:

    *.cson filter=cson-sort

And add and commit your files!
