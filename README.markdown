# Geany Syntax Files

## Description

The **geany-syntax** repository provides a collection of syntax files for **Geany**. The following syntax files are available:

* **filetypes.Mallard.conf** — A syntax file for the Mallard XML language according to [Mallard 1.0 DRAFT (as of 2013-02-11)](http://projectmallard.org/1.0/index.html). See also my [geany-snippets](https://github.com/jhradilek/geany-snippets) repository for snippets for this language.

## Installation

### Installing the Syntax Files

To install any of the available syntax files, change into the directory with your local copy of this repository and run the following command:

    cp filetypes.<filetype>.conf ~/.config/geany/filedefs/

For example, to install the syntax file for Mallard, type:

    cp filetypes.Mallard.conf ~/.config/geany/filedefs/

This copies the selected file to the **~/.config/geany/filedefs/** directory. Note that the directory must exist prior to running this command; to create it, type the following at a shell prompt:

    install -d ~/.config/geany/filedefs/

### Adding Support for the File Type

To add support for the selected file type, start **Geany** and select *Tools*→*Configuration Files*→*filetype_extensions.conf* from the menu. This opens the **~/.config/geany/filetype_extensions.conf** file in the editor.

1.  In the file, add a line in the following format to the **[Extensions]** section:

        <filetype>=*.<extension>;

    For example, to add support for the Mallard markup language that uses the **.page** file extension, type:

        Mallard=*.page;

2.  In the same file, add the file type to one of the groups in the **[Groups]** section:

        <group>=<filetype>;

    For example, to add the Mallard markup language to the Markup group, type:

        Markup=Mallard;

The changes take effect the next time you start the editor.

## Copyright

Copyright © 2013 Jaromir Hradilek

This program is free software; see the source for copying conditions. It is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
