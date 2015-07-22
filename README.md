# PyTMM
Transfer Matrix Method implementation &amp; RefractiveIndex.info database browser

## Installation &amp; Basic Usage
By default the RefractiveIndex module thinks that it is installed side-by-side with the RefractiveIndex.info database:
.
+-- _PyTMM
|   +-- refractiveIndex.py
+-- RefractiveIndex
|   +-- library.yml


In this case, the database can be used as follows:
    $ catalog = RefractiveIndex()
    $ mat = catalog.getMaterial('main', 'Si', 'Aspnes')
    $ n = mat.getRefractiveIndex(500))  # wavelength in nanometers
    $ n = mat.getExtinctionCoefficient(500))  # wavelength in nanometers

If your folder structure is different, you just need to specify the path to the RefractiveIndex database:
    $ catalog = RefractiveIndex("./path/to/folder/with/RefractiveIndex/databae")
    $ mat = catalog.getMaterial('main', 'Si', 'Aspnes')
    $ n = mat.getRefractiveIndex(500))  # wavelength in nanometers


Examples of using the transferMatrix module can be found in
.
+-- _PyTMM
|   +-- _tests
|       +-- transferMatrix_tests.py


###Dependencies
- numpy
- pyyaml
- matplotlib (for plotting)
