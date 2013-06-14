.. _specify:

Analyze a Specific Site
=======================

Weakly druggable sites can be missed in druggability analysis step. Or,
a site of interest might be partly identified. Druggability of a specific
site can be calculated using the following interface:

.. figure:: _static/gui_specify.png
   :scale: 80%


Input Files
-----------

Input files area list of ligand :file:`.pdb` files and :file:`.dso` file
from previous step. Ligand-bound form of the protein should be aligned
to the simulated structure. You can use :file:`prefix_heavyatoms.pdb`
file for alignment.


Options & Parameters
--------------------

1. Parameters determined how many probe binding spots are incorporated in
   assessment of the specified site. Selected probe should be close to
   the ligand, so 1.5 Å should be sufficient. If the ligand is bound to
   a weak site, maximum free energy may be lower that that is used in
   the previous step, such as -0.5 kcal/mol.

2. GUI will try to locate Python executable path, but if you do not see an
   entry, you will need to specify it manually.

Output Files
------------

Output from this step is a set of PDB files written into :file:`prefix`
and the druggability of sites specified by ligands.
