
<h1 align="center"> Predicting topics and sentiments of customer service queries and recommending suggested responses </h1>
<h3 align="center"> DSIF 9 Capstone Project </h3>  

</br>



<!-- CONTENTS -->
<h2 id="table-of-contents"> Contents</h2>

- [Problem Statement](#problem-statement)
- [Approach](#approach)
- [Data Collection](#data-collection)
- [Preprocessing](#preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modelling and Evaluation](#modelling)
- [Conclusion and Recommendations](#conclusion)



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div id="problem-statement"></div>

## Problem Statement
    
Company data on customer queries today is not categorised by topic or sentiment, and the process of filtering spam before addressing each query requires dedicated manpower.
    
This prevents the team from easily tracking spikes in complaints about a particular issue or topic in real-time for quick resolution, and also limits optimal manpower allocation to other more resource-heavy tasks.

The initial model's outputs can inform the building of dashboards for live tracking of top customer queries. Potentially retrieving the most likely responses to the query based on historical data means the team can address queries more efficiently.

<br>

Questions to address:
<ol>    
    <li> How can we generate topics and sentiments from the customer queries when we don't explicitly ask for it from customers? </li>
    <li> What are the themes/sentiments of these queries? </li>
    <li> How can more efficiently address frequently-asked questions? </li>
</ol>

</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div id="approach"></div>

## Approach

The dataset comprises ~4000 individual queries with the relevant responses. The headers are:

- Subject: Email subject
- Case: Created Date/Time
- Case: Date/Time Closed
- Case Subject: Truncated version of email subject
- Assigned: Officer who handled the query
- Completed Date/Time: Date and time the case was closed
- Status: Whether case is open or completed
- Activity ID: Unique serial number for each case
- Comments: Response from us to member of public
- Case Number: Serial number relating to each occurrence of email exchanged. If there is a follow-up query to the original response from us, there will be multiple counts of one case number.
- Case Description: original query from the public
- Lead ID: ID of the individual if he/she is registered on our database. Blank values represent non-members.



**Steps:**

Obtain raw data in CSV format from the company CRMS with:

- Dates of each query and corresponding response
- Clean, anonymise and remove spam from the data. Might use NER to remove sensitive info like names and organisations.
- Pre-process the data in preparation for training the following models:
    - Topic modeling to explore the range of possible themes underlying the dataset
    - Few-shot classification to predict labels for topics and sentiments using transformers
    - Option 1: Attempt a question-answering model that retrieves the most appropriate answer to a question from a given text and/or external sources
        - A foreseeable challenge is the need to identify the start and end index of the answer within a given context for each particular question in the training set. 
        - References explored via desk research so far: extractive question answering which relies on a provided dataset to match and retrieve answers, Retrieval Augmented Generation (RAG) which makes use of external datasources for question answering 
        - One drawback to keep in mind is that questions which are completely new to us will not have a prior response available. As such, the response "bot" is best positioned as something used for FAQs, not an open-ended response generator.
    - Option 2: List the top 10 questions associated with each topic for internal reference so officers can more easily craft a customised response


**Performance metrics:**

- Accuracy or F1 score to check that both false positives and negatives are low

**Foreseeable challenges:**

- Unsure how data retrieval and response generation works, and how the model might be finetuned.
- Need thorough hashing and anonymisation

**Stakeholders:**

- Colleagues and bosses who are keen to optimise manpower allocation and automate customer service roles.








<br>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)







<br> 


<!-- CREDITS -->
<h2 id="credits"> Credits</h2>

Referenced ReadMe file from [Mohammad Amin Shamshiri](https://github.com/ma-shamshiri/Pacman-Game/blob/master/README.md)

Acknowledgements: Based on UC Berkeley's Pacman AI project, <a href="http://ai.berkeley.edu">http://ai.berkeley.edu</a>
