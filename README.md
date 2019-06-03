# Wall Probe Module
This module was developed by [ATA Engineering](http://www.ata-e.com) as an 
add-on to the Loci/CHEM computational fluid dynamics (CFD) solver. The module 
can be used to output wall data to files during a Loci/CHEM simulation. The
user inputs the desired location of the wall probes, and the data output comes
from the closest face center on the nearest viscous boundary 
(e.g. **viscousWall** or **wallLaw**). The data output includes wall quantities
of interest such as pressure, temperature, heat flux, shear stress, and y+. The
data from each wall probe will be output to a separate file with its same name.

# Dependencies
This module depends on both Loci and CHEM being installed. Loci is an open
source framework developed at Mississippi State University (MSU) by Dr. Ed 
Luke. The framework provides a rule-based programming model and can take 
advantage of massively parallel high performance computing systems. CHEM is a 
full featured open source CFD code with finite-rate chemistry built on the Loci 
framework. Both Loci and CHEM can be obtained from the 
[SimSys Software Forum](http://www.simcenter.msstate.edu) hosted by MSU.

# Installation Instructions
First Loci and CHEM should be installed. The **LOCI_BASE** environment
variable should be set to point to the Loci installation directory. The 
**CHEM_BASE** environment variable should be set to point to the CHEM 
installation directory. The installation process follows the standard 
make, make install procedure.

```bash
make
make install
```

# Usage
Usage follows the standard probe functionality in Loci/CHEM. First the module
must be loaded at the top of the **vars** file. The user can then define the
location of the probes and their frequency with the **wall_probe** and 
**wall_probe_freq** variables.

```
loadModule: wallProbe

wall_probe_freq: 5
wall_probe: <wprobe1=[0,0,0], wprobe2=[1,0,0]>
```

