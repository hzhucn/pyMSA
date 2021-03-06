<p align="center">
  <br/>
  <img src=resources/pymsa.png alt="pyMSA">
  <br/>
</p>

# Scoring Multiple Sequence Alignments with Python
[![Build Status](https://img.shields.io/travis/benhid/pyMSA.svg?style=flat-square)](https://travis-ci.org/benhid/pyMSA)
[![PyPI License](https://img.shields.io/pypi/l/pyMSA.svg?style=flat-square)]()
[![PyPI Python version](https://img.shields.io/pypi/pyversions/pyMSA.svg?style=flat-square)]()

pyMSA is an open source software tool aimed at providing a number of scores for
multiple sequence alignment (MSA) problems. A [tutorial](resources/tutorial-pymsa.pdf) about pyMSA is available in the resources folder of the proyect.

## Features
The scores that are currently included are:
* Sum of pairs,
* Star,
* Minimum entropy,
* Percentage of non-gaps,
* Percentage of totally conserved columns *and*
* STRIKE (**S**ingle s**TR**ucture **I**nduced **E**valuation).

## Downloading
To download PyMSA just clone the Git repository hosted in GitHub:
```bash
$ git clone https://github.com/benhid/pyMSA.git
$ python setup.py install
```

Alternatively, you can install it with `pip`:
```bash
$ pip install pyMSA
```

### Substitution matrices

pyMSA has two available substitution matrices: *PAM250*  and *Blosum62*. Other substitution matrices can be used by reading a matrix [file](ftp://ftp.ncbi.nih.gov/blast/matrices/) with `read_matrix_from_file()` (from the `pymsa.util.substitution_matrix` module). `FileMatrix` implements this method by default:

```python
from pymsa.core.substitution_matrix import PAM250, Blosum62, FileMatrix

pam250 = PAM250()
blosum62 = Blosum62()
pam380 = FileMatrix('PAM380.txt')
```

## Usage
An example of running all the included scores is located in the [`example`](examples/) folder.

<p align="center">
  <br/>
  <img src=resources/terminal.png width=600 alt="Terminal session">
  <br/>
</p>

## Authors
### Active development team
* [Antonio Benítez-Hidalgo](https://benhid.github.io/) <antonio.b@uma.es>
* [Antonio J. Nebro](http://www.lcc.uma.es/~antonio) <antonio@lcc.uma.es>

## License
This project is licensed under the terms of the MIT - see the [LICENSE](LICENSE) file for details.
