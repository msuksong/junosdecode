# Junos $9$ secrets encrypt/decrypt script

## Usage
```
$ python junosdecode.py
usage: junosdecode.py [-h] [-v] [-r] [-e PLAINTEXT | -d SECRET]

Junos $9$ password en/decrypt script

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         show program's version number and exit
  -r, --result-only     Output resulting string only
  -e PLAINTEXT, --encrypt PLAINTEXT
                        encrypt plaintext
  -d SECRET, --decrypt SECRET
                        decrypt secret

```

## Examples
```
$ python junosdecode.py -e 'hello'
Junos $9$ secrets en/decrypter
python version by matt hite/min song
original perl version by kevin brintnall

plaintext version: hello
encrypted version: $9$lateMXVb2JGi7-Dk

$ python junosdecode.py -d '$9$lateMXVb2JGi7-Dk'
Junos $9$ secrets en/decrypter
python version by matt hite/min song
original perl version by kevin brintnall

encrypted version: $9$lateMXVb2JGi7-Dk
decrypted version: hello

$ python junosdecode.py -r -e 'hello'
$9$BrKEcyLX-Y2avWYoGif5/CA

$ python junosdecode.py -r -d '$9$BrKEcyLX-Y2avWYoGif5/CA'
hello
```
