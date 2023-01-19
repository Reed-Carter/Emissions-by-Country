# Emissions-by-Country

#### By [Ruben Giosa](https://github.com/rgiosa10), [Reed Carter](https://github.com/Reed-Carter), [Chloe (Yen Chi) Le](https://github.com/ChloeL6)

#### This repo includes exercises for working with datasets using pandas working as a team. 

<br>

## Technologies Used

* BigQuery
* Looker Studio
* Python
* Pandas
* Git
* Markdown
* JSON
* NumPy
* `.gitignore`
* `requirements.txt`
  
</br>

## Datasets Used

1. [World Energy Consumption](https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption)
2. [Emissions by Country](https://www.kaggle.com/datasets/thedevastator/global-fossil-co2-emissions-by-country-2002-2022)
3. [Latitude and Longitude for Every Country and State](https://www.kaggle.com/datasets/paultimothymooney/latitude-and-longitude-for-every-country-and-state)

</br>

## Description

This repo includes an ETL pipeline leveraging the different datasets highlighted above. The team began by identifying the different agr

 working with a team. Alejandro performed profiling, cleaning and transformations on the [Global Cost of Living](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living), and exported to a clean version of the csv named `cost_living.csv`. Drew worked on profiling, cleaning and transformations for the [World Happiness Report 2021](https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2021) and [World Happiness Ranking](https://www.kaggle.com/datasets/anamvillalpando/world-happiness-ranking) data sets to merge into `world_happiness_clean.csv`. Ruben performed profiling, cleaning and transformations on the [USA Real Estate Data](https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset) to compile `clean_realtor_data.csv`, and then joined the other contributors' datasets into one consolidated csv file. The realtor and cost of living data were concatenated in order to expand the data set for price per square meter data at the city level. Then that expanded data (`cost_living_with_realtor.csv`) set was merged with `world_happiness_clean.csv` into the consolidated `cl_real_happiness.csv`.

Once the datasets were cleaned and consolidated, the team created (and in some cases recreated) data visualizations and analysis using `cl_real_happiness.csv`. In the `rg_maps.ipynb` notebook is a geo heat map of life expectancy by country that was put together by Ruben. Below is the output of the visualization:

<br>

![life_exp_map.png](./images/life_exp_map.png)

Drew put together a pie chart highlighting the life expectancy for the top 10 countries. Code for the visualization is located in `dw.ipynb`. Below is the pie chart:

<br>

![lifeexpectancy.png](./images/lifeexpectancy.png)

Drew also put together a line graph highlighting the happiness score for the top 10 countries. Interesting note is there seems to be correlation between Happiness and Life Expectancy with the two showing the same exact top ten countries. Code for the visualization is located in `dw.ipynb`. Below is the line chart:

<br>

![worldhappiness2021.png](./images/worldhappiness2021.png)

<br>

Drew compiled a map highlighting the happiness score for all countries. Code for the visualization is located in `dw.ipynb`. Below is the output of the visualization:

![happiness_geo_heat.png](./images/happiness_geo_heat.png)

<br>

Alejandro put together a map visualization using Folium, that shows the average price per square meter by state. Code for the visualization is located in `alex_work.ipynb`. Below is a snapshot of the visualization, as it is a dynamic map so in the notebook you can zoom in and out:

![p_per_sq.png](./images/p_per_sq_meter.png)

Alejandro also used geopandas to create a similar map on a global scale: 

!['p_per_sq_meter_global2.png'](./images/p_per_sq_meter_global2.png)

Ruben created a scatter plot visualization that shows the average price per square meter against life expectancy and social support, for 10 countries with the highest life expectancy. Code for the visualization is located in `rg_scatter.ipynb`. Below is a snapshot of the visualization:

![scatter_plot.png](./images/scatter_plot.png)

Overall, the team was able to limit the amount of merge conflicts by working on independent notebooks and assigning different tasks (e.g. Each focused on different data sets, Ruben completed README, etc.). One challenge that we underwent was version control for the datasets that were transformed and then needed to be leveraged by the broader group. One key learning we had was going forward a good practice to help mitigate this is to spend time as a group validating the final data set, agree its ready to be leveraged, and then go on to begin our data visualizations and exploration. This would prevent having version control issues and digging through code to ensure its reading from proper csv files.

## Individual Work Outside the original scope of project by Ruben Giosa:

Created a scatter plot visualization that shows the average price per square meter against life expectancy and social support, for 10 countries with the highest life expectancy. Code for the visualization is located in `rg_scatter.ipynb`. Below is a snapshot of the visualization:

![scatter_social_support.png](./images/scatter_social_support.png)

In addition to the scatter plot view above, in `rg_dynamic_scatter.ipynb` I created additional functionality that allows a user to filter by either 1) 10 countries with the highest life expectancy or 2) 10 countries with the highest social support. This is accomplished by an input requested by the user and then utilizes branching logic to filter the data set.

Finally, I cleaned, transformed and merged a new data set (`countries and continents.csv`) with the `cl_real_happiness.csv` which is consolidated in the newly created `data_with_continents.csv`. I then added functionality that allows a user to filter by continent to see 1) 10 countries with the highest life expectancy or 2) 10 countries with the highest social support by continent. This is located in the `rg_dynamic_scatter.ipynb`.

## Setup/Installation Requirements

* Go to https://github.com/rgiosa10/team-week.git to find the specific repository for this website.
* Then open your terminal. I recommend going to your Desktop directory:
    ```bash
    cd Desktop
    ```
* Then clone the repository by inputting: 
  ```bash
  git clone https://github.com/rgiosa10/team-week.git
  ```
* Go to the new directory or open the directory folder on your desktop:
  ```bash
  cd python-team-week
  ```
* Once in the directory you will need to set up a virtual environment in your terminal:
  ```bash
  python3.7 -m venv venv
  ```
* Then activate the environment:
  ```bash
  source venv/bin/activate
  ```
* Install the necessary items with requirements.txt:
  ```bash
    pip install -r requirements.txt
  ```
* Download the necessary csv files listed in the Datasets Used section
* Download the cleaned up csv files created by the contributors on this [google drive](https://drive.google.com/drive/folders/1lq9CVXbi3C3INEUpxUeNBACZHR3vWxhE)
* One all csv data sets have been added to the data folder in this directory, you can open it
* With your virtual environment now enabled with proper requirements, open the directory:
  ```bash
  code .
  ```
</br>

## Known Bugs

* No known bugs

<br>

## License

MIT License

Copyright (c) 2022 Ruben Giosa, Alejandro Socarras, Drew White

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

</br>

<iframe width="600" height="450" src="https://datastudio.google.com/embed/reporting/dbe92c8b-ccd3-41d9-b269-5964eb9717c3/page/f94CD" frameborder="0" style="border:0" allowfullscreen></iframe>
<iframe width="600" height="450" src="https://datastudio.google.com/embed/reporting/8a085df7-5101-4878-8c2c-8c6230de60d2/page/p_rh0ezxzj2c" frameborder="0" style="border:0" allowfullscreen></iframe>
<iframe width="600" height="450" src="https://datastudio.google.com/embed/reporting/fd52bc6a-18e7-4421-a385-c74ed91b9794/page/hpzCD" frameborder="0" style="border:0" allowfullscreen></iframe>