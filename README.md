# ACA centroiding

### Goals

1. Replicate the on-board PEA centroids ('raw centroids'):

    * access level0 raw images,
    
    * compute first moments for background subtracted images,
    
    * compare the raw centroids with the telemetered values (<code>aoacyan</code>, <code>aoaczan</code>).

2. Apply a Gassian mask to the raw images to assign higher weigt to the central pixels. Check if this improves ACA centroiding for faint stars.

### Results

1. PEA centroids replicated to the accuracy of 0.01 arcsec (standard deviation of the residuals) even for faint stars (10.2 mag) with high background noise.

2. However, no improvement to centroiding when a weighting mask is used. The residuals show spikes corresponding to <code>IMGCOL0</code> and/or <code>IMGROW0</code> changing by ~1px due to the drift of the image withing the ACA window, while the weighting mask is static and centered in the 8x8 pixel image.
