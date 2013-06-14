Background
==========

Druggability of a target protein is an important question in drug discovery.
A reliable and physically relevant measure of druggability can help determining
risks associated with pursuing a given target protein. Furthermore, a
comprehensive analysis of druggability of a target can help identifying novel
sites and alternate inhibition mechanisms.

To this extent, experimental NMR and X-ray and computational screening methods
are utilized for druggable binding site identification. Protein pockets that
bind a wide range of fragments or organic solvent molecules in these screening
experiments usually coincide with known druggable sites.


Method & Theory
---------------

Based on these ideas, we developed a unbiased simulation based approach to
assess druggability of target proteins with known structures. Our approach
involves simulations of the target in presence of a set of small organic
molecules (probes) with diverse physiochemical properties. Probes are selected
to be small (four non-hydrogen atoms) so that they can diffuse fast and explore
small and even transient pockets in simulations. This property also helps
sampling large number of binding events and enables reaching equilibrium in
relatively short simulation times.

Simulation trajectories are analyzed to calculate probe enrichment on protein
surface and pockets using a grid based approach. Enrichment grids are converted
to probe binding affinities using inverse Boltzmann relation. Binding sites
are identified by locating clusters of high affinity probe binding spots.
Druggability index for a binding site is calculated by considering
the affinities of seven or eight probe molecules (28 to 32 non-hydrogen atoms),
which is equivalent to a drug-like molecule in size.


Details of the approach can be found in [AB12]_. We showed that probes
mimic interactions of drug-like molecules, as well as substrates and
inhibitors that are not necessarily drug like. Thus, the approach is suitable
for assessing druggability or ligandability of a protein.