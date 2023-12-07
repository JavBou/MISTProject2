
# MIST Group Project 2


## Team Name

cs_g5p1


## Team Members

1. Javi Bou [@JavBou](https://github.com/Javbou)
2. Sebastian Taborda [@SebastianTaborda1](https://github.com/SebastianTaborda1)
3. Coleman Leathers [@cleatherss](https://github.com/cleatherss)
4. Matt Pietri [@MattPietri](https://github.com/MattPietri)
## Dataset Description

Our dataset provides information on motor vehicle operators involved in traffic collisions occurring on county and local roadways within Montgomery County, as collected via the Automated Crash Reporting System (ACRS) of the Maryland State Police, and reported by the Montgomery County Police, Gaithersburg Police, Rockville Police, or the Maryland-National Capital Park Police. We obtained our dataset from https://catalog.data.gov/dataset, and our specific data can be found at https://catalog.data.gov/dataset/crash-reporting-drivers-data. While our dataset contains numerous data types, some of the key metrics it records are crash date and time, road where the crash occurred, collision type, weather, light level, injuries, vehicle information and damage, and more. Each row of the dataset represents a reported traffic collision.
## Analysis of Questions

### Question 1
#### What are the most dangerous times of day (when you are most likely to get into a crash), and under what weather conditions are there the most crashes in Montgomery County?

This question is important because it shows the different times of day and what the weather is during said time. This data is ordered by how frequently a crash happens during that time and the crash's respective weather conditions. We also have a graph emphasizing the weather during all of the crashes. This graph also orders them by how frequently a crash happens with a certain type of weather.  These graphs are helpful so people can see an overall view of the time and weather where most crashes take place, but also a more concise graph solely focusing on the weather. People will be able to know how frequently crashes happen. 


### Question 2
#### What kind of collision type (where in the car was there damage) resulted in the greatest amount of “suspected minor  injuries” in the county?

We wanted to ask a question that would lead to a possible discovery of a correlation between the type of car collision and how severely injured the people in the crash are. People who look at these graphs will be able to read and understand the different types and angles in which car crashes can happen. These people could identify which type of crash is most dangerous and try to improve their driving so they can avoid these injuries. For example, A person who reads these graphs and sees that a head on left turn can cause a lot of possible injuries, suspected minor injuries and suspected major injuries, then in the future, they could be more cautious when making left turns. This will cause the number of total crashes from head-on left turns to decrease, and fewer people will end up getting injured. 

## Data Manipulation

One main manipulation we had to perform on the data was with regard to the date and time of the entries. In the original data set, both the date and the time of the crash were contained in the same cell (when looking at the data in CSV format). To combat this, text to columns was used in Excel in order to separate the date and time within each entry, thus allowing us to use date and time independently in the data set. Even with the manipulation, the way the dates were formatted was unrecognizable to SQL due to the specific date/time format SQL supports. Because of this, we we're unable to utilize line graphs with dates or times in our data analysis.

One other small manipulation we performed on the data was with respect to outlying column types and apparent errors in the dataset itself. For example, some light-level types were shown as strings of letters and numbers as opposed to actual descriptors and needed to be excluded from the data. Considering an automated reporting system was used to collect the data (as mentioned in the Dataset Description), it makes sense that there would be some small errors in some of the data. These outlying entries only represented a small portion of the data and appeared only around 3-4 times among the 5000 total entries.
## Analysis and Results

### Question 1
#### Graph 1:
![Table 1](https://i.imgur.com/FH9tymL.png)

In this graph, we can see how weather affects the amount of car crashes that take place. We are able to see how frequent car crashes take place when it is either clear, raining, cloudy, or no weather reported at all. A majority of car crashes take place in clear weather, which makes sense because it is usually clear out during the day when compared to raining or cloudy.

#### Graph 2:
![Table 2](https://i.imgur.com/7o9EbZg.png)

This graph separates each type of weather by date and time to find the frequency of car crashes at a certain weather condition and further filters by the time of day of the occurrence. The darker the box, the higher the frequency of crashes. Each individual box represents a point in time during a given day. What we can gather from the chart is that most crashes, on average, happen during clear weather. Once we look at individual times, 5:00 PM has the highest number of crashes during clear weather, with 28. The next most frequent being 12:30, 10:00, 3:15 and so on, all during clear weather. Overall the chart shows that most crashes happen during clear weather at any given point in the afternoon.

### Question 2
#### Graph 1:
![Table 3](https://i.imgur.com/l62cwLH.png)

Our first graph shows the total number of crash reports that gave people different types of injuries based on the type of car crash they got into. We noticed that there were a substantial amount of suspected minor injuries, so we decided to pull that data into a separate graph below.

#### Graph 2:
![Table 4](https://i.imgur.com/LTxF5o6.png)

In this graph, we excluded no injuries and possible injuries because they would not help us determine what specific injuries, such as suspected minor injuries, occurred. Because of this, after pulling out the suspected minor injuries from the first graph, we are better able to understand how many minor injuries happen during car crashes. According to the data, the types of car crashes that cause the most minor injuries include; the same rear end, straight movement angle, and head-on left turn.
## Tableau Packaged Workbook

#### The packaged workbook containing the visualizations shown above is attached to this repository.
