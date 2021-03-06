# ldit

List Docker hub Image Tags.

## Requirements

- python>=3.2
- requests

## Installation

```
$ pip3 install -U ldit
```

## Usage

- CLI

```
ldit [-h] image [image ...]

positional arguments:
  image       image name, eg. fedora, google/debian etc.

optional arguments:
  -h, --help  show this help message and exit
```

- As module

```python
from ldit.ldit import list_tags

print(list_tags('image'))
```

## Example

- CLI

```
$ ldit google/debian fedora
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

- As module

```
>>> from ldit.ldit import list_tags
>>> print(list_tags('google/debian'))
['jessie', 'wheezy']
>>> print(list_tags('fedora'))
['31', 'rawhide', '30', '29', 'latest', '26', '27', '28', 'branched', '25', '26-modular', 'modular', '24', 'heisenbug', '20', '21', '22', '23']
```
