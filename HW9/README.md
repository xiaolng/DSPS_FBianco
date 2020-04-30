## scope
This homework is quite open ended. There is no scheleton notebook for it. 

Use the PLAsTiCC challenge data you used in HW6 and 7 and extract features from the time series via autoencoder. 

Then augment the feature space you used in HW7 with the new features created by the autoencoder, and see if this improves the classification. 

## Challenges

For each object in the dataset there are 7 time series for 7 optical filters. Each time series is composed of a series of time stamps and a series of fluxes (i.e. the time series are sparsely sampled).

1. Choose if you want to treat each filter for each object separately, or together. From a domain point of view, the relationship between what happens in different filters (i.e. at different wavelengths) is important. From a practical point of view ignoring it may be easier. 

2. You must choose a common time frame for all observations: for example for each object choose the timestamps of the first observation and set it to 0. Cound time forward in days from that point. 

3. Choose if you want to interpolate the time series (e.g. linear interpolation, spline, gaussian processes) and extract evenly sampled values or you want to deal with the sparsely sampled time series. 
 - in the first case you will create a function f(t) that allows you to extract the flux at N points in time. Now your time series are evenly sampled. This is the best option, i.e. the option that gives you the best chance of getting a good result, but you will have to work out the interpolation which may not be easy. It is not mandatory.
 - in the second case you need to preserve the time stamps and reprganize the time series accordingly. 
 
 Consider an image: it is a NxN object. To feed it to the NN you flatten it: 
 
      A1|A2|A3|A4|A5
      B1|B2|B3|B4|B5
      C1|C2|C3|C4|C5
      D1|D2|D3|D4|D5
      E1|E2|E3|E4|E5



