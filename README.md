# Chicago "L" analysis
Analyzing Chicago's L System for optimal location to start a restaurant business. Takes into account both spatial coordinates, and traffic density. Originally for a data science challenge, but now for an interest independent project, looking at just how much **good, strong** inference you can squeeze out of the data. Format is in Jupyter notebook so that you can run section of the code you desire. 

### Requirements (to run most of analysis):
+ NumPy, Pandas, matplotlib
+ skimage, scipy, sklearn
+ Basemap

### Features:
+ 2D histograms
+ Extrapolation through RBF
+ Lloyd Algorithm & spectral density clustering
+ Region selections

### Complications
+ being able to overlay a google maps or a physical map of the traffic onto our results or plotting them has been a challenge. The problem with this is that the results we get are in terms of meters or coordinates (degrees), but the image of the map when we import it, is a 2D array of value coordinates starting at 0,0. The only way to resolve this is to either map the map (haha) to the data, or squash the data into an image format. 
+ running clustering algorithms including the weights. Because most clustering algorithms deal with counts, rather then weights on a single data point, it was a challenge to be able to map it such. The brute force mechanism would be to add duplicates for each additional count, but that would blow up our data, so instead we included an args parameter to include the weight.
+ plotting with color -- it never worked for me, always had grayscale. I wasn't sure why..but gray scale isn't bad. It may not be visually as bright,but it may be easier to interpret in our case.

## Origin Story
I was posed with an open-ended investigation for a data science position, to look at the data acquired from this L-System in Chicago, and infer some useful set of knowledge from this data. The problem was a bit more specific, and a bit more product driven, and because of the rich and delicious history of Chicago and the eats, I dedicated it to the local restaurant businesses that made Chicago what it is today. What started as a timed project turned into something I think is rather beautiful -- unfinished and rough on the edges, but beauitful. 

During that time, I learned the basics of map plotting, of other ways to go about clustering, and ultimately making use of categorical data in a quantitative sense.

### Included in the future (in the works, when I get the time):
+ ROI selection (physically selecting stations)
+ Time series on traffic
+ Traffic flow interpretation
+ Periodogram and butterworth filtering
