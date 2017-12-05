# Transform

Before making visualisation, it is often required for the dataset to be transformed. We can use the `transform` key to do these transformations.

- **Bin**: Convert continuous data to categorical bins (e.g. for histograms)
- **Filter**: Create a smaller subset of the data
- **Calculate**: Derive new variables based on a calculation
- **Aggregate**: Summarize and group data (e.g. min, max, sum, ...)
- **Sample**: Select a sample of the data 
- **Reshape**: Change the shape of the data (e.g. tall <-> wide) *// Not supported*

These transformation are applied in a sequence, so it is denoted as an array of transformation in the code.
