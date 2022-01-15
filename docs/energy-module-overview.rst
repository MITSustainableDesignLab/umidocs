.. |br| raw:: html

   <br />

.. _energy-module-overview:

Energy Module Overview
======================

.. container:: align-right

   .. figure:: assets/energy-module-overview-s83k47fm.png
      :scale: 35 %
      :align: center
      :name: figure_1

      Input Geometry

   .. figure:: assets/energy-module-overview-slk3yf86.png
      :scale: 35 %
      :align: center
      :name: figure_2

      Insolation Analysis Mesh |br| [high(red) low(blue)]

   .. figure:: assets/energy-module-overview-s83kd7s5.png
      :scale: 35 %
      :align: center
      :name: figure_3

      Clustering

      .. image:: assets/energy-module-overview-sjd63jdf8.png
         :scale: 50%
         :align: center

      .. raw:: html

         <p style=" text-align: center">low - insolation - high</p>

   .. figure:: assets/energy-module-overview-s93k47f8.png
      :scale: 35 %
      :align: center
      :name: figure_4

      Shoebox clusters


The operational energy model simulation uses your umi buildings and building template settings as well as the shading geometry on the umi shading layers. A small input geometry example is shown in :numref:`figure_1`.

First your building envelope is subdivided into floor volumes according to your floor to floor height settings in the building template. Along the facades of each floor volume a solar insolation analysis is performed using Radiance / GenCumulativeSky. Internally your geometry is meshed and then handed over to radiance. :numref:`figure_2` shows a typical result of this insolation simulation.

This radiation data as well as the basic facade surface orientation are then used to cluster facade regions of each building by solar micro climate similarity - see :numref:`figure_3` for an example. Each color represents a cluster. The number of clusters is a user setting and can be specified for each orientation (a typical cluster count per facade is two).

The Shoeboxer then assigns an area weight to each cluster centroid. This centroid is then also the location for a shoebox model that then represent the cluster. See :numref:`figure_4`. Each Shoebox or Cluster is written out as IDF file and is simulated with EnergyPlus. The final simulation step is to gather all shoebox data and aggregate the building result. For further details regarding the method please refer to the `reference paper <http://www.ibpsa.org/proceedings/BS2013/p_1123.pdf>`_.
