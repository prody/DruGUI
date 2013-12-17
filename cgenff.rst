.. _cgenff:

Diverse Molecules from CGenFF
=============================


DruGUI also has a command utility, :program:`drugui`
for setting up a system containing molecules from
`CHARMM General Force Field <http://mackerell.umaryland.edu/~kenno/cgenff/>`_.


In VMD :guilabel:`Tk Console`, typing :program:`drugui` command will print::

  Info) Usage: drugui <psffile> <pdbfile> [options]
  Info)
  Info) Options:
  Info)     -probes <Yes/no>
  Info)       (use default probe mixture; see below)
  Info)     -PROBE <percentage>
  Info)       (probe type and percentage, e.g. -IPRO 80 -ACET 10 -IPAM 10)
  Info)     -prefix <outname>
  Info)       (data will be written to outname.psf/outname.pdb/etc.)
  Info)     -outdir <directory>
  Info)       (data will be written into specified directory, default is .)
  Info)     -rotate <yes/No>
  Info)       (rotate molecule to minimize water volume)
  Info)     -padding <distance>
  Info)       (minimum solvent box padding in all directions, default is 6 A)
  Info)     -boundary <distance>
  Info)       (minimum distance between water/probe and solute, default is 2.4 A)
  Info)     -neutral <Yes/no>
  Info)       (add counter ions, chloride or sodium, to make the system neutral)
  Info)     -lipid <yes/No>
  Info)       (system is solvated by considering lipid bilayer in xy plane)
  Info)     -nsim <number>
  Info)       (number of independent simulations, default 0)
  Info)     -simlen <ns>
  Info)       (length of individual simulations in ns)
  Info)     -constrain <Heavy/calpha>
  Info)       (which protein atoms to contraint in equilibration step)
  Info)     -parameter <filename>
  Info)       (additional parameter files; multiple occurrence is handled)
  Info)
  Info) Available probes -RESI [default_percentage] (name, charge, source)
  Info)
  Info) Core probes
  Info)     -IPRO 70% (isopropanol, 0.0e, PBDA)
  Info)     -ACAM 10% (acetamide, 0.0e, PBDA)
  Info)     -ACTT 10% (acetate, -1.0e, PBDA)
  Info)     -IPAM 10% (isopropylamine, 1.0e, PBDA)
  Info)     -IBTN (isobutane, 0.0e, PBDA)
  Info)     -IMID (imidazole, 0.0e, PBDA)
  Info)
  Info) Polar probes
  Info)     -PRO2 (2-propanol, 0.0e, CGenFF)
  Info)     -GLYN (glycine, 0.0e, CGenFF)
  Info)     -ACEH (acetic acid, 0.0e, CGenFF)
  Info)     -ACEM (acetamide, 0.0e, CGenFF)
  Info)     -PRAM (propionamide, 0.0e, CGenFF)
  Info)     -NMA (N-methylacetamide, 0.0e, CGenFF)
  Info)     -ACO (acetone, 0.0e, CGenFF)
  Info)     -TFE (trifluoroethanol, 0.0e, CGenFF)
  Info)     -MP_0 (neutral methylphosphate, 0.0e, CGenFF)
  Info)     -UREA (urea, 0.0e, CGenFF)
  Info)     -MSAM (methanesulfonamide, 0.0e, CGenFF)
  Info)     -MMSM (N-methylmethanesulfonamide, 0.0e, CGenFF)
  Info)     -MMST (methyl methanesulfonate, 0.0e, CGenFF)
  Info)     -DMSN (dimethyl sulfone, 0.0e, CGenFF)
  Info)     -MESN (methyl ethyl sulfone, 0.0e, CGenFF)
  Info)     -DMSO (dimethylsulfoxide, 0.0e, CGenFF)
  Info)     -2PDO (2-pyrrolidinone, 0.0e, CGenFF)
  Info)     -TMAO (trimethylamine N-oxide, 0.0e, CGenFF)
  Info)
  Info) Hydrophobes
  Info)     -IBUT (isobutane, 0.0e, CGenFF)
  Info)     -BUTA (butane, 0.0e, CGenFF)
  Info)     -EMS (ethylmethylsulfide, 0.0e, CGenFF)
  Info)     -DMDS (dimethyldisulfide, 0.0e, CGenFF)
  Info)     -DFET (difluoroethane, 0.0e, CGenFF)
  Info)     -TFET (trifluoroethane, 0.0e, CGenFF)
  Info)     -DCLE (1,1-dichloroethane, 0.0e, CGenFF)
  Info)     -TCLE (1,1,1-trichloroethane, 0.0e, CGenFF)
  Info)
  Info) Negatively charged
  Info)     -ACET (acetate, -1.0e, CGenFF)
  Info)     -PROA (propionic acid, -1.0e, CGenFF)
  Info)     -CO3 (ionized carbonate, -2.0e, CGenFF)
  Info)     -MP_1 (anionic methylphosphate, -1.0e, CGenFF)
  Info)     -MP_2 (dianionic methylphosphate, -2.0e, CGenFF)
  Info)     -MSNA (methyl sulfonate, -1.0e, CGenFF)
  Info)     -ESNA (ethyl sulfonate, -1.0e, CGenFF)
  Info)
  Info) Positively charged
  Info)     -GUAN (guanidinium, 1.0e, CGenFF)
  Info)     -MGUA (methyl-guanidinium, 1.0e, CGenFF)
  Info)     -AMDN (amidinium cation, 1.0e, CGenFF)
  Info)
  Info) 5-membered rings
  Info)     -IMIA (imidazole, 0.0e, CGenFF)
  Info)     -IMIM (imidazolium, 1.0e, CGenFF)
  Info)     -MIMI (4-methylimidazole, 0.0e, CGenFF)
  Info)     -THAZ (thiazole, 0.0e, CGenFF)
  Info)     -TRZ4 (triazole124, 0.0e, CGenFF)
  Info)     -PYRL (pyrrole, 0.0e, CGenFF)
  Info)     -FURA (furan, 0.0e, CGenFF)
  Info)     -THIP (thiophene, 0.0e, CGenFF)
  Info)     -OXAZ (oxazole, 0.0e, CGenFF)
  Info)     -ISOX (isoxazole, 0.0e, CGenFF)
  Info)     -ISOT (isothiazole, 0.0e, CGenFF)
  Info)     -PYRZ (pyrazole, 0.0e, CGenFF)
  Info)     -OXAD (oxadiazole123, 0.0e, CGenFF)
  Info)     -2HPR (2H-pyrrole, 0.0e, CGenFF)
  Info)     -2PRL (2-pyrroline, 0.0e, CGenFF)
  Info)     -2PRZ (2-pyrazoline, 0.0e, CGenFF)
  Info)     -2IMI (2-imidazoline, 0.0e, CGenFF)
  Info)     -PRLD (pyrrolidine, 0.0e, CGenFF)
  Info)     -3PRL (3-pyrroline, 0.0e, CGenFF)
  Info)     -PRLP (pyrrolidine protonated, 1.0e, CGenFF)
  Info)     -3PRP (3-pyrroline protonated, 1.0e, CGenFF)
  Info)     -2PRP (2-pyrroline protonated, 1.0e, CGenFF)
  Info)     -2IMP (2-imidazoline protonated, 1.0e, CGenFF)
  Info)     -2HPP (2H-pyrrole protonated, 1.0e, CGenFF)
  Info)     -3HPR (3H-pyrrole, 0.0e, CGenFF)
  Info)     -CPDE (cyclopentadiene, 0.0e, CGenFF)
  Info)     -DIOL (1,3-Dioxolane, 0.0e, CGenFF)
  Info)     -IMDP (Imidazolidine protonated, 1.0e, CGenFF)
  Info)     -PRZP (Pyrazolidine protonated, 1.0e, CGenFF)
  Info)     -2DHF (2,3-dihydrofuran, 0.0e, CGenFF)
  Info)     -MCPE (methylcyclopentane, 0.0e, CGenFF)
  Info)     -OXD4 (oxadiazole124, 0.0e, CGenFF)
  Info)     -THF (tetrahydrofuran, 0.0e, CGenFF)
  Info)     -THFM (Methyl-tetrahydrofuran, 0.0e, CGenFF)
  Info)     -THFO (3'-hydroxyl-tetrahydrofuran, 0.0e, CGenFF)
  Info)     -CPEN (cyclopentane north types, 0.0e, CGenFF)
  Info)     -CPES (cyclopentane south types, 0.0e, CGenFF)
  Info)
  Info) 6-membered rings
  Info)     -BENZ (benzene, 0.0e, CGenFF)
  Info)     -PY01 (4H-Pyran, 0.0e, CGenFF)
  Info)
  Info)
  Info) Notes:
  Info)     - Passing "y" or "n" (case-insensitive) is sufficient for applicable options.
  Info)     - When probe types are specified, probe percentages must add up to 100.
  Info)     - When probe is "no", only water (and ions) will be added.
  Info)     - Water segment name prefix is "WT".
  Info)     - Ion segment name is "ION".
  Info)     - Input molecule dimensions are used to determine size of the solvation box.
  Info)     - When specified, all atoms of the system is rotated by 10 degree increments.
  Info)     - Sodium and chloride ions are used to neutralize the system.
  Info)     - Minimum distances from solute and between ions are set to 5 A.