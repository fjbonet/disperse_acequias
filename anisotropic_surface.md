# Obtain an anisotropic cost layer to describe waterflow in the system of irrigation channels


The idea is to label each pixel according to its chance to receive water from the closest irrigation channel. This should be done using an hydrological model. As we have not any, we will compute this feature using the landscape metrics as surrogates.

IDRISI implemented a nice algorithm (DISPERSE) to create such a friction surface. I am trying to use R or ArcGIS to do it.

* ArcGIS "Path distance". It does not work
	* Input raster: todas_juntas_clip.shp
	* Output distance raster: PathDis_toda1
	* Input cost raster: slope
	* Input surface raster: mde