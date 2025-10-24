# DATABOOTCAMPMIDTERM
Project Title: Institutional Ownership and Urban Housing Markets — LA • NYC • Miami • Philadelphia

API's used: ATTOM API, American Bureau Census API, Redfin Databank (CSV download)

By: Lola Serdan, Lucas Lee, Antonio Vieira

Main Guiding Question: How have real estate sales trends (volume and prices) evolved over time in major U.S. cities, and how do those trends relate to demographic and housing characteristics from the U.S. Census?

Introduction:

Our project began from a shared interest in how cities grow, change, and evolve. Each of us started this project with different backgrounds(even countries), having interests in real estate, data analysis, and urban studies, but we were united when cultivating the idea, asking how data can help us understand the evolution of housing markets and the forces shaping modern cities. 
All of us who have grown up in major cities have come to understand that numbers never tell the full story, whether that's in the real estate market (such as buying a home) or something else entirely. One of us came to NYU already obsessed with the prospect of a career in real estate, having been raised in Los Angeles and visited numerous open houses, off-market luxury listings, and engaged in casual dinner-table talk about the health and state of the market. Another had spent months buried in insurance data over the summer, crunching numbers using Python, but never connecting to an API. The third has been reading about gentrification in New York and various other cities, like Miami. Understanding it not as an abstract force, but as an uncomfortable truth, one tied to institutional investors buying entire city blocks, reshaping and cherry-picking who gets to live where. Each of us had our own reason to care and to try. Together, we wanted to turn our curiosity into something measurable, quantifiable, and most importantly, visual. This led us to our central guiding question: What relationships can be observed between housing prices, population changes, and institutional investor activity across major U.S. housing markets from 2018 to 2025?

Code Structuring and Development (see comments in the Jupyter Notebook):

We started with a simple, ambitious, and seemingly bulletproof plan, which, to our surprise, wasn’t quite true. Our central idea floated around connecting the dots between market movement and urban change. Our first engine of data was the ATTOM API, which thus called a function to locate a city name within ATTOM’s innate geography identifier(GeoIDv4). After this, our code requests extractions of historical data and sales trends, listing: average price, median price, and volume of transactions. Behind each computed result in a cell is a conversion to location names, I.E., Los Angeles, Miami, and so forth. Next, we layered in figures to give context to our housing data. Using the United States Census Bureau’s ACS API, we could understand the relationships between things like a city's population and median sales price. This API aided in turning out rather bland-looking data into a narrative, offering insights on supply, demand, change, and overall evolution. Subsequently, we merged the datasets so that for each time point, we could say: “Here's what the city did in sales, here's the price range of houses, and here's how many sold, in set year.” Suddenly, we could figure out insights via our charts, hinting at neighborhoods aging, demand surging, supply lagging, and cities reshaping themselves.
Bringing everything together, the last feature of our Colab Notebook, graphs, became our way of translating the data. For Boston, the dual-axis chart shows averages in sale price against population and time, showing a steady climb, showing the city expanding not just economically, but demographically as well. The two lines rise nearly in tandem, suggesting that Boston’s price appreciation is bound to a growing demand from the people who actually live there. New York tells an entirely different story; its line and trends waver every year, displaying the huge volatility of such an ultra-massive City, like the Big Apple. Miami’s chart moves without hesitation; we can speculate that the surges were a result of things like migration patterns and new era wealth brought about by the pandemic. The city reflects a market more similar to a new brand, where everyone wants in. And then there’s Los Angeles, where two contrasting lines, average sale price and home sale count, pull in opposite directions. Prices ascend while the number of sales fluctuates and falls, hinting at scarcity, competition, and a whole new world of wealth disparity. This graph reflects the notion that demand won’t quit and is met by a supply that can’t keep up.
Gentrification is both a social and economic transformation, and our project captures how it unfolds through data. By combining real estate data from ATTOM, demographic data from the U.S. Census, and investor activity from Redfin, we were able to create visualizations of the issue that has been changing neighborhoods across America by rising home prices, shifting populations, and concentrated ownership. Our findings connect closely with Elora Raymond and John Humphries research,  “Keeping Up with the Blackstones”. The research demonstrates how institutional investors, including private equity firms, drive up property values and accelerate neighborhood change through large-scale home purchases. These investors normally concentrate their property purchases in specific neighborhoods, allowing them to control local markets. With this control they increase rents,  and reduce affordability. While Raymond and Humphries note that some areas show slight increases in diversity due to more rental housing, the overall pattern reveals a widening economic divide and erosion of community stability.
In our data, we saw similar trends: investor share increased significantly in cities like Miami and Los Angeles, aligning with growth in both median sale prices and transaction volume. These findings mirror the patterns documented by Raymond and Humphries and highlight the growing influence of large investors in shaping housing access. They also represent what is shown in Class Divide, the HBO documentary that explores gentrification in Chelsea, NYC, where luxury housing and private education develop next to public housing projects. One of our group members witnessed this problem while attending school in Chelsea, watching how investment and development transformed the community. That personal experience motivated our analysis and made the data feel more human instead of just numbers. Through this project, we wanted to show that gentrification is not only visible in the cities around us, but also measurable in the numbers revealing how concentrated ownership and rising investment reshape neighborhoods.  
After coming to understand the function of RedFin’s API, which is a database that shows what percent of outstanding properties are owned by institutional investors vs families, and a great list of other insights. We brought in our data from ATTOM and Census, as we mentioned before. RedFin’s data helped us understand that the housing market isn’t just about supply and demand, but who and which entities drive the supply and demand. RedFin’s API tracks the share of homes owned by institutional investors compared to individual homeowners and co-op tenants. RedFin’s data allowed us to quantify the growing footprint of large-scale residential and commercial investors, made up of private equity firms, REITs, hedge funds, and so on. Many cities' residential markets were once dominated by families, but by merging our data, we found a way to carve out the map of ownership concentration against real-world housing outcomes.

Graph Analysis:

	After we got our data, we created different forms of graphs to help us visualize and understand the information. For each city we created four graphs: 1. Average Sale Price vs. Home Sale Count (Yearly), which compares housing prices to transaction volume; 2. Institutional Ownership Over Time, which tracks the rise of investor market share; 3. Investor Share vs. Average Sale Price, which measures how investor activity correlates with housing prices; and 4. Correlation Heatmap (Selected Variables), which displays the relationships between multiple factors such as price, population, housing units, and investor presence. 
(1) - Average Sale Price vs. Home Sale Count (Yearly), which compares housing prices to transaction volume
In all four cities, as the average sale price increased, the number of home sales declined. This trend makes sense when considering the dynamics of supply and demand, when prices go up past what typical buyers can afford, less people are able to purchase homes, resulting in a drop in sales volume. This pattern is most visible in Miami and less visible in New York City.
(2) - Institutional Ownership Over Time
Across all four cities, the institutional ownership graphs show a noticeable dip around 2020, followed by a sharp rise in the years after. This drop aligns with the early stages of the COVID-19 pandemic when the market was very unstable. However, as the housing market recovered, investor activity not only returned but grew even stronger. By 2022 and beyond, institutional market share in cities like Miami and Los Angeles climbed rapidly, suggesting that investors took advantage of low interest rates. After the pandemic, institutional investors quickly returned to the market, strengthening the same trends of ownership concentration and reduced affordability that our project explored.
(3) - Investor Share vs Average Sales Price
Across LA, NYC, Miami, Philadelphia over , the charts suggest a clear positive relationship between investor market share and average sale prices: when investor share rises, prices tend to increase as well. This ties back to our original discussion and shines light on the fact that the more present institutions are in the real estate market, the harder it is for an everyday person to afford to live in the city. 
(4)  - Correlation Heatmap(Selected Variables)
On average, periods with higher sales volume coincide with higher prices. The correlation heatmap shows moderate links between multifamily units sales and institutional investor ownership, while the relationship between single and multi family units in the cities appear limited, with the exception of Philadelphia, which seems to have a balanced number of single and multi family houses.
In the 4 studied cities, population does not seem to have any relevance to average sale prices. 

Conclusion:

In the end, we feel confident to say that we built not only a code, but a map detailing the way that cities evolve. Though simple, our code can act as a microscope with graphs acting as different lenses. It felt satisfying to run each cell, culminating our hard work into an astute, yet quiet finished product, which combined our collective passions with very real and significant data. By connecting multiple API’s, ATTOM for property sales, US Census Bureau for population and housing, and RedFin for ownership architecture. We created a framework that tracks the relationship between people, prices, and investors and how they interact over the years. Each step of the process and integration taught us and gave us a clear understanding of which forces shape the housing markets.





























Works Cited


ATTOM. ATTOM Data API. ATTOM Data Solutions, 2025, https://api.developer.attomdata.com/
	https://api.gateway.attomdata.com/v4/location/lookup
	https://cloud-help.attomdata.com/article/579-geocodes


Redfin. Redfin Data Center API. Redfin Corporation, 2025, https://www.redfin.com/news/data-center/

U.S. Census Bureau. American Community Survey (ACS) API. United States Census Bureau, 2025, 
https://www.census.gov/data/developers/data-sets/acs-5year.html
https://www.census.gov/data/developers/data-sets/acs-1year.html



HBO. Class Divide. Directed by Marc Levin, HBO Documentary Films, 2016.

Raymond, Elora, and John Humphries. Keeping Up with the Blackstones: Institutional Investors and the 
Race-Class Geography of the Housing Market. Federal Reserve Bank of Atlanta, Community and 
Economic Development Department, 2023. 


