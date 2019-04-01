# GeoSim-Final-Project
### WS 2017/2018

* GROUP MEMBERS: Akhil Patil, Saphir El -KaiyKaiy, Shenaha Sivakumar, Zhihao Liu
* PAPER: We are working with the paper "Spatial vegetation patterns and imminent desertification in Mediterranean arid ecosystems" by Ke´fi et al. (2007)
* TASK: The task is to create a model that reproduces the results of the paper.

## contouring
infile = r"D:\script\hydro-CEM\input\TDF_N08W062_02_WBM.tif"
outfile = r"D:\script\hydro-CEM\output\62\countour.shp"
if os.path.exists(outfile):
    os.remove(outfile)
else:
     os.path.join(outfile)
     os.system('gdal_contour -b 1 -a ELEV -i 10.0 -off 1 -f "ESRI Shapefile" %s %s'%(os.path.join(infile),os.path.join(outfile)))
