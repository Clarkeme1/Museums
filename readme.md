## Museums Across the United States Per Capita

In this Project, I wanted to explore museum data across the United States. To highlight the states that have dedicated themselves to preserving their history, I compared the raw museum counts against population data, which revealed some interesting observations. 

Based on raw numbers alone, massive states like California, New York, and Texas naturally show the highest number of museums. However, when looking at data per capita (calculating the number of museums per 100,000 people), states like Vermont, Maine, and Wyoming surprisingly rise to the top. I had a lot of fun compiling the data for this interactive web map, and I am excited to use these insights to guide my future research and museum visits! 

#### Code and Data Collection 

- Leaflet Library.
- Languages: HTML, CSS, and JavaScript.
- The population data I got from [2026 U.S. Census data](https://www.census.gov/newsroom/press-kits/2026/national-state-population-estimates.html).
- The raw museum count I got from the [Institute of Museum and Library Services](https://www.imls.gov/). I organized it and calculated per capita in my own excel spreadsheet. I then loaded my downloaded CSV file into [GeoJson.io](GeoJson.io) and loaded that into VS Code. 
- The base map I downloaded from [Leaflet Providers](https://leaflet-extras.github.io/leaflet-providers/preview/).
- The US States outline I downloaded from [GitHub](https://github.com/PublicaMundi/MappingAPI/blob/master/data/geojson/us-states.json).

#### Major Map Functions

The purpose of this application is to compare museum data per capita across the United States. I chose to display this data using a proportional symbol map because I was working with per capita data. Circle symbols represent specific locations or concentrations rather than uniform shading across a landscape. Proportional symbols also allow for a better representation of the data without introducing bias towards geographically larger states. 

This approach creates an overall cleaner design, with clear focal points for interactive tooltips. When the mouse hovers over a state, both the physical state outline and the proportional symbol are highlighted. This allows users to identify exactly which state they are interacting with. The highlights only appear when the mouse is directly over a state and disappear when the mouse moves away, creating a clear and intuitive interactive experience. 

I also added a bound pop-up containing information about each state, which the user can easily close once they have finished reading. To keep the map simple and easy to understand, I created a nested legend that clearly communicates the data. Additionally, I included a descriptive text box in the lower left corner to provide readers with accessible context and help them better understand the information presented. Finally, I kept the overall style of the map white, simple, and easy to read. 