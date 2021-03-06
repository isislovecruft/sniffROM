# sniffROM
A tool for passive data capture and reconnaissance of serial flash chips. It is used in conjunction with a Saleae logic analyzer to reconstruct flash memory contents and extract contextual information about device operations.

* Supports SPI and I²C flash chips.
* Recognizes most flash commands across different chip vendors.
* Preserves actual memory addresses of captured data.
* Binary visualization of reconstructed image.
```
usage: sniffROM.py [-h] [--addrlen [{2,3,4}]] [--endian [{msb,lsb}]]
                   [--filter [{r,w}]] [-o [O]] [--summary] [--graph] [-v]
                   input_file

sniffROM - Reconstructs flash memory contents and extracts other data from
passively sniffed commands in a Saleae logic analyzer capture file. Currently
supports SPI and I2C flash chips.

positional arguments:
  input_file            Saleae Logic SPI or I2C Analyzer Export File (.csv)

optional arguments:
  -h, --help            show this help message and exit
  --addrlen [{2,3,4}]   set length of SPI memory address in bytes (default: 3)
  --endian [{msb,lsb}]  set endianness of SPI memory bytes (default: msb)
  --filter [{r,w}]      analyze only READ or WRITE commands (default: both)
  -o [O]                flash image output file name (default: output.bin)
  --summary             print summary of sniffed commands and metadata
  --graph               show visual representation of flash layout
  -v                    increase verbosity (up to -vvv)
```
See [Wiki](https://github.com/alainiamburg/sniffROM/wiki) for documentation
