# Classifying Star Type Based on Numerical Data

## Problem

The problem I tried to solve was classifying the type of star based on the data that was given. I tried to use the numberical data instead of the data that seemed more abstract, such as color and spectral class. This means the variables available are temperature, radius, luminosity, and absolute magnitude.

Note: I had the idea to try and determine the other classifications (color and spectral class) based on the numerical data as well, but I ran out of time.

## Treating the Data

I first researched the variables to determine what they all meant, and realized that absolute magnitude was similar to luminosity. Absolute magnitude seemed to be more consistent and was related to the logarithm of lumiinosity, so I determined that focusing on absolute magnitude and removing luminosity as a variable was sometihng I wanted to do. This relationship can be seen by the first graph in the notebook.

## Finding relationships in the data

Additionally, since there were only 240 samples, I decided that I could try visualizing the data to try and find relationships in the data. Using pandas and matplotlib, I made a function that would input the two variables to graph with each other, and then color each of the points according to star types.

The relationships I found were as follows.

1. In the second graph, we can see the yellow points (hypergiants) have a much higher radius than all the other stars. Because of this, all stars over 500 are hypergiants.
2. Additionally, by changing the viewing window of the graph, we see that all the stars with a radius above 50 are supergiants, as shown by the third graph.
3. The remaining supergiants have a lower absolute magnitude than the remaining stars.
4. The third graph further shows that the main sequence all have absolute magnitudes between -5 and 7.5
5. The fourth graph graphs absolute magnitude vs temperature, only looking at the remaining stars. This shows that the brown dwarfs have absolute magnitudes greater than 15.5
6. There is also a clear temperature barrier between red dwarfs and white dwarfs, as shows by the fourth graph.

Using these relationships, I made a function to classify the stars based on data about the star itself.

## Testing

To test the function, I made a function to iterate through the rows of the csv file and using the function on them. It returns the acccuracy rate of the function. In this instance, the accuracy was 1.0, or 100%

## Conclusions

Based on the data that was given, the model works, however, it is unclear whether stars outside of the dataset will always fit the restrictions found based on this data. I tried to make the boundaries in the middle ground of whichever stars they were seperating, but there will always be data points that overlap with each other as more data is added. Since these classifications are usually made based on either the chemical properties or timeline of a star, the boundaries made may not be hard boundaries for the star classifications (Ex. There may eventually be a supergiant that is bigger than a hypergiant, even though that is a boundary I set in this model).

Overall, even though the model works for the dataset, more data is always valuable when trying to make classification algorithms.
