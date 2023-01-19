# XtalTools Overview

This directory tree contains various scripts to manipulate periodic
structures in the context of molecular dynamics or refinement calculations.

Documentation is in the doc/xtaltools.pdf file, which is mainly designed to
give a roadmap to what is available, and to describe some ways the tools can
be combined for useful tasks.  Most of the documentation is in the scripts
themselves.

# Folder info:

* src  -- utilities from Dave Cerutti for set up of crystal MD simulations
* XtalAnalyze  -- utilities from Pawel Janowski for analysis
* ensemble_scripts -- tools for creating supercell ensembles for MD/refinement
* phenix_scipts  -- builds on phenix for miscellaneous manipulations
* ccp4_scipts  -- builds on CCP4/refmac for miscellaneous manipulations

# Installation

There is nothing really to "install".  Go to the src folder and type
"make" to generate the executables there.  The remaining bash, perl and
python scripts generally assume that you will copy the files to a working
directory, make changes there with an editor, then run.  I am working to
put most of the documentation inside each script.

# Warning

This is a work in progress, and may not always be in a stable state
(although that is my goal for the main branch).  I may not be able to
respond to requests for support.

# License

This project is licensed under the GNU General Public License, version
2, or (at your option) any later version.  See the LICENSE file for more
information.

