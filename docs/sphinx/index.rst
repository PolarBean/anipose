Anipose
#######

|PyPI version| |DOI| |License: LGPL v3|

Anipose is an open-source toolkit for robust, markerless 3D tracking of animal behavior from multiple camera views. It leverages the machine learning toolbox `DeepLabCut <https://github.com/AlexEMG/DeepLabCut>`_ to track keypoints in 2D, then triangulates across camera views to estimate 3D pose.

Anipose consists of four modular components: (1) a 3D calibration module designed to minimize the influence of outliers, (2) a set of filters to resolve errors in 2D detections, (3) a triangulation module that integrates temporal and spatial constraints to obtain accurate 3D trajectories despite 2D tracking errors, and (4) a pipeline for efficiently processing large numbers of videos. These modules are packaged together within Anipose, but the calibration and triangulation functions are also availble as an independent library (aniposelib) for use without the full pipeline and applications beyond pose estimation.

The name Anipose comes from **Ani**\ mal **Pose**, but it also sounds
like "any pose".

Getting started
===============

1) Setup DeepLabCut by following the instructions
   `here <https://github.com/AlexEMG/DeepLabCut/blob/master/docs/installation.md>`_
2) Install Anipose through pip: ``pip install anipose``


.. figure:: anipose-tutorial/tracking_3cams_full_slower5.gif
   :align: center

   Videos of flies by Evyn Dickinson (slowed 5x), `Tuthill Lab <http://faculty.washington.edu/tuthill>`_

.. figure:: anipose-tutorial/hand-demo.gif
   :align: center

   Videos of hand by Katie Rupp

Documentation
=============

.. toctree::
   :maxdepth: 2

   installation
   params
   start2d
   start3d
   tutorial 
   aniposelib-tutorial
   aniposelib-api

   :caption: Contents:

Collaborators 
=============

- **Pierre Karashchuk**, Neuroscience Graduate Program, University of Washington 
- **Evyn S. Dickinson**, Department of Physiology and Biophysics, University of Washington
- **Katie Rupp**, Department of Physiology and Biophysics, University of Washington
- **Bingni W. Brunton**, Department of Biology, University of Washington
- `**John C. Tuthill**, Department of Physiology and Biophysics, University of Washington <http://faculty.washington.edu/tuthill>`_

References
==========

Here are some references for DeepLabCut and other things this project
relies upon: 

- Mathis et al, 2018, "DeepLabCut: markerless pose
  estimation of user-defined body parts with deep learning" 
- Insafutdinov et al, 2016, "DeeperCut: A Deeper, Stronger, and Faster
  Multi-Person Pose Estimation Model" 
- Romero-Ramirez et al, 2018, "Speeded up
  detection of squared fiducial markers" 
- Garrido-Jurado et al, 2016, "Generation of fiducial marker dictionaries
  using Mixed Integer Linear Programming"

.. |PyPI version| image:: https://badge.fury.io/py/anipose.svg
   :target: https://badge.fury.io/py/anipose
.. |DOI| image:: https://zenodo.org/badge/165723389.svg
   :target: https://zenodo.org/badge/latestdoi/165723389
.. |License: LGPL v3| image:: https://img.shields.io/badge/License-LGPL%20v3-blue.svg
   :target: https://www.gnu.org/licenses/lgpl-3.0

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
