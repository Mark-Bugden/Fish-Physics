# To-do
* Optimise the data collation. Instead of concatenating dataframes for each fish, concatenate arrays for each fish, and then convert to DataFrame at the end
* Fill in "inf" values using linear interpolation rather than fill forward
* Construct nicer heatmaps for individual frames by smoothing. The answers at [this](https://stackoverflow.com/questions/2369492/generate-a-heatmap-in-matplotlib-using-a-scatter-data-set/59920744#59920744) Stack Overflow question may be useful.
* <del>Obtain velocities from the fish trajectories. A simple difference between consecutive frames is probably sufficient, but I must be careful when the fish tracking 'jumps'. A simple way to implement this is to discard any velocities which are bigger than the maximum speed of a sunbleak. </del> DONE
