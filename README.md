# ElbowFit

Not functionalized yet sadly or written for ggplot2, hosted as an easy way to grab code here during analysis 

Simple modification of Seurat ElbowFit function to interpolate function to elbow plot, calculate derivative, and plot f'[x] over each PC. To help in determining number of PCs to include.

To use: modify 'dat' variable to be your seurat object after normalizing, finding variable features, scaling, and runing PCA on Seurat (or running SCTransform > RunPCA).

ndims will be the number of dimensions to plot. Again not functionalized or written with ggplot2 yet.
