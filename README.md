# Hotel_Booking
In this analysis, we analyzed the Hotel Bookings dataset to gain insights from the reservation patterns of customers using Python programming language.\
**Author Name:** Ali Hassan\
**Email:** official.aharain@outlook.com\
**Website:** https://contra.com/arainofficial \
**Github:** https://github.com/AHArain-analyst


## About Dataset
### Description
This data set contains booking information for a city hotel and a resort hotel and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.

All personally identifying information has been removed from the data.

### Features
| Variable                                | Class    | Description                                                                                                           |
|-----------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------|
| hotel                                   | character | Hotel (H1 = Resort Hotel or H2 = City Hotel)                                                                      |
| is_canceled                             | double   | Value indicating if the booking was canceled (1) or not (0)                                                       |
| lead_time                               | double   | Number of days that elapsed between the entering date of the booking into the PMS and the arrival date            |
| arrival_date_year                       | double   | Year of arrival date                                                                                                 |
| arrival_date_month                      | character | Month of arrival date                                                                                                |
| arrival_date_week_number                | double   | Week number of year for arrival date                                                                               |
| arrival_date_day_of_month               | double   | Day of arrival date                                                                                                  |
| stays_in_weekend_nights                 | double   | Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel                     |
| stays_in_week_nights                    | double   | Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel                           |
| adults                                  | double   | Number of adults                                                                                                    |
| children                                | double   | Number of children                                                                                                  |
| babies                                  | double   | Number of babies                                                                                                    |
| meal                                    | character | Type of meal booked. Categories are presented in standard hospitality meal packages: Undefined/SC – no meal package; BB – Bed & Breakfast; HB – Half board (breakfast and one other meal – usually dinner); FB – Full board (breakfast, lunch and dinner) |
| country                                 | character | Country of origin. Categories are represented in the ISO 3155–3:2013 format                                          |
| market_segment                          | character | Market segment designation. In categories, the term "TA" means "Travel Agents" and "TO" means "Tour Operators"    |
| distribution_channel                    | character | Booking distribution channel. The term "TA" means "Travel Agents" and "TO" means "Tour Operators"                  |
| is_repeated_guest                       | double   | Value indicating if the booking name was from a repeated guest (1) or not (0)                                    |
| previous_cancellations                  | double   | Number of previous bookings that were cancelled by the customer prior to the current booking                      |
| previous_bookings_not_canceled           | double   | Number of previous bookings not cancelled by the customer prior to the current booking                            |
| reserved_room_type                      | character | Code of room type reserved. Code is presented instead of designation for anonymity reasons                           |
| assigned_room_type                      | character | Code for the type of room assigned to the booking. Sometimes the assigned room type differs from the reserved room type due to hotel operation reasons (e.g. overbooking) or by customer request. Code is presented instead of designation for anonymity reasons |
| booking_changes                         | double   | Number of changes/amendments made to the booking from the moment the booking was entered on the PMS until the moment of check-in or cancellation |
| deposit_type                            | character | Indication on if the customer made a deposit to guarantee the booking. This variable can assume three categories: No Deposit – no deposit was made; Non Refund – a deposit was made in the value of the total stay cost; Refundable – a deposit was made with a value under the total cost of stay. |
| agent                                   | character | ID of the travel agency that made the booking                                                                      |
| company                                 | character | ID of the company/entity that made the booking or responsible for paying the booking. ID is presented instead of designation for anonymity reasons |
| days_in_waiting_list                    | double   | Number of days the booking was in the waiting list before it was confirmed to the customer                           |
| customer_type                           | character | Type of booking, assuming one of four categories: Contract - when the booking has an allotment or other type of contract associated to it; Group – when the booking is associated to a group; Transient – when the booking is not part of a group or contract, and is not associated to other transient booking; Transient-party – when the booking is transient, but is associated to at least other transient booking |
| adr                                     | double   | Average Daily Rate as defined by dividing the sum of all lodging transactions by the total number of staying nights |
| required_car_parking_spaces             | double   | Number of car parking spaces required by the customer                                                            |
| total_of_special_requests                | double   | Number of special requests made by the customer (e.g. twin bed or high floor)                                     |
| reservation_status                       | character | Reservation last status, assuming one of three categories: Canceled – booking was canceled by the customer; Check-Out – customer has checked in but already departed; No-Show – customer did not check-in and did inform the hotel of the reason why |
| reservation_status_date                  | double   | Date at which the last status was set. This variable can be used in conjunction with the ReservationStatus to understand when was the booking canceled or when the customer checked out of the hotel |


### Data Source
The data is originally from the article [Hotel Booking Demand Datasets](https://www.sciencedirect.com/science/article/pii/S2352340918315191), written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019.

The data was downloaded and cleaned by [Thomas Mock and Antoine Bichat](https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-02-11/readme.md#data-dictionary) for #TidyTuesday during the week of February 11th, 2020.


## Purpose of Analysis

The dataset consists of various attributes related to hotel bookings, including information about guests, booking details, and hotel characteristics. The primary purpose of this analysis is to gain insights and understanding of the data to inform business decisions, improve hotel management, and enhance the guest experience. The key objectives of the analysis include:

1. **Booking Trends**: Explore trends in hotel bookings, such as the time of year when bookings are most frequent, the distribution of booking channels, and the average lead time between booking and arrival.

2. **Cancellation Analysis**: Investigate factors contributing to booking cancellations, including the impact of deposit type, market segment, and previous cancellations.

3. **Guest Demographics**: Understand the demographic profile of guests, including the number of adults, children, and babies, as well as the countries of origin for guests.

4. **Room Assignment**: Examine patterns in room assignments, including how often the assigned room type matches the reserved room type, and how booking changes affect room assignments.

5. **Pricing and Revenue**: Analyze the Average Daily Rate (ADR) to assess pricing strategies and revenue generation.

6. **Special Requests and Services**: Investigate the number of special requests made by guests and assess the impact of these requests on the guest experience.

7. **Customer Type Analysis**: Understand the different types of bookings, such as group bookings, contract bookings, transient, and transient-party, to tailor services accordingly.

8. **Parking and Other Amenities**: Evaluate the demand for car parking spaces and identify any additional services that can enhance guest satisfaction.

9. **Reservation Status**: Analyze the reservation status to identify patterns of cancellations, check-outs, and no-shows.

10. **Time Series Analysis**: Examine time series data to identify long-term trends and seasonal patterns, which can be used for revenue forecasting and resource allocation.

By conducting this analysis, we aim to provide actionable insights to hotel management, marketing teams, and other stakeholders, allowing them to make informed decisions to optimize hotel operations, improve guest satisfaction, and maximize revenue.

## Project Scope: Hotel Booking Analysis

### Introduction
The primary objective of this project is to analyze the Hotel Bookings dataset using Python to uncover interesting details about the booking patterns and trends. The dataset includes information such as the type of hotel, country of booking, arrival date, number of visitors, etc.

### Project Steps:

1. **Importing Required Libraries**:
   - **Libraries**: pandas, matplotlib, seaborn, warnings
   - **Purpose**: To facilitate data processing, visualization, and handling warnings.

2. **Reading the Dataset**:
   - **Method**: pandas `read_csv()` function
   - **Purpose**: To load the dataset into a DataFrame and get an initial overview using `tail()`, `shape()`, and `info()` functions.

3. **Data Cleaning**:
   - **Transformations**: Convert `reservation_status_date` to datetime format using `pd.to_datetime()`.
   - **Handling Missing Data**: Remove rows with missing data using `dropna()`.
   - **Removal of Columns**: Delete 'company' and 'agent' columns due to high missing values.

4. **Data Exploration and Visualization**:

   - **Exploratory Data Analysis**:
     - **Purpose**: To get unique counts and totals of variables like `hotel`, `is_canceled`, `meal`, `country`, etc.
     - **Visualization Tools**: seaborn, matplotlib

5. **Descriptive Statistics**:
   - **Key Metrics**: Using `describe()` to understand basic statistical details like count, mean, std, min, max, and percentiles.

6. **Trend Analysis**:
   - **Booking Trends**: Analyze patterns over years, months, and week numbers.
   - **Cancellation Trends**: Identify reasons and patterns in booking cancellations.
   - **Guest Demographics**: Examine the distribution of guest types and their origin.

7. **Correlation Analysis**:
   - **Correlation Matrix**: Identify correlations between different numerical features.

### Results
- Insights gained from analyzing booking trends, guest demographics, cancellation patterns, and room assignments.
- Visualization of key trends and correlations to aid in data interpretation.

### Conclusion
- Summarize the key findings and their implications for hotel management and operations.
- Provide recommendations based on the analysis to improve guest satisfaction and operational efficiency.

## Detailed Report
A detailed report has been created to provide an in-depth understanding of the code and analysis. You can access the report using the following [link](https://contra.com/p/eoQOcvrM-hotel-booking-project).
