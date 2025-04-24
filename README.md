# mist4610groupproj2
Team Name:

21482 Group 1

Team Members:

Sophie Naustdal https://github.com/sophienaustdal/MIST4610GroupProject2.git
Riley Cook https://github.com/rileyacook/4610Proj2
Rachel Chuan
Chidera Nwosu
Coleman Vaughn
Description of Dataset:

Question 1:

Question: What are the top 15 components that have the highest potential impact across the top 5 manufacturers with the most frequent recalls? How many vehicles are possibly affected by each component for each manufacturer?

Importance: 
Lets us pinpoint which components cause the most problems across those 5 manufacturers
Supports Consumer safety by identifying potential failures early
Avoiding repeating recalls on the same components can potentially save companies millions in repair, legal, and reputational costs
Will reveal patterns in component failure that will lead to improved designs, supplier choices, or quality control practices


Screenshot 2025-04-22 at 7 17 19 PM
Through filtering the manufacturers by top 5 by [Recall Count] and the components by top 15 by SUM([Potentially Affected]), this graph identifies the top 5 manufacturers with the most amount of recalls and the top 15 components that affect the most vehicles. The SUM([Potentially Affected]) was placed in the color mark to illustrate the total number of possibly affected vehicles for each component recall for each of the manufacturers. The lighter colors indicate components that affect fewer vehicles, while the darker colors highlight the highest-risk components. A grand total row was added to show how many total vehicles could be affected by each manufacturer for these components. The results were sorted in ascending order by the grand total of SUM([Potentially Affected]) within each manufacturer, and also in descending order by the grand total of SUM([Potentially Affected]) of each component. This allows us to quickly identify which components are the most critical and affect the most amount of vehicles, and also which manufacturers are the leading contributors to the most amount of recalls. Our results indicate that air bags, electrical system, and power train components have the highest potential impact across all components. Particularly, for General Motors, air bags are the riskiest component, prompting further investigation and likely higher standards and regulations needing to be put in place. The recalled components of General Motors, Ford, and Chrysler affect the largest number of vehicles as compared to Daimler Trucks and Forest River, which have fewer, likely due to their specialization in commercial vehicles. The results from this visualization are useful in order to pinpoint which vehicle components regulators should focus on, as they likely need better industry standards. These findings would be especially important for manufacturers to identify which specific components need more quality control. It could also be important for consumers when making buying decisions, as they could identify which manufacturers to possibly steer clear of.

Question 2:

Question Part 1: Since vehicles and equipment are the most frequently recalled items, which of our “major brands” have the highest number of recalls in these categories? Question Part 2: For the top three brands, what specific components are most commonly found to be faulty?

Importance: Part 1: 
Understanding which major brands have the most commonly faulty components helps us pinpoint recurring issues, assess potential risks, and guide quality control efforts, as well as help maintain brand reputation. 


Manipulations Applied:

Permanent Filters:
Report Received Date: filtered from 2000 - 2025 to manage high volume and increase relevance.
Calculated Field:
Recall Count: COUNT([Nhtsa Id]) 
Data Used:
Report Received Date, Nhtsa id, Manufacturer, Recall Type, Component, Potentially Affected.


Part 1:

“Major Brands”: Ford, GM, Chrysler, BMW, Mercedes, Volkswagen, Honda, Nissan, Hyundai, Kia, Subaru, Tesla, Mazda, Toyota

Category: Vehicle and Equipment

Part 2:

Category: Vehicle

Components: All Vehicle Components with COUNT(Recall Count) >= 10

Brands: GM, Ford, Chrysler

Tableau Packaged Workbook:
