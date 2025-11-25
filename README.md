# Android Data Image Utilities

Git repository containing utilities for working with Android data images.

## Usage

*img2sdat - A tool to convert filesystem images into Android data images:*
```
$ ./img2sdat -h
usage: img2sdat [-h] [-b] [-c CACHE_SIZE] [-o OUT_DIR] [-v VERSION] input_image [original_image]

A tool to convert partition images into Android data images.

positional arguments:
  input_image           input partition image
  original_image        original partition image

options:
  -h, --help            show this help message and exit
  -b, --brotli          compress data image with brotli
  -c, --cache-size CACHE_SIZE
                        cache partition size (16 KiB by default)
  -o, --out-dir OUT_DIR
                        output directory (current directory by default)
  -v, --version VERSION
                        transfer list format version (version 4 by default)
```

##

*sdat2img - A tool to convert Android data images into raw images:*
```
$ ./sdat2img -h
usage: sdat2img [-h] [-o OUT] transfer_list new_dat

A tool to convert Android data images into raw images.

positional arguments:
  transfer_list  input transfer list
  new_dat        input data image

options:
  -h, --help     show this help message and exit
  -o, --out OUT  output file path (partition.img in the current directory by default)
```

## Dependencies

These utilities require Python 3 or newer installed on your system.

## Credits

This project would not be possible without the work of the these people:
- Andrei Conache ([@xpirt](https://github.com/xpirt)) - for bringing up img2sdat and sdat2img.
- Salvo Giangreco ([@salvogiangri](https://github.com/salvogiangri)) - for his work on modernizing img2sdat.
