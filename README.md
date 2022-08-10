# Investigate Business Hotel using Data Visualization

## Intro
This is another Data Analysis Portfolio that I made to increase my ability to analyze, visualize and interpret a dataset. This porfolio also associated with [Rakamin Academy](rakamin.com) where I learn and discuss about data-related stuff. You can also read related article I created on [Medium](https://medium.com/@triesonyk/hotel-booking-analysis-127addfe5ba7)

## Data Info
The source of the data is [Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand). The data itself is actually from a [scientific article](https://www.sciencedirect.com/science/article/pii/S2352340918315191) written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019. There are two hotels, a resort hotel, and a city hotel, as the sources of the dataset, both hotels are located in Portugal.
There are 31 features there are related to booking information such as dates, lead booking time, average daily rate (ADR), number of guest, etc.

![image](https://user-images.githubusercontent.com/20869651/181665109-16fb8391-e7ef-4724-ab85-380a8c026c56.png)


## Data Preprocessing
### Data Cleansing
The data itself is not really that problematic. Only a handful of missing values and outliers. I replace missing values in country to `unknown`, for children, agent, and company I replace them with `0`. I assume the missing value mean that they don't bring children, do not book trough agent or do not associate with any company for the reservations 

![image](https://user-images.githubusercontent.com/20869651/181665551-b8fc1328-e825-425d-8344-3159a3a26b96.png)

### Feature Engineering
I created or extracted new features to make it easier to do analysis such as, 
- `total_guest` : number of guest including kids, 
- `total_stays` : number of days the guest stay at the hotel,
- remapping `arrival_date_month` to numbers so it's easier to analyze using machine learning later

## Insights and Recommendation
You can read the full analysis on [Medium](https://medium.com/@triesonyk/hotel-booking-analysis-127addfe5ba7) but this is some recommendation I gained from the insight
- For customers, booking a hotel long before the stay is good but do not book more than 9 months of the stay, the best time to book is 1–3 months.
- For city hotel owners, the rates of cancelation at a city hotel are quite high. Giving a penalty (from the deposit) to people who cancel their booking 1 month before the stay date to lower the chance of cancelation, also gives a maximal of 14 days before the stay to cancel a reservation.
- For resort hotel owners, 7 days is one of the most favorites duration for staying, if people book 5–6 days give them an option to book for 7 days with cheaper rates.
