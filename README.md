# Data-in-Dating
Analyzing important features in speed dating data, and then matching algorithms like Gale Shapley and maximum weight to find the largest number of compatible matches
## How might a dating app decide who to match?

### Dating apps sell people on finding love, and different apps run differently depending on what they are trying to advertise.

1. One app might advertise that it will send you your dream match.  In this case members see many others they might be interested in, but the interest may not be reciprocal.  This business model may keep clients on the app longer in hopes of their dream match finally accepting them, even though the other member may not reciprocate as often as they would like. We use the <u>maximum weighted matching</u> algorithm to model this approach.

2.  One app might advertise it produces high quality matches, where both members enjoy high levels of compatibility.  While the level of 'dreaminess' may not be as high as the first app, it can advertise more reciprocation. We use the <u>Gale-Shapley</u> algorithm to model this approach.

In this project we will analyze speed dating data to determine which factors are most important when a person decides whether to accept a match or not.  Then we will use these important features to determine which algorithm would make the best suggestions, depending on whether we are using dating app model 1 or 2.

The <a href="http://www.stat.columbia.edu/~gelman/arm/examples/speed.dating/">data</a> we use was compiled by Columbia Business School professors Ray Fisman and Sheena Iyengar for their paper<a href= "https://www0.gsb.columbia.edu/mygsb/faculty/research/pubfiles/867/datingFULL-EK1.pdf#:~:text=We%20study%20dating%20behavior%20using%20data%20from%20a,while%20femaleselectivity%20is%20strongly%20increasing%20in%20group%20size"> Gender Differences in Mate Selection: Evidence From a Speed Dating Experiment. </a>  They collected data from 21 speed dating events to analyze their decisions.

### Conclusion and future directions
-The largest number of acceptances from women was 65.8% from maximum weighted matches based on like, and was 58.4% from Gale Shapley with women proposing based on like. The largest number of mutual matches was 36.1% from maximum weighted matches based on like, and was 40.1% from Gale Shapley with men proposing based on like. It was expected that the maximum weighted matchings would get more acceptances from women than Gale Shapley. While Gale Shapley produced more mutual matches than weighted matches, it is interesting that the percentages are not far off, considering that the maximum weighted matchings don't take into account men's preferences! Even if a dating company had a goal of optimizing mutual matches, perhaps it might still benefit the company to use maximum weighted matchings over Gale Shapley, because it may more likely retain female members who are receiving more acceptable matches.

-The 'like' category seemed to perform best in either matching algorithm. However, a practical difficulty in trying to implement this matching based on like is that we wouldn't know whether she likes him until she sees his profile or meets him in person, at which point we would have her decision anyway. A similar issue may apply to attraction, fun, and shared interests, though we may be able to use image or language processing to get an estimate.

-Perhaps combining some features would predict match acceptances more accurately?
