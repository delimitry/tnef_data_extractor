# TNEF data extractor
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/delimitry/tnef_data_extractor/blob/master/LICENSE)

A tool in Python for extracting data, like attachments and e-mail content (in compressed RTF format), from TNEF files (e.g. `winmail.dat`).

Installation:
-------------
Before running the tool, please install the dependencies using `pip`:
```
pip install -r requirements.txt
```

Usage:
------
```
usage: tnef_data_extractor.py [-h] [-f FILE] [-o OUTPUT]

TNEF data extractor

optional arguments:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  input file (e.g. winmail.dat)
  -o OUTPUT, --output OUTPUT
                        output directory ("out" by default)
```

Examples:
---------
```
user$ python3 tnef_data_extractor.py -f winmail.dat -o ./out_dir
Saving decompressed RTF data to: winmail.dat_data_0.rtf
Saving attachment to: 2018~1.PDF
Saving attachment meta file to: 2018~1.PDF_meta_0.raw
```
After that the next files will be in `out_dir` directory:
```
user$ ls ./out_dir
2018~1.PDF  2018~1.PDF_meta_0.raw  winmail.dat_data_0.rtf
```

License:
--------
Released under [The MIT License](https://github.com/delimitry/tnef_data_extractor/blob/master/LICENSE)
