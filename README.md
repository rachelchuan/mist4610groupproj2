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
Our dataset is comprised of vehicle, equipment, tire, and child seat recalls from 1/19/1966 - 4/4/2025 and was published by the National Highway Traffic Safety Administration. The data reporting requirements are made by manufacturers who determine that a product or piece of original equipment either contains a safety defect or is not in compliance with Federal safety standards. Our data columns include: Report Received Date, Nhtsa Id, Recall Link, Manufacturer, Subject, Component, Mfr Campaign Number, Recall Type, Potentially Affected, Recall Description, Consequence Summary, Corrective Action, Park Outside Advisory, and Do Not Drive Advisory. The dataset has 28,895 rows, indicating the total number of recalls. The dataset comprises 2,208 manufacturers and 41 components that were part of these recalls.


## Question 1:
Question: What are the top 15 components that have the highest potential impact across the top 5 manufacturers with the most frequent recalls? How many vehicles are possibly affected by each component for each manufacturer?

Importance:
This question lets us pinpoint which components cause the most problems across the top 5 most recalled manufacturers. The resulting visualization could be a very important tool for regulators, manufacturers, and consumers. Regulators can identify which components need higher regulations and which manufacturers need to be more closely monitored. It can further support consumer safety by identifying potential failures early. Also, by highlighting risky component recalls, manufacturers can avoid repeated recalls on the same components, thus potentially saving companies millions in repair, legal, and reputational costs. Overall, the heatmap reveals patterns in component failure that could lead to improved designs, better informed supplier choices, and higher quality control practices.

<img width="1121" alt="Screenshot 2025-04-27 at 7 15 57 PM" src="https://github.com/user-attachments/assets/8003e1a8-eadd-4ef7-afe0-6924eccb9c79" />

Through filtering the manufacturers by the top 5 by [Recall Count] and the components by the top 15 by SUM([Potentially Affected]), this graph identifies the top 5 manufacturers with the most amount of recalls and the top 15 components that affect the most vehicles. The SUM([Potentially Affected]) was placed in the color mark to illustrate the total number of possibly affected vehicles for each component recall for each of the manufacturers. The lighter colors indicate components that affect fewer vehicles, while the darker colors highlight the highest-risk components. A grand total row was added to show how many total vehicles could be affected by each manufacturer for these components. The results were sorted in ascending order by the grand total of SUM([Potentially Affected]) within each manufacturer, and also in descending order by the grand total of SUM([Potentially Affected]) of each component. This allows us to quickly identify which components are the most critical and affect the most amount of vehicles, and also which manufacturers are the leading contributors to the most amount of recalls. Our results indicate that air bags, electrical system, and power train components have the highest potential impact across all components. Particularly, for General Motors, air bags are the riskiest component, prompting further investigation and likely higher standards and regulations needing to be put in place. The recalled components of General Motors, Ford, and Chrysler affect the largest number of vehicles as compared to Daimler Trucks and Forest River, which have fewer, likely due to their specialization in commercial vehicles. Thus, component recalls have a greater impact on passenger vehicles as compared to commercial vehicles. The results from this visualization are useful in order to pinpoint which vehicle components regulators should focus on, as they likely need better industry standards. These findings would be especially important for manufacturers to identify which specific components need more quality control. It could also be important for consumers when making buying decisions, as they could identify which manufacturers to possibly steer clear of.

## Question 2:

Question:
- Part 1: Since vehicles and equipment are the most frequently recalled items, which of our “major brands” have the highest number of recalls in these categories? 
- Part 2: For the top three brands, what specific components are most commonly found to be faulty?

Importance:
This question allows us to understand which major brands have the most commonly faulty components. The results could help us pinpoint recurring issues, assess potential risks, guide quality control efforts, as well as help maintain brand reputation.

Part 1:

<img width="1121" alt="Screenshot 2025-04-27 at 7 17 04 PM" src="https://github.com/user-attachments/assets/95cf9b08-c3cb-4363-b526-59bec8056703" />


We filtered manufacturers to include "major brands", as the common manufacturers most people think of. The filter included Ford, GM, Chrysler, BMW, Mercedes, Volkswagen, Honda, Nissan, Hyundai, Kia, Subaru, Tesla, Mazda, and Toyota. Recall type, which included the categories of Vehicle and Equipment, was placed in the color mark to differentiate the two more easily. We observed that, of our four categories of "Recall Type" (Vehicle, Equipment, Tire, Child Seat), Vehicle and Equipment recalls far outweighed the latter two. Following this, we wanted to narrow our large data pool into relevant information, so the "Major Brands" filter was created. Comparing our brands to the number of recalls, we found two key pieces of information: Ford, GM, and Chrysler are the most recalled brands, and Vehicular recalls were much higher than Equipment recalls consistently per brand. 


Part 2:

<img width="1124" alt="Screenshot 2025-04-27 at 7 26 53 PM" src="https://github.com/user-attachments/assets/887e06be-f36c-4578-9263-5e2a4d75da85" />

Seeing that Ford, GM, and Chrysler were the highest in recall numbers, as well as Vehicle recalls being more prevalent in our dataset, we decided to further look into which specific parts of vehicles were faulty for these high-risk brands. We filtered manufacturers to display the top 3 most recalled brands based on their [Recall Count]. The vehicle components were filtered to show the top 10 by [Recall Count]. The Recall Type was also filtered to display only "Vehicle" recalls. Our graph shows that electrical system, air bags, power train, service brakes, and steering are the top issues for each brand. Having this information in hand can be useful for both the producer and consumer. For the manufacturer, such as our top 3, they can pinpoint recurring issues, assess risks and implement risk management techniques, and improve quality control efforts (i.e., increased training, higher job requirements, etc.), to help maintain brand reputation. Additionally, a car buyer may utilize this data to make a better informed decision prior to making a large financial commitment.

## Dataset Manipulations:

We used one permanent filter on our data, which was the Report Received Date. We decided to use data that was reported between 2000 and 2025. This decision was made to increase the relevance it had to our questions and to manage the sheer size of the data we had. We also created a calculated field called "Recall Count." This was a COUNT function of the Nhtsa Id since each recall had its own unique ID associated with it. We only used a small percentage of the rows in the dataset to create our questions. The rows we used included: Report Received Date, Nhtsa Id, Manufacturer, Recall Type, Component, and Potentially Affected.


## Tableau Packaged Workbook:
The packaged workbook has been added as a file to this repository.
