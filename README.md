# California wildfires analysis:

* The purpose of this project is to analyse wildfires in California between 2013 and 2020
* The dataset were obtained from Kaggle, and the original data scraped from www.fire.ca.gov and large-scale traffic and weather event dataset
* Some outliers were present in the data which had to be cleaned, but overall the data seemed reliable.

## Code and Resources Used:

**Python Version:** 3.8

**Packages:** pandas, seaborn, matplotlib

**Enviroment:** google collab

**Tableau:** Public

**Data:** Obtained from Kaggle

## Data Cleaning:

After obtaining the data, I needed to clean it up so that it was usable for my analysis. I made the following changes:

* **Change Datatypes:** Extinguished, Started and Updated were set to datetime64
* **New Columns:** A New column was created called days active by subtracting Extinguished from Started and its datatype changed accordingly.
* **Assigning new values:** The column acres was changed to hectares by dividing acres by 2.471
* **Deleting columns:** Since all the active fires were false, that column was dropped. Fires that do not belong to CalFireIncident were also dropped as well as ControlStatement since the mayority is null. In total, these were all the deleted columns:
  - Active
  - ArchiveYear
  - CalFireIncident
  - ConditionStatement
  - ControlStatement
  - CountyIDs
  - Features
  - Final
  - FuelType
  - Locatopn
  - PercentContained
  - SearchDescription
  - SearchKeywords
  - Status
  - UniqueID
  - Updated
 
## EDA

I needed to think some questions to answer in order to make an analysis about this dataset, the questions were:

1. At what time do usually wild fires occur?
  - Wild fires in California usually start at 14:21 hours
2. How frequent and destructive they are?
  - There were 1251 fire incidents, i.e., 1 fire starts every 2 days and 2017 was the year with more fires and 
  - There were a total of 2.3 million hectares burned which is similar to half of the area of Switzerland.
3. Which places are the most affected during the time measured?
  - **Top 5 places by structures destroyed:**
    - Butte - 19021
    - Sonoma - 7372
    - Napa - 7186
    - Ventura - 2724
    - Shasta - 1940
4. Which places have the most burned area?
  - **Top 5 counties by hectares burned:**
    - Lake 235745
    - Mendocino 207007
    - Colusa 185883
    - Ventura 171823
    - Glenn 167077

5. Is there a correlation between lack of rain and fires?
  - The year with most rain taking place is 2017. From 2016 the data is incomplete. From the graph and the data collected, there seems to be a correlation between lack of rain and wildfires.


<img src="https://user-images.githubusercontent.com/99658869/216359306-ed8cce5c-8eef-49e5-b8f2-d5de028d8ce2.png" width="900" height="650">

<img src="https://user-images.githubusercontent.com/99658869/216360475-beafcfed-08f0-4c16-a665-542fb3311755.png" width="450" height="350"><img src="https://user-images.githubusercontent.com/99658869/216360729-299de3b8-d94d-4526-90fd-ecb105e60ed7.png" width="450" height="350">

A more complete graph visualization can be seen in:

https://public.tableau.com/app/profile/marcelo7812/viz/Californiawildfiresincidents/Californiawildfiresincidents

## Outlook:

As the planet heats up, more wildfires will appear not only in remote locations but also in urban locations causing a tremendous amount of material damage, with a significant loss of wildlife. It of vital importance to make predictive models which can assess if a fire is likely to occur given some climatological factors.
