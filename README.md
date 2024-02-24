Introduction


In this project, I had to assist a fictional Bike company called Cyclistic Bikes to try and convert their casual riders into 
membership riders. 


In order to answer the business questions, follow the steps of the data analysis process: 


Ask


Prepare


Process


Analyze


Share


Act




Scenario


You are a junior data analyst working on the marketing analyst team at Cyclistic, a bike-share
company in Chicago. The director of marketing believes the company’s future success
depends on maximizing the number of annual memberships. Therefore, your team wants to
understand how casual riders and annual members use Cyclistic bikes differently. From these
insights, your team will design a new marketing strategy to convert casual riders into annual
members. But first, Cyclistic executives must approve your recommendations, so they must be
backed up with compelling data insights and professional data visualizations
Case Study Roadmap


●Prepare Guiding questions 


● Where is your data located? 


● How is the data organized? 


● Are there issues with bias or credibility in this data? Does your data ROCCC? 


● How are you addressing licensing, privacy, security, and accessibility? 


● How did you verify the data’s integrity? 


● How does it help you answer your question? 


● Are there any problems with the data? Key tasks 


● Download data and store it appropriately. 


● Identify how it’s organized. 


● Sort and filter the data. 


● Determine the credibility of the data. Deliverable 


● A description of all data sources used
Ask


Three questions will guide the future marketing program:


1. How do annual members and casual riders use Cyclistic bikes differently?


2. Why would casual riders buy Cyclistic annual memberships?


3. How can Cyclistic use digital media to influence casual riders to become members?


Moreno has assigned you the first question to answer: How do annual members and casual
riders use Cyclistic bikes differently?
​

Questions to answer through data


What distance do members vs casual riders typically travel?


Are electric or classic bikes rented more by casual riders or members?


How long are the riders staying on the bikes?


What day of the week do members/ casual riders usually use the bikes?


What is the average ride time for members vs casual riders?

​
The business task: Find a way to influence casual riders to buy memberships


Prepare


Dataset link: https://divvy-tripdata.s3.amazonaws.com/index.html


Fields: 


Ride_id - The ID number used to identify the rider


Rideable_type - The type of bike used, electric or classic


Started_at - The date and time the ride started


Ended_at - The date and time the ride finished


Start_station_name - The name of the station they started their ride


Start_station_id - The station’s ID


End_station_name - The name of the station they ended their ride


End_station_id - The station’s ID


Start_lat - The starting longitude


Start_lng - The starting latitude


End_lat - The ending longitude


End_lng - The ending latitude


Member_casual - If the person is a member or a casual rider

​
Issues with data: A lot of missing information under: Start_station_id, End_station_name, End_station_id, End_lat, End_lng,
Start_lat, Start_lng


Actions Taken


Uploaded to Excel to check data


Deleted unneeded empty cells


Added columns: ride_length and day_of_week (1 = Sunday and 7 = Saturday (1-sun, 2-mon, 3-tues, 3-wed, 4-thurs 5- fri, 7-sat)
subtracting the column started_at from the column ended_at (for
example, =D2-C2)


=WEEKDAY(C2,1)


Under Cells>Format>Format Cells>time>13:30:55>OK


Deleted data that didn’t populate correctly for the ride_length field


Calculate the mean of ride_length


=AVERAGE()


Calculate the max ride_length


=MAX()


Calculate the mode of day_of_week


=MODE()

​
Created Pivot Tables with the following: 


● Calculate the average ride_length for members and casual riders. 


Try rows = member_casual


Values = Average of ride_length.
​

Titled: average ride_length
​

● Calculate the average ride_length for users by day_of_week. 


Try columns =day_of_week


Rows = member_casual


Values = Average of ride_length

​
Titled: average ride_length by dayofwk

​
● Calculate the number of rides for users by: 


day_of_week by adding Count of trip_id to Values.
​

Titled: number of rides


Process


Tools I worked with: 


    Excel: manipulate, delete, and add info to the data

    
    BiqQuery: SQL queries

    
    Jupiter Notebook: documentation, Python analysis

    
Analyze


![Dashboard 1](https://github.com/asbrown59/asbrown59-asbrown_Data-Analysis-Cyclistic_Bikes-Capstone-Project/assets/152925636/14666a0a-6716-4bd2-8d2b-4f0541a35445)


Link to Tableau: https://public.tableau.com/views/cyclistic_bikes_17088089561630/Dashboard1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link


Findings


From the visuals, you can see there are a lot of casual riders are not choosing to get a membership. Throughout the day, causual riders are staying on the bikes for longer, but are 
renting out the bikes less. The most common day both casual riders and member riders are renting are between Tuesday and Wednesday. 


My Solutions?


Offer limited-time promotions or discounts for memberships targeted specifically at casual riders. For example, provide a discount for signing up during their most common rental 
days (Tuesday's and Wednesday's) or offer a trial membership for a reduced fee.


Forge partnerships with the most frequented locations. Offer joint promotions or discounts to incentivize membership sign-ups.


Highlight the convenience of membership, such as faster check-in processes, priority access to bikes during peak times, and the ability to reserve bikes in advance.


Incentivize current members to refer their casual rider friends by offering discounts or rewards for successful referrals. Word-of-mouth marketing can be powerful in reaching 
this demographic.
