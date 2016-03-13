# ldpop
Two locus likelihoods and ARGs under changing population size

## Installation and Dependencies

Prerequisites:
* Scientific distribution of Python 2.7, e.g. [Anaconda](http://continuum.io/downloads), [Enthought Canopy](https://www.enthought.com/products/canopy/)
  * Alternatively, custom installation of pip, the SciPy stack
* Optional: Java 8
  * Required for posterior sampling of 2-locus ARGs.
  * Not required for computing lookup tables.

To install, in the top-level directory of ldpop (where "setup.py" lives), type
```
pip install .
```

To uninstall, do
```
pip uninstall ldpop
```

## Getting started
Use `bin/ldtable.py` to create a lookup table. See
```
bin/ldtable.py --help
```
for usage.

By default `bin/ldtable.py` uses an exact algorithm to compute the likelihoods.
To use a reasonable approximation that is much faster and scales to larger sample sizes,
use the flag `--approx`.

`bin/ldproposal.py` and `bin/ImportanceSampler.jar` are for importance sampling from the posterior distribution of 2-locus ARGs.
`bin/ldproposal.py` creates a proposal distribution, that `bin/ImportanceSampler.jar` uses to sample the ARGs. See their `--help` for instructions.

Also, see the [examples](example/).

## Authors

[John Kamm](mailto:jkamm@stat.berkeley.edu), Jeffrey Spence, Jeffrey Chan, Yun S. Song

## License

ldpop is not yet publicly released; please do not share with others.

When ldpop is publicly released, it will be free software under conditions of GNU GPL v3.

# TODO

Tasks, in roughly the order of importance (edited by Jeff S. 3/9/16):
* Write better tests in test/
