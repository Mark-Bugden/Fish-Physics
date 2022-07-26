# Summary
This file collates and cleans the data contained in the *1024 sunbleak* subfolder of the *Data* folder. It also does some minor data exploration

### Collating
In the original dataset, each fish is given an individual .npz file with the tracking data associated to that fish, including x position, y position, frame number, and time. This ipython file collates those individual files into a single Pandas DataFrame, df. The columns of this dataframe are ["Fish", 't', 'x','y', 'frame'] corresponding to the fish number, the time, the x position, the y position, and the frame respectively. 

### Cleaning
The file also replaces invalid data - when the tracking software is unable to resolve two fish, it returns a value of 'inf' for the x position and y position. The file replaces all such occurances with an approximation of the actual x position and y position of the fish. 

### Exploration of data
The file plots example fish trajectories, fish positions at given frame, and heatmaps for the fish positions at a given frame and averaged over the whole dataset. Two interesting observations arose: 
  * Averaged over the whole timeframe, the fish tend to congregate at the edges of the tank
  * There are some minor stitching artifacts from when the four videos were stitched together to create one video
