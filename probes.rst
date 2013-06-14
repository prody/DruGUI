Probe Molecules
===============

Probe molecules and their fractional composition, shown below, were selected
based on analysis of FDA approved drugs [AB12]_. The best composition for
a specific system may, however, depend on the surface properties of the target.
For a protein with a highly charged surface, increasing the proportion of
acetate and isopropylamine might perform better in identifying ligandable
sites.

.. only:: html

   +----------------------------+----------------------------+----------------------------+
   |.. figure:: _static/ipro.png|.. figure:: _static/acam.png|.. figure:: _static/acet.png|
   |   :scale: 25%              |   :scale: 25%              |   :scale: 25%              |
   |                            |                            |                            |
   |   Isopropanol (70%)        |   Acetamide (10%)          |   Acetate (10%)            |
   +----------------------------+----------------------------+----------------------------+
   |.. figure:: _static/ipam.png|.. figure:: _static/ibut.png|                            |
   |   :scale: 25%              |   :scale: 25%              |                            |
   |                            |                            |                            |
   |   Isopropylamine (10%)     |   Isobutane (0%)           |                            |
   +----------------------------+----------------------------+----------------------------+

.. only:: latex

   .. figure:: _static/ipro.png
      :scale: 25%

      Isopropanol (70%)

   .. figure:: _static/acam.png
      :scale: 25%

      Acetamide (10%)

   .. figure:: _static/acet.png
      :scale: 25%

      Acetate (10%)

   .. figure:: _static/ipam.png
      :scale: 25%

      Isopropylamine (10%)

   .. figure:: _static/ibut.png
      :scale: 25%

      Isobutane (0%)

Among these, isobutane is not included in the default configuration due to its
high propensity to aggregate. If it is included, it should have a small
fraction.


Topology & Parameter
--------------------
Probe atom types and parameters are based on protein side-chains
described in CHARMM force field. Below topology and parameter files
distributed with the plugin are shown:

.. literalinclude:: drugui/probe.top

.. literalinclude:: drugui/probe.prm

