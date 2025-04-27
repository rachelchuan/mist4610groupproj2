# Group 1 MIST4610 Group Project 2

## Team Name:
21482 Group 1

## Team Members:
1. Sophie Naustdal https://github.com/sophienaustdal/MIST4610GroupProject2.git
2. Riley Cook https://github.com/rileyacook/4610Proj2 
3. Rachel Chuan https://github.com/rachelchuan/mist4610groupproj2/blob/main/README.md
5. Chidera Nwosu
6. Coleman Vaughn https://github.com/Colemanv33/groupproject2

## Description of Dataset:

## Question 1:
Question: What are the top 15 components that have the highest potential impact across the top 5 manufacturers with the most frequent recalls? How many vehicles are possibly affected by each component for each manufacturer?

Importance:

<img width="1200" alt="Screenshot 2025-04-22 at 7 17 19 PM" src="https://github.com/user-attachments/assets/9b989a3b-5f9b-448f-b599-8dd0e4b78ce3" />


Through filtering the manufacturers by top 5 by [Recall Count] and the components by top 15 by SUM([Potentially Affected]), this graph identifies the top 5 manufacturers with the most amount of recalls and the top 15 components that affect the most vehicles. The SUM([Potentially Affected]) was placed in the color mark to illustrate the total number of possibly affected vehicles for each component recall for each of the manufacturers. The lighter colors indicate components that affect fewer vehicles, while the darker colors highlight the highest-risk components. A grand total row was added to show how many total vehicles could be affected by each manufacturer for these components. The results were sorted in ascending order by the grand total of SUM([Potentially Affected]) within each manufacturer, and also in descending order by the grand total of SUM([Potentially Affected]) of each component. This allows us to quickly identify which components are the most critical and affect the most amount of vehicles, and also which manufacturers are the leading contributors to the most amount of recalls. Our results indicate that air bags, electrical system, and power train components have the highest potential impact across all components. Particularly, for General Motors, air bags are the riskiest component, prompting further investigation and likely higher standards and regulations needing to be put in place. The recalled components of General Motors, Ford, and Chrysler affect the largest number of vehicles as compared to Daimler Trucks and Forest River, which have fewer, likely due to their specialization in commercial vehicles. Thus, component recalls have a greater impact on passenger vehicles as compared to commercial vehicles. The results from this visualization are useful in order to pinpoint which vehicle components regulators should focus on, as they likely need better industry standards. These findings would be especially important for manufacturers to identify which specific components need more quality control. It could also be important for consumers when making buying decisions, as they could identify which manufacturers to possibly steer clear of.

## Question 2:

Question:
- Part 1: Since vehicles and equipment are the most frequently recalled items, which of our “major brands” have the highest number of recalls in these categories? 
- Part 2: For the top three brands, what specific components are most commonly found to be faulty?

Importance:


Part 1:

<img width="1185" alt="Screenshot 2025-04-25 at 10 23 47 AM" src="https://github.com/user-attachments/assets/92f52514-c5f7-468b-b5a7-acc7f20eb106" />

Manipulations:

“Major Brands”: Ford, GM, Chrysler, BMW, Mercedes, Volkswagen, Honda, Nissan, Hyundai, Kia, Subaru, Tesla, Mazda, Toyota

Category: Vehicle and Equipment

We observed that, of our four categories of "Recall Type" (Vehicle, Equipment, Tire, Child Seat), Vehicle and Equipment recalls far outweighed the latter two. Following this, we wanted to narrow our large data pool into relevant information, so the "Major Brands" filter was created. Comparing our brands to the number of recalls, we found two key pieces of information-- Ford, GM, and Chrysler are the most recalled brands, and Vehicular recalls were much higher than Equipment recalls consistently per brand. 


Part 2:

<img width="1182" alt="Screenshot 2025-04-25 at 10 28 21 AM" src="https://github.com/user-attachments/assets/b6cb8194-02c3-4103-8f69-7af9457b2aa8" />

<img width="1069" alt="Screenshot 2025-04-25 at 10 57 59 AM" src="https://github.com/user-attachments/assets/a8504ed5-1438-4c8b-9e5d-947bad4c6f4c" />


Manipulations:

Category: Vehicle

Components: All Vehicle Components with COUNT(Recall Count) >= 10

Manufacturer: Top 3 by COUNT(Recall Count)

Seeing that Ford, GM, and Chrysler were the highest in recall numbers, as well as Vehicle recalls being more prevalent in our dataset, we decided to further look into which specific parts of vehicles were faulty for these high-risk brands. Our graph shows that Brakes, Steering, Electrical, Power Train, and Fuel Systems are the top issues for each brand. Having this information in hand it can be useful for both the producer and consumer. On the end of the manufacturer, such as our top 3, they can pinpoint recurring issues, assess risks and implement risk management techniques, and improve quality control efforts (i.e., increased training, higher job requirements, etc.), to help maintain brand reputation. Additionally, a car buyer may utilize this data to make a better informed decision prior to making a large financial commitment.

## Dataset Manipulations:

We only had one permanent filter on our data, which was the Report Received Date. We only used data that was reported between 2000 and 2025. This decision was made to increase the relevance it had to our questions and just to manage the sheer size of the data we had. We also created a calculated field called "Recall Count." This was just a COUNT function of the Nhtsa Id since each recall had its own unique Id associated with it. We only actually used a small percentage of the rows in the dataset to create our questions. The rows we used included: Report Received Date, Nhtsa id, Manufacturer, Recall Type, Component, and Potentially Affected.


## Tableau Packaged Workbook:
