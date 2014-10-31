# bibkeys

A simple program to print keys from a BibTeX file. Written in vanilla Perl.


## Synopsis

```
bibkeys [OPTIONS] [FILE1] [FILE2] [...]

    --help, -h          Print this help message and exit
    --columns, -c       Put output in columns
    --nocolumns, -1     Suppress columns; print one key per line
```

## Description

bibkeys is a simple program to print out the keys of one or more BibTeX files.
It takes a list of filenames as arguments; if none are provided, it globs the
current directory for `.bib` files.

## Options

### --help, -h

Print a help message and exit

### --columns, -c

Output to columns, auto-formatted to terminal width. Requires
Array::Columnize; this option will be ignored if this module isn't
installed. This option is the default.

### --nocolumns, -1

Suppress columnized output; print one key per line.


## Exit Status

0 on success, 1 if no bib files could be found.

## Dependencies

This has a soft dependency on Array::Columnize. If you want output in
columns, formatted to your terminal width, you need it. If the module can't be
found, the program does the easy thing and defaults to single-column output
(as if you'd passed `--nocolumns` on the command line.

## Author

Michael McClimon, michael@mcclimon.org

## Bugs and Limitations

Probably lots. This program is written to scratch an itch of mine, and does
things in the dumbest way possible that still works for my needs. I wouldn't
be at all surprised if it didn't work on Windows.

## License and Copyright

Copyright (c) 2014 Michael McClimon

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
