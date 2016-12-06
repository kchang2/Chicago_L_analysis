# Chicago "L" analysis
Analyzing Chicago's L System for optimal location to start a restaurant business. Takes into account both spatial coordinates, and traffic density. Originally for a data science challenge, but now for an interest independent project, looking at just how much **good, strong** inference you can squeeze out of the data.

Modules needed (to run most of analysis):
+ NumPy, Pandas, matplotlib
+ skimage, scipy, sklearn
+ Basemap

Features:
+ 2D histograms
+ Extrapolation through RBF
+ Lloyd Algorithm & spectral density clustering
+ Region selections

Format is in Jupyter notebook so that you can run section of the code you desire. 

Included in the future (in the works, when I get the time):
+ ROI selection (physically selecting stations)
+ Time series on traffic
+ Traffic flow interpretation
+ Periodogram and butterworth filtering
