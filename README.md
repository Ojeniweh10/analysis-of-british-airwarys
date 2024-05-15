# Data Analysis of British Airways

The competition in the airline industry is at an all-time high due to the introduction of new airlines and expansion of existing services. Thus, to stay relevant in the industry it is crucial to understand the drivers of customer satisfaction for service improvements and effective marketing strategies. This analysis aims to analyze customer satisfaction within the airline industry, focusing on British Airways. By identifying factors influencing customer ratings and understanding seasonal booking trends, the analysis provides actionable insights that could enhance service delivery and customer experience.

The project follows a traditional data analysis methodology starting with data preprocessing, exploratory data analysis (EDA), and hypothesis testing to determine factors affecting customer satisfaction. The analysis was performed using Python. The data preprocessing of this dataset was challenging, and the detailed steps are presented after the results and discussion. 

To provide the final insights, the familiarity of the reader with the dataset is essential. The dataset contains passenger’s flight information including the routes, flying month, the class of flight and their review and rating regarding their flight experience. The figure shows the details. The complete code is presented [here](Data_Analysis_of_British_Airways.ipynb).

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/eaebc8c1-f2d5-4ec7-ba6a-ecf27fb0e978)

Let’s get the real value out of this dataset and present recommendations that can help British Airways enhance their services.

# 1.	The factors affecting customer choices.
To identify these factors that affect customer choices, the impact of rating on different variables has been studied. The satisfaction levels of customers can be analyzed for each variable that includes Type of Traveler, Flying Class.
The analysis reveals a significant difference in ratings among various traveler types. The Satisfaction rates for Leisure (Solo, Couple and Family) is higher as compared to Business travelers. This suggests that the experience of business travelers is significantly different from those traveling for leisure. Business travelers may have higher expectations regarding comfort, and connectivity, which are critical for their travel purpose. Business travelers might not be fully satisfied with the current offerings that cater primarily to leisure travel needs. The data shows that solo leisure travelers are the most satisfied group. This could be due to the more flexible and personal nature of their travel, potentially making it easier to meet or exceed their expectations compared to those traveling for business or in groups.

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/9924e8f7-cc66-4758-869b-aca6d822b28d)

The Figure below represents ratings per class. Satisfaction rates exhibit variation among different classes. More interestingly, the first-class customers have higher average ratings than business class customers, which indicates that expectations of business class are not met. In contrast, economy and premium economy showed lower but comparable ratings. The superior satisfaction ratings in first-class could be attributed to the exceptional services, space, and privacy afforded to these travelers, which significantly exceed those available in other classes. Despite the premium offerings of business class, the lower satisfaction compared to first-class might indicate gaps in service quality or amenities that do not align with the expectations of business travelers. This could involve aspects such as seating comfort, meal quality, or the efficiency of the check-in process.

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/9b6f3507-9d05-4c4a-8f14-facab315b10d)

# 2.	Evaluate the influence of holiday booking time on customer behaviour.

To evaluate the influence of holiday booking time on customer behaviour, the booking times are not available in the dataset. However, the dataset contains Flying month information which can be used to find monthly trends of the flights. Thus, monthly data for flights is extracted and then flight distribution for each month is visualized to see the monthly trends of flights. Finally, visualizations of flight distribution each month and the average customer rating by month is obtained to understand the influence of flight time on customer behaviour. The upper chart represents the number of flights each month. It can be observed that March, May, and June have the highest number of flights indicating the peak travel period. While the chart at the bottom shows the average customer ratings for each month.

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/e528b638-1e47-4e6c-9b5e-0f80b4146bff)


The higher ratings in October and September suggest an improved experience, while lower ratings in April and June indicate less favourable experiences.  The chart reveals that marks the beginning of the holiday season, this is where the highest number of flights are recorded, and this could mean that due to a high number of flights, indicating increased burden on the airways leading to strain on airline resources as well as capacity and potentially leading to unmet customer expectations. Thus, it can be concluded that the holiday season greatly affects the customers and that too in a negative way. The high volume of flights during the holiday season, particularly in the spring and early summer months, seems to correlate with decreased customer satisfaction, highlighting a potential area for airlines to address to improve passenger experiences during these critical periods.

# 3.	Find the likelihood of a successful holiday booking based on customer characteristics.
To perform this analysis, first the definition of ‘successful’ needs to be identified. By analyzing our data set, the factor that can represent a successful booking is a higher rating. A high rating is a rating above a certain threshold. In this analysis, we define that threshold rating and then segment the data into high, low ratings. Finaly, the distribution of high ratings on the number of flights each month is visualized to see how the month of travel correlates with high ratings thus indicating successful holiday booking. To define a certain threshold for high ratings, let’s look at the distribution of ratings.

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/5d36f97b-2f7e-45d1-8a60-d192a520c41f)

Given this distribution, a reasonable approach would be to consider ratings in the top quartile (75%) as high ratings. Therefore, the threshold for a high rating will be a rating of 4 or above. 

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/21625a81-8562-47d0-839f-5738c451bd38)

Next, the data is segmented on this threshold and the distribution of these high ratings are analyzed across months in fig. The likelihood of receiving a high rating is highest in September which is (36%) and that in October is 35%. Thus, suggesting a greater chance of successful bookings in these months. While June has the lowest likelihood of high ratings with 20%, indicating adverse conditions for travel. The likelihood varies across months, which indicates that customer satisfaction is greatly influenced by the holiday periods. Higher satisfaction in autumn could be linked to better weather, less congestion, or seasonal promotions that airlines might offer.

# 4.	Investigate the popularity of various routes.

To investigate the popularity of various routes and flight schedules, we analyze the dataset by focusing on the most frequently travelled routes and the multivariate analysis of routes and flying month leading to an understanding of popular routes on specific months or times of the year. To find the popularity of the routes, we count the number of times each route appears in the route column. However, there is one catch in it, the route column has inconsistent formatting across rows, so first we convert all the airport code names to city names and then find the frequency of each route. 
The results suggest that London to Cape Town is the most frequent and hence most popular route with 24 occurrences followed by Hong Kong to London. Moreover, the most common city among the top 10 routes is London. Of course, one reason might be because the dataset belongs to British Airways.
![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/5ed011ef-6e44-4491-b6ba-e4be8226734d)

The data analysis has been concluded. This analysis has successfully navigated through the complexities of airline customer satisfaction by highlighting the crucial periods and factors that contribute to the customers choices and popularity of various elements of British Air Ways. 

# Recommendations based on Hypothesis Testing

This section presents hypothesis testing based on research questions in the context of the study and then based on statistical tests we present the final recommendations. 
**Research Question:** Is there a significant difference in satisfaction levels among customers travelling for business compared to leisure?

![image](https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/47104001-c4ec-4d83-8d29-d685fe468b40)

The results of the Mann-Whitney U test are U-Statistic is 542754.0 while P-Value is 3.52e-15.
The U-Statistic is a measure of the difference in the distributions of the groups while p-value is significantly less than 0.05, indicating that there is a significant difference in the distributions of satisfaction levels between the business travellers and those travelling for leisure Thus rejecting our null hypothesis.  This result implies that both these traveler types exhibit different expectations and Airline may consider offering them tailored services based on the different preferences of business and leisure travelers.


# Recommendations to British Airways

The results from the Mann-Whitney U test show a significant difference in the satisfaction levels across customers related to business and those travelling for leisure. This result has several potential impacts and applications in the airline industry. These include Targeted services, Personalized Marketing strategy, and customized reward plans.

**Targeted services**
These results provide important insight into airlines to provide targeted services according to the different preferences of business and leisure travellers. The airline services should understand from these insights that these two groups shouldn’t be given similar treatment and packages. For instance, Business travellers may need faster check-ins, and reliable Wi-Fi for uninterrupted connectivity, while leisure travellers might consider more comfort and entertainment.

**Personalised Marketing strategy**
Moreover, Airlines can utilize these results to develop targeted marketing strategies for each group separately without relying on the same strategy for both, as both groups have different needs and desires. They should experiment with different elements to target these groups such as language, visual creatives, and services.

**Loyalty Programs Customization:**
Airlines can design customized reward packages and loyalty programs to benefit each group with different rewards based on what appeals to each group. One example can be to offer lounge access or priority boarding to loyal business travellers.



# Data Pre-Processing:
Data preprocessing is the process of transforming data to improve its quality and make the data ready for analysis. Preprocessing involves multiple steps and is dependent on the quality of the available dataset. The most common steps involved in preprocessing for data analysis are handling data inconsistencies, handling missing data, duplicate analysis and managing outliers. To proceed with data preprocessing, The dataset can be seen in the notebook. In addition to the Nan values, we see some inconsistencies in most of the columns. For example, flying_month has incorrect records that are most likely belonging to Route column as encircled in red. Thus, to handle the inconsistencies across the dataset, the data needs to be reshuffled to their actual columns.

**Handing Data Inconsistencies**
The dataset has been analyzed in-depth and all the inconsistencies are presented in Table. This table is structured to separate the expected correct and incorrect data for each column and the appropriate category for each of the incorrect data where this data belongs to. The Aircraft type is a new feature introduced in this analysis to store the aircraft type data.

<img width="593" alt="image" src="https://github.com/Mabrar92/Data-Analysis-of-British-Airways/assets/18236632/276265c0-319e-41b7-8549-17cd8689cb89">


For complete code with data preprocessing and all the above steps please click on [the code I wrote](Data_Analysis_of_British_Airways.ipynb).





