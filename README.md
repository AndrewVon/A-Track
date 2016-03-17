# Moving Object Detection

### Dependencies:

* [Python](https://www.python.org/) 3.4.x or later.
* [Numpy](http://www.numpy.org/) 1.8.x or later.
* [Pandas](http://pandas.pydata.org/) 0.16.x or later.
* [AliPy](http://obswww.unige.ch/~tewes/alipy/) 2.0.x or later.
* [PyFITS](http://www.stsci.edu/institute/software_hardware/pyfits) 3.3.x or later.
* [f2n](https://github.com/akdeniz-uzay/mod/tree/master/f2n) for Python 3

### <a name="usage"></a> Usage

```bash
usage: python3 atrack.py [-h] [--ref ref_image] [--skip-align] [--skip-cats]
                         [--skip-pngs] [--skip-gif] [--version]
                         fits_dir

A-Track.

positional arguments:
  fits_dir         FITS image directory

optional arguments:
  -h, --help       show this help message and exit
  --ref ref_image  reference FITS image for alignment (with path)
  --skip-align     skip alignment if alignment is already done
  --skip-cats      skip creating catalog files if they are already created
  --skip-pngs      skip creating PNGs
  --skip-gif       skip creating animation file
  --version        show version
```

### Installation

A-Track is tested on Ubuntu 14.04 LTS, Fedora 22 and Mac OS X Yosemite.

To install A-Track on any OS, run the following commands:


**Ubuntu:** ```sudo apt-get install python3 python3-pip imagemagick git-all sextractor```

**Fedora:** ```sudo dnf install python3-pip imagemagick git-all```

* Install the latest SExtractor from [here](http://www.astromatic.net/download/sextractor/) (we suggest v2.19.5 as the older versions detect fewer objects).

**Mac OS X:** You need [Homebrew](http://brew.sh) to install the dependencies.

* ```brew install imagemagick git python3 sextractor```

Numpy, Pandas, Scipy, pyFITS and pillow can be installed with pip3 (GNU/Linux users! Don't forget the ```sudo```):

```bash

cd ~
pip3 install numpy pandas pyfits pillow scipy matplotlib

git clone https://github.com/akdeniz-uzay/alipy.git
cd alipy
python3 setup.py install

cd ..
git clone https://github.com/japs/astroasciidata
cd astroasciidata
python3 setup.py install
cd ..
```

Finally, you can download the A-Track files and install the f2n package:

```
cd ..
git clone https://github.com/akdeniz-uzay/A-Track
cd f2n
python3 setup.py install
```

Now, you have A-Track! You can open a command-line interface in the A-Track directory and execute the file [atrack.py](#usage)!

**P.S.:** If you want to use A-Track on Windows, you need to install SExtractor first! This is a bit tricky. Please see the [link](http://www.astromatic.net/forum/showthread.php?tid=948).
