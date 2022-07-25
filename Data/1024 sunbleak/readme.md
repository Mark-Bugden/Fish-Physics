## Source and licensing of data
[Source](https://dx.doi.org/10.17617/3.4y) and [license](https://creativecommons.org/licenses/by/4.0/) of data, which is part of the source material for the [paper](https://doi.org/10.7554/eLife.64000).

## Context for the data
[TRex](https://trex.run/docs/) is a tracking software designed to track and identify individuals and other moving entities using computer vision and machine learning. The data consists of tracking data from approximately 1024 fish (Sunbleak) in a 3m tank. 

## Description of the data
The subfolders in the *1024 sunbleak* folder contain the tracking observations for subsets of fish. Although there were approximately 1024 fish in the experiment, there are more than 1024 fish observations since occasionally the tracking ID of a fish was lost. 
* *1024 sunbleak*
  * *Fish 0-99*
  * *Fish 100-199*
  * *Fish 200-299*
  * ...
  * *Fish 1100-1125*
  
The source data is identical to the data contained here, although I have subsetted the observations into subfolders to make uploading to github easier. The files contained in the subfolders are .npz files containing the observations about an individual fish. 
