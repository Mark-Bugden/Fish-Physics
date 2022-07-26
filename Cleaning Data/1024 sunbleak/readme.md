# Summary
This file collates and cleans the data contained in the *1024 sunbleak* subfolder of the *Data* folder. It also does some minor data exploration.

Note: The file produces and saves a .csv file of the cleaned and collated data, but since the filesize is approximately 1000mb I can't upload it to GitHub. 

### Collating
In the original dataset, each fish is given an individual .npz file with the tracking data associated to that fish, including x position, y position, frame number, and time. This ipython file collates those individual files into a single Pandas DataFrame, df. The columns of this dataframe are ['Fish', 't', 'x','y', 'frame'] corresponding to the fish number, the time, the x position, the y position, and the frame respectively. 

### Cleaning
The file also replaces invalid data - when the tracking software is unable to resolve two fish, it returns a value of 'inf' for the x position and y position. The file replaces all such occurances with an approximation of the actual x position and y position of the fish. 

### Extracting velocities and cleaning them
The instantaneous velcoties of the fish are obtained by taking the difference of the position vectors of a fish at two consecutive frames. Tracking problems can result in a situation where TRex thinks the fish is on one side of the tank in one frame, and on the other side of the tank in the next frame. This results in a huge velocity for that frame, and so we filter out by all velocities higher than the sunbleak maximum speed. 

### Exploration of data
The file plots example fish trajectories, fish positions at given frame, and heatmaps for the fish positions at a given frame and averaged over the whole dataset. It also looks at the distribution of speeds and positions. Two interesting observations arose: 
  * Averaged over the whole timeframe, the fish tend to congregate at the edges of the tank
  * There are some minor stitching artifacts from when the four videos were stitched together to create one video
  * Excluding speeds of zero results in a very smooth distribution. The speeds exactly equal to zero are likely created by the method of imputing missing position values, and should disappear when the more sophisticated method of imputing those values is implemented. 



