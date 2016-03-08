#Minimum viable product

##Solution overview

##Functional requirements

* Define post types
* Define custom fields
* Write API endpoints (`/funds`, `/organisations`, `/participants`, `/projects`)
* Write filters/queries on `/participants` endpoing
  * Participant age (range – min/max)
  * Art form (ID of `/artforms`)
  * Funding org (ID of `/organisations`)
  * Fund (ID of `/funds`)
  * Deliver org (ID of `/organisations`)
  * Project cost (range – min/max)
  * Number of participants (range – min/max)
  * Outcome (ID of `/outcomes`)
* Build basic "marketing" site to:
  * Introduce the project
  * State the project's objectives
  * Show how to contribute
  * Show how to get data

##Technical implementation – estimated person-days

Activity | Estimated days
--- | ---
Define post types | 0.5
Define custom fields | 0.5
Write API endpoints | 4
Write filters/queries | 5
Build marketing site | 5
Total | 15 days

##Technical implmentation – estimated elapsed time

6 weeks

##On-going effort

This solution would require a part-time data administer to collect, enter and manage data into the system. Suggest a budget of one person-day per arts project added.

##Advantages

* Quick to specify
* Quick to build
* Lowest implementation cost

##Disadvantages

* Minimal use to non-technical users (only serves an API)
* Arts organisations would have to contact the central team to add data. As a result:
  * High ongoing administrative effort
  * Potential for data entry errors