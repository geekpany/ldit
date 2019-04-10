# ldit
List Docker hub Image Tags.

## Dependences
- python>=3.2
- requests==2.21.0

## Usage
```
python3 ldit.py [-h] image [image ...]

positional arguments:
  image       image name, eg. alpine, google/debian etc.

optional arguments:
  -h, --help  show this help message and exit
```
## Example
```
$ python3 ldit.py google/debian fedora
The image 'google/debian' on Docker Hub got following tag(s):
jessie
wheezy
The image 'fedora' on Docker Hub got following tag(s):
31
rawhide
30
29
latest
26
27
28
branched
25
26-modular
modular
24
heisenbug
20
21
22
23
```
