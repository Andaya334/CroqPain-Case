# CroqPain-Case
Prediction model to forecasts which location yields best return on investment


●	Michel Boutillon asked by company president, Jean Gerard, to make a presentation
●	He was hired 2yrs ago to be a transition manager for Croq’Pain (fast food chain)
●	Responsible for preparing restaurants before they open
●	He has been asked to develop a better system for the selection of locations for newer stores
●	Performance from 7/10 stores that opened in the first half of the year were less than satisfactory

The Company

●	Founded by Jean Gerard in 1981 in Paris
●	Opened 2nd restaurant 6 months later targeting student clientele 
●	Opened other restaurants of his were opened during the next 5yrs
●	Goal: offer quality food… fast, not fast food
●	By 1987, 15 stores in Paris, Toulouse and Marserlles
●	1987, poor financials led to marketing survey of customers
○	Survey review revealed that customer base were professionals and baby boomers
●	New stores concentrated in areas that served this clientele and away from student neighborhoods
○	Withdrew from the competition with other fast food chains
●	Now stores concentrated in downtown areas and business centers
○	Strategy paid off and expanded the company at a steady pace
●	Company owned 50 stores throughout France by 1994
●	Construction Department of Croq’Pain controlled all new store openings
○	Responsible for selecting the location of new stores

The Croq’Pain Concept
●	Croq’Pain took advantage of workers eating lunch around their jobs because they lived to far from work to commute back home for lunch and come back to work.
●	Croq’Pain offered sandwiches, salads and pies; they served a variety of drinks as well
●	They did not offer the lowest prices but rather a good mix of quality food, based on French traditions, and price
○	Also offered convenience and a unique look

The Construction Department
●	Employs 40 people (architects, lawyers, designers, accountants, and construction workers)
●	Process of launching a new restaurant begins approx 1 year before restaurant’s scheduled opening date
●	Steps include:
1.	Choice of location: city and location of new store
a.	company determines investment needed to open store
i.	Includes building and land as well as equipment
2.	Property acquisition: building or land purchased (or possibly leased)
3.	Design: new store design during property acquisition stage
a.	It’s finalized during the property acquisition stage
4.	Remodeling and/or building: Actual construction of store
5.	Logistics: prior to opening, transition manager steps in to oversee logistical problems (installation of proper equipment, local supply chain, and staff)
6.	Opening Day: morning ceremony, transition manager passes keys to store manager and store opens same day

●	Transition manager moves on after opening day to next assignment
●	Store manager adjust workforce during the year, and adjusts the store’s operating hours to a lesser extent
●	Location setup determines the company’s future earnings to a large extent
○	Its been an imperfect art determining the store’s location and size
●	Company has a growing need to standardize location selection process and minimize the risk of failure
●	Usual procedure: 
○	location expert chooses several possible options, 
○	makes an earnings potential estimate of each location,
○	 then a recommendation to company president and the director of construction
●	Director of construction: Didier Marchand

Developing a Model for the Selection of Store Locations

●	Michel gathered location selection experts to devise ideas for the structure of the model
●	Independent variables of the model were to be those variables that they thought would influence the profitability of a new store
○	List established is on table 6.25
●	Michel collected data on all stores
○	Data of stores after 1994 were incomplete and could not be used
○	Operating earnings is shown for July 1994 to June 1995
○	He ran a regression of earnings figures using all the parameters of the model (table 6.27)
●	He did not like the first result and needed to improve the initial model
○	He didn’t like the choice of certain parameters because it had little value for predicting financial results
○	Homemade parameters were of little use, which were made by the experts
●	Michel had serious doubts about the feasibility of such a model-based approach for selecting store locations
●	He was uncomfortable with his regression model
○	Some coefficients didn’t make any sense, and weren’t statistically significant
○	Needs improvement
●	He thought of a good way of testing the applicability of the regression model was to consider what would have happened last year had the model been used to evaluate and select the 1994 store locations
○	He would need to amend model to use data obtained for the first 50 stores
○	Then he would use this regression model to evaluate the ten stores that were opened in 1994
●	Croq’Pain Goal: 16% return on invested capital after taxes
○	They define their “performance ratio” for the store as:
  
○	Target performance = 0.26 = 26%
●	Michel needs to consider his recommendations for new stores for 1996
○	Experts made 10 locations (see table 6.28)
○	Michel wanted to use model to help him select potential locations of stores to be opened in 1996
●	He needs to prepare his presentation to executives using definitive arguments
○	Needs to offer strong arguments for or against using a regression model
○	Needs to point out possible shortcomings of the model methodology

Questions
### Part (a)

Visualize the data: examine histograms and scatterplots. Look at correlations between variables and try to identify sources of concern. Pay particular attention to the correlation for `total` and `P15` through `P55`. Do these correlations make sense to you?

Apply a transformation to the variables `EARN`, `P15`, `P25`, `P35`, `P45`, `P55`, `COMP`, `NCOMP`, and `NREST` where you normalize them by `total`. You can apply this normalization by defining new variables such as `EARN_total` which is equal to `EARN` divided by `total`.

Evaluate correlations and regressions with both the transformed and un-transformed data. Which do you prefer and why?

When you run regressions, be sure to use the `VIF` feature in Radiant for a more rigorous evaluation of multicollinearity. As you are building a model, it can also be useful to examine standardized coefficients. Also, conduct linear regression validation checks by using the `dashboard` plots in the `Plots` tab (see section 6.6 in the book).

If interested, you can experiment with the `Stepwise selection` option in the _Summary_ tab (i.e., click the checkbox) in the R version of Radiant (launched from RStudio). This is a feature in Radiant that uses a purely statistical approach to model building based on the Akaike Information Criterion (AIC). It will go through a series of steps and recommend a final model (see the bottom of the output). Compare the model selected using `Stepwise selection` to the model you arrived at yourself. Be critical and make a decision about the final model to recommend for Croq`Pain.

### Part (b)

Remember to use a subset of the `CroqPainFix` data with only the 50 stores opened up prior to 1994. After you build your regression model using `CroqPainFix` select the `Predict` tab in Radiant.

### Part (c)

This part can be completed using the same Radiant features applied earlier.
