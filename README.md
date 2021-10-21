# UniqPy

UniqPy is a UNIQUAC-based tool designed for vapor-based quantification of multicomponent systems. Due to UniqPy deals only with vapor phase it is able to quantify only volatile organic compounds (VOCs).

## Dependencies

Only the `scipy` python library is required.

## Usage

### Model fitting

Suppose that `x.txt` contains the matrix where each column means the substance, each row means the sample, and values means relative concetrations of the substances for each sample in the source (mainly liquid) phase. The file named `y.txt` contains the same information but about vapor phase relative pressures. The fitting can be performed with the following command:

`uniqpy fit -l x.txt -v y.txt -q Q.txt -r R.txt -p parameters.txt`

`-p` parameter sets the output file name. `Q.txt` and `R.txt` are text files which contain molecular surface areas and volumes. These values can be found in different ways, for instance using the MSMS algorithm implemented as a [PyMOL plugin](http://pldserver1.biochem.queensu.ca/~rlc/work/pymol/msms_pymol.py). Examples of x, y, Q and R are availabe in the `test` folder in this repository.


### Vapor data transforming

Vapor-to-liquid transformation can be performed with this command:

`uniqpy transform -v y.txt -q Q.txt -r R.txt -p parameters.txt`



### References

will be added