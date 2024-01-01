# NASA | DrivenData.org
## The Pale Blue Dot - *Pale Blue Dot*

This challenge proposed by driven data, in conjunction with NASA and NASA Tournament Labs - *NTL*
Is a challenge whose goal aims to achieve the Sustainable Development Goals - *SDGs*
The objectives in focus are: Zero Hunger, Clean Water and Sanitation, and Climate Change

As a data analyst, scientist, or citizen scientist, you must create intriguing visuals that help policymakers make decisions.

Attention: It is necessary to use public data about the USA in your study. Check the available datasets in full at: [Pale Blue Dot](https://www.drivendata.org/competitions/256/pale-blue-dot/)

## How to do a project like this (*but different*)

To build your project, you must pay attention to the following 3 points (not necessarily in order, and it can be cyclical):

- Brainstorming
  - Understanding the problem
  - Building possible solutions
  - Linking available data and problems to solve
- Data
  - Downloading data
  - Understanding the data
  - Transforming the data
- Visualization / Problem Solving
  - Building graphs
  - Validating the data and the constructed graph
  - Question: Does this graph solve the problem proposed in the Brainstorming/Data phase? If not, go back to where necessary

In this case, let's skip the brainstorming phase to train in a specific case:
  Precipitation over ice in Alaska

When asking ChatGPT what would be the use cases for a dataset aiming to understand the ice precipitation index in Alaska, it responded:

> This dataset on the frequency and distribution of rain on snow during cold seasons in Alaska between 2003 and 2016 has several interesting applications. Here are some potential use cases:
> 
> Flood Risk Prediction: Use snow rain patterns to predict the risk of floods during snowmelt in spring. This could be crucial for communities and local authorities preparing for flood events.
> 
> Wildlife Impact: Analyze how rain on snow affects the ecology and behavior of wildlife in Alaska. This can help biologists and conservationists better understand how climate change is influencing animal populations in the region.
> 
> Agriculture and Water Resources: Study how rain on snow affects water levels available for agriculture and other human activities. This could be crucial for water resource planning and agricultural management in the region.
> 
> Climate Change Modeling: Use this data to validate and improve climate models that try to predict future patterns of rain on snow. This can help better understand global climate change and its regional impacts.
> 
> Infrastructure Planning: Understand how rain on snow affects infrastructure, such as roads, buildings, and energy networks, to better plan construction and maintenance in affected regions.
> 
> The reason these use cases are relevant is that rain on snow can have significant effects on various aspects of life and human operations in Alaska. Understanding these patterns may be crucial for adapting to climate change and mitigating associated risks.

Therefore, let's use the brainstorming done by our companion and study at least one of these topics.

In the data phase, we need to download the relevant data for our analysis

In this case, by clicking here, we can see the [data on precipitation in Alaska from 2003-2016](https://search.earthdata.nasa.gov/search/granules?portal=idn&p=C2162145449-ORNL_CLOUD&pg%5B0%5D%5Bv%5D=f&pg%5B0%5D%5Bgsk%5D=-start_date&fi=MODIS&as%5Bscience_keywords%5D%5B0%5D=Atmosphere%3APrecipitation&tl=1703557365.73%213%21%21&fst0=Atmosphere&fsm0=Precipitation)

Remember, it's necessary to register on the website's system before gaining access to view and download the information.
Once you've registered your account, downloading a file is as simple as finding it and clicking a "download" or "download all" button -> and you'll receive a list of URLs to click and download, one by one.

Assuming you've downloaded the file, the last necessary step would be to open the ["ALASKA_rain_on_snow.ipynb"](https://github.com/Birlinha/Pale_Blue_Dot_NASA/blob/main/ALASKA_rain_on_snow.ipynb) file and click the button at the top "Open in Colab"

Within the Notebook, which is the name given to this code interpreter, you'll need to open the tab on the left, where there's an icon of a folder

Inside that folder, click upload and upload the .tif image file downloaded from the Alaska precipitation dataset

After that, simply copy the file's name and input it into the code, replacing the name ABoVE.Rain-On-Snow.2003_Water_Year_Ah000-001v000-001.001.10212018 (1).tif with your file's name

Upon running the entire notebook, it will ask for your permission to access Google Drive and store the file there, inside a folder named rain_on_snow_NASA. If the folder doesn't exist, the file won't be moved, and it won't be possible to take a screenshot of the image

For any difficulties, create an ISSUE in this repository, so we can communicate

## Examples

Some of the projects used as examples in the main article on the [Pale Blue Dot](https://www.drivendata.org/competitions/256/pale-blue-dot/) site are:

- Monitoring greenhouse gas emissions: Use [AIRS](https://airs.jpl.nasa.gov/) data to create a linear graph of emissions from a specific country over time and help policymakers monitor progress on SDG 13 (climate action).
  - For a more advanced example, check the [global map of methane emissions](https://www.earthdata.nasa.gov/learn/articles/methane-fossil-fuel-exploitation) from oil, coal, and gas exploration created for NASA's Carbon Monitoring System.

- Increasing crop yield for subsistence farmers: Combine [HRRR](https://rapidrefresh.noaa.gov/hrrr/#:~:text=The%20HRRR%20is%20a%20NOAA,grids%20with%203km%20radar%20assimilation) climate data with [SMAP](https://www.earthdata.nasa.gov/learn/find-data/near-real-time/smap) soil moisture data to create monthly cultivation condition plots for an agricultural region and help farmers decide what and when to plant.
  - Read about how [Catherine Nakalembe, with NASA's Harvest mission, is supporting farmers](https://www.devex.com/news/how-a-nasa-backed-scientist-uses-satellites-to-help-african-farmers-105010) across East and Southern Africa.
  - Other real-world projects have studied [subsistence farming in Bhutan](https://storymaps.arcgis.com/stories/e36505aa74ea474d9de8db3271ece80a) and [rice in the western United States](
