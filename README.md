# FSD-Elevation-Editor
This is the release/issues repo for Foxtrot Scenery Design's Elevation Editor. This tool allows you to convert a Digital Elevation Model (DEM) raster image to Microsoft Flight Simulator Rectangle objects with heightmaps. Since this is a project to mostly solve an inhouse issue and a way to dive deeper into programming, especially with GIS data, I am keeping the code private for now. Down the line this project might be open to commits from other contributors!

## Roadmap
- [x] Create elevation rectangles from single georeferenced raster files (WGS84 EPSG:4326 only!)
- [ ] Create elevation rectangles from multiple raster files and multiple projections
- [ ] Drape runways over customised terrain
- [ ] Add Irregular (Quadtree) Tessellation for projects with various resolutions in different areas
- [ ] Improved UI and UX, especially visualising the area of interest being worked on and improved progress reporting
- [ ] Import/Export 3D models of (handsculped) terrain from and to MSFS
- [ ] Flatten coastlines using shapefiles
- [ ] More...

## Getting Started
![image](https://github.com/BrianDavos/FSD-Elevation-Editor/assets/44494655/d51352b6-7aac-4191-bc55-aaa55a88d819)
1. Open a WGS84 EPSG:4326 DEM raster image
2. Open a MSFS scenery xml where you want the rectangles to be placed
3. Choose a desired resolution in metres. The tool will not upscale the raster and will use the maximum available resolution. The tool will downscale an image if needed using bilinear interpolation
4. If checked, the default falloff will be overidden. By default, the tool will use a falloff value equal to the resolution and at the edge rectangles it will use higher values to blend the default terrain into the rectangles (Note, due to terraforming bug in MSFS, blending does not work as expected)
5. Start the conversion process
6. Status window for user feedback


## Documentation
COMING SOON

## Disclaimer
While this method works, it does not use the native CGL format since there is no updated method or tool available to generate CGL files. Therefore, this method is not guaranteed to offer the same performance as the native CGL files. Nonetheless, it should provide a reliable way to get elevation data into MSFS.
