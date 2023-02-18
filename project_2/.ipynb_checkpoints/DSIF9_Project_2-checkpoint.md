
<h1 align="center"> Identifying the Best Predictors of</br> 
Housing Resale Prices in Singapore </h1>
<h3 align="center"> DSIF 9 Project 2 </h3>  

</br>


<!-- CONTENT -->
<h2 id="table-of-contents"> Contents</h2>

1. [Background](#background)  
2. [Problem Statement](#problem-statement)
3. [External Research and Additional References](#external-research)
4. [Data Dictionary](#data-dictionary)   
5. [Analysis Approach](#analysis)   
6. [Findings and Recommendations](#findings-recommendations)
7. [Kaggle Submission](#kaggle-submission)
7. [Credits](#credits)


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- BACKGROUND -->
<a name="background"></a>
<h2 id="background"> Background </h2>

<p align="justify"> 
    
One of Singapore's leading property web portals PropertyGuru would like to publish an interactive game on its website for customers to see how different permutations of various factors can predict home resale prices in Singapore. 
    
This is an attempt to drive website traffic up in the face of competition from similar websites such as 99co and Stacked Homes. They hope that people looking to sell or buy their first property in Singapore will use the game to inform their decisions.

PropertyGuru is interested to highlight the top factors that most strongly influence property resale prices and build it into their interactive game. Regression models, which are known for their ease of interpretability, might be suitable models for predicting property resale prices in Singapore in a way that is understood easily.

Success to PropertyGuru would be higher brand awareness and an uptick in website traffic after the game has been made public.
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a name="problem-statement"></a>
<h2 id="problem-statement"> Problem Statement</h2>

<p align="justify"> 

The main questions that the model aims to answer are:
<ol>    
    <li> Which factors best predict the resale price of a typical housing unit in Singapore and should be included in the interactive game? </li>
    <li> Which neighbourhoods fetch higher resale prices? </li>

</ol>

</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a name="external-research"></a>
<h2 id="external-research"> External Research and Additional References</h2>

<p align="justify"> 

Location is a primary consideration when it comes to real estate. The presence and proximity of amenities and lifestyle choices affect property resale prices, and in Singapore the following factors are known to be especially important influencers of property purchase decisions:
    
<ol>    
    <li> Proximity to quality local schools for young families </li>
    <li> Proximity to workplaces (which explains why property prices have a positive relationship with closeness to the Central Business District) </li>
    <li> Proximity to social, shopping and recreational centres </li>
    <li> Flat condition </li>
    <li> Lease duration </li>
    <li> Flat size </li>
    <li> Estate maturity </li>
</ol>  

These factors are not truly independent of each other. For example, working professionals with young children will not just want access to good schools but also an easy commute to work, and access to shopping centres, affordable food, or recreational services. 

There is also a growing trend of public housing resale prices exceeding SGD 1M in recent years. 2021 saw a record 259 million-dollar HDB resale flats transactions, a stark increase from 82 in 2020. There were a record number of 111 HDB resale flat transactions that breached the million-dollar mark in the third quarter of 2022. 

More recently, news about Anglo-Chinese School (ACS) relocating ACS (Primary) from Barker Road to Tengah in 2030 triggered much discussion, with analysts predicting that the move will likely push up home prices in Tengah up by 15 per cent. It appears that certain schools may also have a palpable impact on housing prices.

Sources: [Redbrick SG](https://www.redbrick.sg/blog/what-affects-real-estate-prices/), [ChannelNews Asia](https://www.channelnewsasia.com/singapore/hdb-resale-flat-prices-strong-demand-million-dollar-transactions-property-3030186) and [TODAY](https://www.todayonline.com/singapore/relocation-acs-schools-analysts-expect-downward-pressure-newton-property-prices-opposite-effect-tengah-2104606)

</p>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a name="data-dictionary"></a>
<h2 id="data-dictionary"> Data Dictionary</h2>

The full data dictionary and description of variables can be found [here](https://www.kaggle.com/competitions/dsi-sg-project-2-regression-challenge-hdb-price/data).


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a name="analysis"></a>
<h2 id="analysis"> Analysis Approach </h2>

The steps taken to analyse the datasets were as follows:

<ol>    
    <li> Imported the data for inspection and checked for missing values, unexpected outliers, duplicates or clearly erroneous data points. Missing values were imputed with the appropriate values. </li>
    <li> Converted data types in line with the intended analysis to facilitate interpretation (e.g. analysing dates as categorical variables rather than datetime or ordinal) </li>
    <li> Visualised the data to uncover each variable's distribution, identify outliers and understand relationships with other features. Performed exploratory data analysis to address some basic questions about the dataset.  </li>
   <li> Using domain knowledge, dropped variables that had substitutes, close to 0 correlation with the output variable, and used in feature engineering of new variables.  </li>
   <li> Conducted feature engineering by combining existing variables, or calculating new features from existing ones.  </li>
    <li> Used linear regression models to predict resale prices and develop recommendations to address the problem statements. </li> 
</ol>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a name="findings-recommendations"></a>
<h2 id="recommendations"> Findings, Recommendations and Next Steps </h2>

**Findings**

Compared to other regularization methods such as Lasso regression or ElasticNet regression, the Ridge regression model yielded the best predictions for resale price.

The top predictive features for resale price relate to flat models, planning area and primary school names. 

Flat models that are larger in size such as terraces and maisonettes are related to higher resale prices. 

The finding that neighbourhood and proximity to good primary schools are top predicts corresponds with external research, as these are often key considerations Singapore families have when deciding on where to purchase a flat. Neighbourhoods that are further away from the city centre such as Changi (median price SGD 259K) and Choa Chu Kang (median price SGD 404K) come with lower housing resale prices while homes located right at the CBD (Downtown Core) command higher prices, which could also be due to its proximity to workplaces. Homes in areas such as Bukit Timah - close to top schools and amenities - fetch higher prices as well with a median resale price of SGD 719K.   

Proximity to well-known primary schools and those with affiliation to popular secondary schools (such as CHIJ, Tao Nan, Ngee Ann and St Patricks) are strong positive predictors of resale price. 

Unit size is also a strong predictor of a flat's resale price. 

<br>

**Recommmendations**

PropertyGuru should include the following variables in their interactive game for predicting housing prices:

 - full range of neighbourhoods in Singapore
 - a search function for primary schools nearby
 - flat models
 - unit size

<br>

**Future Steps**

- Use ensemble methods or boosting to achieve higher performance through learning from the shortcomings of earlier model iterations. A single regression model seems inadequate for predicting housing prices, given the high error rate and the fact that the data distribution may have been better addresed by other types of models.
- Consider analysing the features predicting resale price using separate models for various housing unit types. The factors predicting the prices for those homes may vary due to different profile of buyers for each unit type.
- If the data is available, it may be useful to merge the dataset with information on the purchasers' family size, demographic profile and income range, which can add more information and aid with model interpretation. 


<p align="center"> 
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Kaggle Submission -->

<a name="kaggle-submission"></a>
<h2 id="kaggle-submission"> Kaggle Prediction Submission </h2>

The scores obtained from the Kaggle submission:

![kaggle](./kaggle/score.png "Kaggle Score").



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- CREDITS -->

<a name="credits"></a>
<h2 id="credits"> Credits</h2>

Referenced ReadMe file from [Mohammad Amin Shamshiri](https://github.com/ma-shamshiri/Pacman-Game/blob/master/README.md)
