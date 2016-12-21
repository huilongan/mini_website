# ADS Final Project: Yelp Review System

Term: Fall 2016

+ Team Name: Group 12
+ Projec title: Yelp Review System
+ Team members
	+ Jiayi Wang jw3316@columbia.edu
	+ Ran Li rl2633@tc.columbia.edu
	+ Shuli Song ss4962@columbia.edu
	+ Xuechun Sun xs2254@columbia.edu
	+ Huilong An ha2399@columbia.edu
	
	
### Yelp Review System Installation: [Dropbox Link](https://www.dropbox.com/sh/2t8netierfalnr0/AACqnX1LW-1Ert5UcuZOGjXSa?dl=0)
  + Download the "app" file by clicking droxbox link above (due to the size of database, we cannot upload files on github)
  + Set up required environment specified in 'requirement.txt' (We support Python 2.7).
  + Run ```python app.py```


### Data Scource: [Yelp Dataset Challenge](https://www.yelp.com/dataset_challenge)
      
  + 2.7M reviews and 649K tips by 687K users for 86K businesses
  + 566K business attributes, e.g., hours, parking availability, ambience.
  + 9 cities across 4 countires: U.K.: Edinburgh, Germany: Karlsruhe, Canada: Montreal, U.S.: Pittsburgh, Charlotte, Urbana-Champaign, Phoenix, Las Vegas, Madison


### Project summary: 
  ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/homepage.png)


  + Build Database 
    + Build the database by using sqlite3 in Python (Traditional relational database)
    + Write a class named 'minidatabase' to encapsulate query methods needed
    + Everytime just need to import recommender and connect to built database by minibase
  
  + Build Website using Flask Python
    + RESTful Based 
    + Request 'user_id' and other information from html and use ajax (based on javascript) for transfering information
  
  + Item based similarity recommendar  
  
     1. **Similarity computation:** This model computes the similarity between items using the observations of users who have interacted with both items.	For similarity here, we choose Cosine similarity, which is computed as:  .
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/Cosine_similarity_recom.jpeg)
    where Ui is the set of users who rated item i, and Uij is the set of users who rated both items i and j.  
    
    2. **Prediction generation:** If we target item j, given a similarity between items i and j, S(i,j), it scores an item j for user using a weighted average of user's previous observation ratings. Prediction for Item j is computed as:
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/recom_prediction.jpeg)
    
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/customize5.png)
  
  + Overview Statistics EDA
  
     + Visualizations of business data, user data and review data, including a worldwide map of user distribution, a detailed map of user distribution by city, an animated donut plot of register users by year, a bar plot of top5 cuisine type by city, a stacked plot of rating distribution by city, a correlation heatmap of review frequency and number of fans and an interactive chord diagram between type of votes and average review.
     
     ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/overview1.png)
     ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/overview2.png)
     ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/overview3.png)
     ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/overview4.png)
     
     
     
  + Individual Statistics EDA
    
    0.  **Website page**
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/customize1.png)
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/customize2.png)
  
    1.  **Individual review text word cloud**
    
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/customize3.png)
    
    2.  **Overview of individual selected restaurants** 
    
    3.  **Statistical summary of individual ratings** 
    
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/customize4.png)
    
    
   
  + NLP Word Cloud
  
    + Overview word cloud based on star rating 1 ~ 5
    + Individual word cloud based on history review text dataset
    
    ![image](https://github.com/TZstatsADS/Fall2016-proj5-proj5-grp12/blob/master/figs/overview6.png)
  


### Tools

	
**Contribution statement**: All team members contributed equally in all stages of this project. All team members approve our work presented in this GitHub repository including this contributions statement. 

Following [suggestions](http://nicercode.github.io/blog/2013-04-05-projects/) by [RICH FITZJOHN](http://nicercode.github.io/about/#Team) (@richfitz). This folder is orgarnized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```

Please see each subfolder for a README file.
