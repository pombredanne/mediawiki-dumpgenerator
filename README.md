mediawiki-dumpgenerator
=======================

**Update:** The project is now on GitHub → https://github.com/WikiTeam/wikiteam

Copy of [WikiTeam](http://code.google.com/p/wikiteam/)’s [http://code.google.com/p/wikiteam/source/browse/trunk/dumpgenerator.py](http://code.google.com/p/wikiteam/source/browse/trunk/dumpgenerator.py) (GPLv3).

> dumpgenerator.py is a script to generate backups of MediaWiki wikis  
> To learn more, read the documentation:  
> http://code.google.com/p/wikiteam/wiki/NewTutorial

## Documentation: creating a dump

Assuming that the API (`/w/api.php`) is enabled. If not, replace the URL with `http://example.org/w/index.php`.

XML dump (full history):

    python dumpgenerator.py --api=http://example.org/w/api.php --xml

Image dump:

    python dumpgenerator.py --api=http://example.org/w/api.php --images

XML (full history) and image dump together:

    python dumpgenerator.py --api=http://example.org/w/api.php --xml --images

Options:

* `--xml --curonly` if only the last revision (instead of the full history) is needed

* `--delay=5` for a delay of 5 seconds

* `--resume --path=dumpdirectory` resumes an interrupted dump
