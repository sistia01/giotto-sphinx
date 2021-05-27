

Getting Started 
==========================================================

Description 
==============================================================
* Giotto provides a flexible framework for common single-cell processing steps such as:

	* Quality control
	* Normalization
	* Dimension reduction
	* Clustering and cell type annotation

* To facilitate the analysis of recently emerging high-throughput, but lower-resolution spatial transcriptomic technologies, such as 10X Genomics Visium and Slide-seq, Giotto has 3 implemented algorithms for estimating the spatial enrichment of different cell types by integration of known gene signatures or single-cell RNAseq expression and annotation data.
* Spatial information is retained through the formation of a spatial grid and/or a spatial proximity network, which is used to:

	* Identify spatial genes
	* Extract continuous spatial-expression patterns
	* Identify discrete spatial domains using HMRF
	* Explore cell-type/cell-type spatial interaction enrichment or depletion
	* Calculate spatially increased ligand-receptor expression in cells of interacting cell type pairs
	* Find interaction changed genes (ICG): genes that change expression in one cell type due to interaction with a neighboring cell type

* Giotto provides a number of options to visualize both 2D and 3D data and the outcome of Giotto can be interactively explored using `Giotto Viewer`_, which allows you to overlay the obtained results with raw or additional images of the profiled tissue section(s).

.. _Giotto Viewer: http://spatial.rc.fas.harvard.edu/spatialgiotto/giotto.install.native.html

Make sure to check out the **Datasets** section to see examples of the Giotto workflow.


Requirements
=============================================================
* R (>= 3.5.1)
* Python (>= 3.0)
* `Windows, MacOS or Linux specific installation tools.`_

.. _Windows, MacOS or Linux specific installation tools.: https://support.rstudio.com/hc/en-us/articles/200486498-Package-Development-Prerequisites

Installation 
=============================================================

R Installation 
------------------------------------------------------------
You can install Giotto with (~1-5 mins)::

	library(devtools)  # If not installed: install.packages('devtools')
	library(remotes)  # If not installed: install.packages('remotes')
	remotes::install_github("RubD/Giotto") 

	# Compilation (gfortran) problems? Check goftran.
	# This version does not require C compilation
	remotes::install_github("RubD/Giotto@cless") 

Required Python Modules
------------------------------------------------------------
These are necessary to run all available analyses, but can be installed automatically:

* pandas
* python-igraph (igraph)
* networkx
* leidenalg
* python-louvain (community)
* smfishHmrf
* python.app (**OSX only**)
* scikit-learn

Automatic installation
------------------------------------------------------------
The python modules will be installed automatically in a miniconda environment when installing Giotto. However, it will ask you whether you want to install them and you can opt out and select your preferred python path. In that case you need to do a manual installation of the python modules.


Manual installation
------------------------------------------------------------
See `Python Installation`_.

.. _Python Installation: 

Workflow Diagram 
================================================================

HowTos
================================================================
Giotto provides a lot of analyses, visualizations and other options to facilitate your spatial dataset analysis. We are working on providing easy-to-understand examples or tutorials, but if anything is not clear or if there is something you would like to see in particular, then do not hesitate to `contact us.`_

.. _contact us.: https://github.com/RubD/Giotto/issues

Giotto Workflow Analyses
----------------------------------------------------------------

*Optional*: Install a Giotto Environment

#. Create a Giotto Object 
#. Process and Filter a Giotto Object 
#. Dimension Reduction  
#. Cluster cells or spots
#. Identify differentially expressed genes
#. Annotate clusters
#. Cell-type enrichment or deconvolution per spot
#. Create a Spatial grid or Network
#. Find genes with a spatially coherent gene expression pattern
#. Identify genes that are spatially co-expressed
#. Explore spatial domains with HMRF
#. Calculate spatial cell-cell interaction enrichment
#. Find cell-cell interaction changed genes (ICG)
#. Identify enriched or depleted ligand-receptor interactions in hetero and homo-typic cell interactions
#. Export Giotto results to use in Giotto viewer
 
Giotto Analyzer and Viewer interaction [work in progress]
-------------------------------------------------------------

* How to switch between Giotto Analyzer and Viewer?

Giotto Tips and Tricks
-------------------------------------------------------------
* Different ways of subsetting Giotto results?
* How to create global instructions and show or save your created plots?
* Different ways to visualize your spatial data?
* How to test and store multiple parameters or analyses?
* Visualize spatial data with voronoi plots
* Adding and working with images in Giotto
* Working with the Giotto class


See `FAQs`_ for more information.
--------------------------------------------------------------

.. _FAQs:

