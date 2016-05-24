# Obtain an anisotropic cost layer to describe waterflow in the system of irrigation channels


The idea is to label each pixel according to its chance to receive water from the closest irrigation channel. This should be done using an hydrological model. As we have not any, we will compute this feature using the landscape metrics as surrogates.

IDRISI implemented a nice algorithm (DISPERSE) to create such a friction surface. I am trying to use R or ArcGIS to do it.


* Primera versión decente. Faltaría reclasificar el raster para facilitar la asignación de etiquetas a los píxeles de modis. En principio sería cambiar el orden de la leyenda y luego aplicar alguna función de agrupación. Verlo con ajpelu. Arcgis Path distance
	* Input: todas_juntas_clip
	* Output distance raster: afecace
	* Input surface raster:
	* Horizontal parameters:
		* Forward horizontal
	* Vertical parameters:
		* Cos vertical
		
Pruebas:

* ArcGIS "Path distance". It does not work
	* Input raster: todas_juntas_clip.shp
	* Output distance raster: PathDis_toda1
	* Input cost raster: slope
	* Input surface raster: mde
	
* ArcGIS "Path distance". It does not work
	* Input raster: todas_juntas_clip.shp
	* Output distance raster: PathDis_toda2
	* Input cost raster: slope
	* Input surface raster: mde_snev
	* Vertical parameters: mde_snev
	
* ArcGIS "Path distance". It does not work
	* Input raster: prueba.shp
	* Output distance raster: prueba1
	* Input cost raster: slope
	* Input surface raster: mde_snev
	* Vertical parameters: mde_snev
	
	
	
* ArcGIS "Path distance". It does not work
	* Input raster: prueba.shp
	* Output distance raster: prueba2
	* Input cost raster: aspect_mde_r1
	* Input surface raster: mde_snev
	* Vertical parameters: mde_snev
	* output baklink: backlink
	
* ArcGIS "Path distance". Sale interesante, valores infinitos sobre la acequia. dis
	* Input raster: prueba.shp
	* Output distance raster: prueba5
	* Input cost raster: 
	* Input surface raster: mde_re
	* output baklink: backlink
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
	
* ArcGIS "Path distance". Sale interesante, valores infinitos sobre la acequia. dis
	* Input raster: prueba.shp
	* Output distance raster: prueba6
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* linear vertical

* ArcGIS "Path distance". Sale interesante, valores infinitos sobre la acequia. dis
	* Input raster: prueba.shp
	* Output distance raster: prueba7
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* linear horizontal.
		* binary vertical
		
* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba8
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* forward horizontal.
		* binary vertical
	* **me gusta porque todas las zonas son cubiertas y el límite superior es neto**
	
* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba9
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* inverse lineal horizontal.
		* binary vertical
	* **me gusta porque todas las zonas son cubiertas y el límite superior es neto**

* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba10
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* binary horizontal.
		* linear vertical
	* ** no mola**

* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba11
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* binary horizontal.
		* symetric linear vertical
	* ** no mola**
	
* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba12
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* binary horizontal.
		* cos vertical
	* ** no mola**
	
	
* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba13
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* fordward horizontal.
		* symetric linear vertical
	* ** distribución homogéna**
	
	
* ArcGIS "Path distance". 
	* Input raster: prueba.shp
	* Output distance raster: prueba14
	* Input cost raster: 
	* Input surface raster: mde_re
	
	* Horizontal parameters: aspect_mde_r1
	* Vertical parameters: mde_snev
		* fordward horizontal.
		* cos vertical
	* ** distribución homogéna**
	


	 
