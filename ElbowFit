# Note: object dat is a seurat object which has had SCTrasnform and RunPCA or equivilent (e.g. NormalizeData, FindVariabeFeatures, ScaleData, etc)
# Not functionlized yet sadly, so set 'ndims' varibale to calculate how many PC dimensions you want to see on the elbow plot... same as in Seurat ElbowPlot

# Fit interpolated function to elbow plot
# Then find derivative of that function
# Plot function curve, elbow plot, and f'[x] for each PC

data.use <- Stdev(object = dat, reduction = 'pca')
stdev <- 'Standard Deviation'
ndims = 40
f <- approxfun(1:ndims,data.use[1:ndims])
deriv = approxfun(2:ndims, diff(data.use[1:ndims])/diff(1:ndims))
diffs = sapply(2:ndims, FUN = deriv) 
diffs = round(diffs,digits = 2)
diffs <- c('',diffs)

curve(f(x), 0, 40, col = "green", xaxt='n')
points(1:ndims,data.use[1:ndims])
text(1:ndims,data.use[1:ndims] + 0.7, labels = diffs, cex = 0.6)
axis(side=1, at=1:ndims,cex.axis=0.5)
