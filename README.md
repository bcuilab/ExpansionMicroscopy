# ExpansionMicroscopy
Codebase for expansion microscopy data shown in our publication https://placeholder.com

Requirements:
The letter-deformation fits shown in Fig. X are performed with Deformetrica: https://www.deformetrica.org/
Deformetrica framework is limited to Linux and MacOsX distributions for now

For the statistics of pillar-to-pillar distances before and after expansion, we provide the Jupyter Notebook 'Analyze_gel_chip.ipynb'. The raw images can be found in the 'chip_replicate' and 'gel_avg_replicate' folders in .tif and .nd2 format. The jupyter notebook runs a code that converts these images into png images in new folders. The script supposes that the user has taken these new .png images, and done a two-class segmentation on them (background, pillar) with the help of ilastik (www.ilastik.org), a free, easy-to-use software. Ilastik will place the segmented data into .h5 files inside the same folder.

For shape matching the deformation of the letters and numbers that we performed, deformetrica is needed to be installed. The jupyter notebook 'process_shapes.ipynb' implements the entire shape-matching pipeline from the data found in 'Chip_crop_byhand' and 'Expanded_gel_crop'. The .xml files are required for deformetrica to correctly run the LDMM algorithm for shape matching. The Jupyter Notebook further shows how to calculate local expansions separately for voids, and filled gels (for example, the letter B contains the void as the letter, but the two 'holes' inside of the letter 'B' have gel in it. 

For any questions, please contact the corresponding author.
