zippy
=====

Unzip Zip64 files using only python
-----------------------------------

I recently found myself needing to unzip a Zip64 file on an older UNIX platform. The system didn't have access to v6.0 or greater of the UnZip tool, where support was added, and so I started digging around. It seems Python has been supporting the file format for a while now, and so I whipped up this script to do some unzipping!

This code should be compatible on any Linux system running Python v2.3 or greater.

    $ ./zippy
    zippy: Extracts Zip & Zip64 files
    Usage: zippy [options]
    
    Options:
      -h, --help      show this help message and exit
      -f ZIP_FILE     specify zip file
      -e EXPORT_PATH  specify an export path (optional)
      -p PASSWORD     specify a password (optional)

The Python v2.3 dependency comes from the optparse lib. I would switch to argparse, since optparse is now deprecated, but I'm trying to keep support out-of-the-box for older systems.