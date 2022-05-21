---
layout: note
title: "Making maps in Python"
date: "2021-10-15"
tags:
- coding
- Python
- how-to
---

In my [NZ project](notes/prj.tempmatch.md), I decided to plot my results entirely in Python to keep the pipeline simple. Turned out if you can fix the projection, you are half-way there. The projection is handled by [Cartopy](https://scitools.org.uk/cartopy/docs/latest/index.html).

# Cartopy for projection

```python
import matplotlib.pyplot as plt
import cartopy.crs as ccrs

# Choosing a projection here
proj = ccrs.Mercator(central_longitude=Catalog.Longitude.mean())
fig = plt.figure(figsize=[8, 8])
# And set the projection of the axis
ax = fig.add_subplot(111, projection=proj)
ax.set_extent([165.5, 175.1, -47.5, -40], crs=ccrs.PlateCarree(proj))
grd = ax.gridlines(draw_labels=True)
s = ax.scatter(Catalog.Longitude, Catalog.Latitude, marker='o',
               s=Catalog.Magnitude**2, edgecolor='k', facecolor='none',
               transform=ccrs.Geodetic())
plt.show()
```

# Plot shapefiles using geopandas
Geopandas is great in that I don't need to fire up any GIS software to extract the spatial information from an shapefile. And the dataframe is ready to use just as in pandas.

```python
import geopandas as gpd

# Read in the composite seismogenic sources shapefile
eshm_css = gpd.read_file("CrustalFaults.shp")
# Get a subset around central Italy
css_apennines = eshm_css.loc[[241, 253, 256, 265, 268, 269, 283], :]

# Setting up the basemap
proj = ccrs.Mercator(central_longitude=13.3)
fig = plt.figure(figsize=[8, 12])
ax = fig.add_subplot(111, projection=proj)
ax.set_extent([11.4, 14.4, 41.4, 43.9], crs=ccrs.PlateCarree(proj))
css_apennines.plot(column="SRMEAN", ax=ax, transform=ccrs.Geodetic(), 
                   colors='viridis', legend=False, lw=2)
ax.coastlines(resolution="10m")
plt.show()
```

# EarthPy for hillshades
Yet to try it but here is the [reference](https://earthpy.readthedocs.io/en/latest/gallery_vignettes/plot_dem_hillshade.html)
