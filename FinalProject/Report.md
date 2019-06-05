# Targeting Consumers According to Venue Categories

## Introduction/Business Problem

Is a person visiting an art gallery likely to next visit a French restaurant? Is a person visiting a metro station likely to next visit a tailor shop? In general, is a person visiting a venue of category *x* likely to next visit a venue of category *y*? In this project, pairs (*x*, *y*) were found for which the answer is Yes.

This problem is relevant for delivering targeted advertising. Advertising seeks to change consumer behavior, but the most likely changes are those that remain within the bounds of normal behavior. Let *P*(*x*, *y*) denote the probability that a person visiting a venue of category *x* next visits a venue of category *y*. If *P*(*x*, *y*) is high, then it makes sense to advertise venues of category *y* to people currently located at venues of category *x*.

## Data

Data for this project came from Foursquare. Foursquare has a large database of venues. Each venue has a category. Many Foursquare users frequently notify Foursquare that they are currently located at one of these venues. This is called "checking in" at the venue.

The Foursquare API includes a feature called "Get Next Venues". Here is the description from [the API documentation](https://developer.foursquare.com/docs/api/venues/nextvenues): 

> Returns venues that people often check in to after the current venue. Up to 5 venues are returned in each query, and results are sorted by how many people have visited that venue after the current one. 

The output of this feature also includes the category of each returned venue.

This feature was used to obtain next venues for 10,000 randomly selected venues in the vicinity of Los Angeles, California, USA.