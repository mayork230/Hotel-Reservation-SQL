# Hotel Reservation Analysis SQL

![5ey4ifbr](https://github.com/user-attachments/assets/954d780e-118c-45a1-8d84-99d7d5d80f40)

## Table of Contents
- [Introduction](#Introduction)
- [Dataset Overview](#Dataset-Overview)
- [Data Cleaning and Tranformation](#Data-Cleaning-and-Transformation)
- [SQL Analysis and Insights](#SQL-Analysis-and-Insights)
- [Conclusion](#Conclusion)

## Introduction
The hotel industry relies heavily on data to make informed decisions and enhance guest experiences. 
This report delves into the analysis of a hotel reservation dataset, aiming to uncover patterns and 
trends that can drive operational efficiency and boost guest satisfaction. Through SQL queries, 
we extracted valuable insights regarding booking trends, guest preferences, and key operational metrics.

## Dataset Overview
The dataset used in this analysis consists of 700 rows and 12 columns, capturing various aspects of hotel reservations, including:
- Booking_ID: Unique identifier for each reservation.
- no_of_adults: Number of adults in the reservation.
- no_of_children: Number of children in the reservation.
- no_of_weekend_nights: Number of weekend nights in the reservation.
- no_of_week_nights: Number of weekday nights in the reservation.
- type_of_meal_plan: Meal plan chosen by guests.
- room_type_reserved: Type of room reserved.
- lead_time: Days between booking and arrival.
- arrival_date: Date of arrival.
- market_segment_type: Market segment to which the reservation belongs.
- avg_price_per_room: Average price per room in the reservation.
- booking_status: Status of the booking (e.g., confirmed, cancelled).

![Hotel Data Screenshot](https://github.com/user-attachments/assets/f952676c-8d27-4f9b-9852-6d9a5eb0beac)

## Data Cleaning and Transformation

- Handling Missing values
```sql
SELECT * 
FROM reservations
WHERE no_of_adults IS NULL
   OR no_of_children IS NULL
   OR no_of_weekend_nights IS NULL
   OR no_of_week_nights IS NULL
   OR type_of_meal_plan IS NULL
   OR room_type_reserved IS NULL
   OR lead_time IS NULL
   OR arrival_date IS NULL
   OR market_segment_type IS NULL
   OR avg_price_per_room IS NULL
   OR booking_status IS NULL;
```
- Checking for Duplicates Records
```sql
  select Booking_ID, count(*) from reservation
group by Booking_ID
having count(*) >1;
```
  
