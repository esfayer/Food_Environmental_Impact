# Food Environmental Impact


Analysis of Environmental Impact by Food Item

### MOTIVATION
I’ve been an off/on pescatarian for the last several years, and for the last few months, I’ve eaten a vegan diet. While the primary reason for these dietary choices is a regard for animals, concern for the environment is a commonly cited reason for many. However, almond production requires large amounts of water, meaning producing almond milk can potentially be less environmentally sound than the raising and milking of cattle. This begs the question: what other dairy and meat alternatives wreak havoc on the environment? Is the focus on the methane excreted by cows misguided, or at least not fairly compared to other deleterious food production methods?


The main question I set to answer was: which diet is the most environmentally sustainable between vegan, vegetarian, and omnivore?



### DATA
I pulled data on many food groups and their impact on their environment by different measures. I then isolated foods that did not have null values for four main impactors of the environment: greenhouse gas emissions, land use, scarce water use – a weighted measure of water use based on the scarcity of water in the location of food production, and eutrophying emissions – pollution emitted into local water sources as a result of food production. This limited my data set to 30 foods/food groups.


### ANALYTICAL APPROACH
Known Issues and Challenges:
•	Difficult to find data on exact how much of each food group an average person eats, broken down by diet-type
o	This is incredibly difficult information to find in general, but even more difficult when you consider that, for example, the average vegan likely eats more beans than the average omnivore, which would be a critical nuance in this study.
•	Difficult to aggregate the four measures in a meaningful way
o	Ie no way to convert square miles to liters

In order to get by without the data to make this complete, I had to format my dashboard based on two assumptions:
1)	Every person eats the same amount of calories every day
a.	Because no additional data is present regarding how much of each food group is consumed per person, it is assumed that everyone eats the same amount.
2)	Every food group is broken down evenly into that calorie count.
a.	Because each environmental impact measure is based on 1000kcalories of said food, it is assumed that each person eats the same calories-worth of each food group as another.

While in the extreme cases this skews the data greatly (it takes about 1000 cups of coffee to reach 1000 kcalories, vs. half a cup of palm oil to reach the same calorie count), the extreme cases are mostly in regards to foods that would be included in every diet. Therefore, while the customized table may not be accurate, the comparison between the different diets can be assumed to be close to accurate.


My project resulted in three different views.

The first is a list of the 30 food products with the aggregate impact on the environment. For this view, each of the foods was broken down by percentiles throughout the four measures so that each of the measures was weighted equally. The closer to 4 the aggregate is, the more detrimental it is on the environment.





The second view shows the foods in an area chart based on environmental impact as well as the top 10 environmental impactors in a bar chart. A user can click through the drop down to see which foods are most impactful by measure, or select All to see it in aggregate.



The third and final view was the MVP – a dashboard showing the different diets’ impacts on the environment. It also includes a Custom bar, where a user can check off whatever foods they eat to see how their impact changes, as well as how it compares to different diets.


### CONCLUSION
Based on my analysis, despite nuts being impactful on the environment, a plant-based diet is still the least harmful to the environment. As the final image shows, while removing nuts does improve one’s effect on the environment, it does not impact it as much as removing meat or dairy altogether. (For example, one can see that the omnivore who doesn’t eat nuts still impacts the environment more than a vegetarian who does.)


### TOOLS USED
•	Excel – data came in CSV format
•	Python/Pandas – data was cleaned and pared down
•	Tableau – for creating the interactive dashboards
•	Git for updating and maintaining versions



### SOURCE
https://www.ers.usda.gov/data-products/food-consumption-and-nutrient-intakes/
	Source: USDA


### TABLEAU
Please follow [this link](https://public.tableau.com/views/FoodEnvironmentalImpact/CapstonePresentation?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link) to find my Tableau story, including my question, why I researched it, caveats/assumptions, and my interactive dashboards.
