#Phase 3 – Analysis app

##Phase overview

([Phase 2]((../master/phases/1-minimum-viable-product.md))) has one major shortcoming: End-users (i.e. any consumer of *open data* – arts organisations, government departments, other funders, interested individuals etc.) can't easily query and report on the data without fairly advanced technical skills

Phase 3 creates a comprehensive querying and analysis portal. The portal should:

* Provide comprehensive filtering based on project and cohort parameters to arrive at a target set e.g. 
  * Age range
  * Outcome
  * Funding organisation
  * Location, etc.
* Display summary statistics, e.g.
  * Average age
  * Average cost per participant
  * Map
  * Summary graphs/charts, e.g. pie chart showing the distribution of results
    * [Individual charts need further specification work]
* Display a list of all projects that meet the filtered criteria. Link to an individual project page, showing more data
* Link to a download (CSV or XLS) of the individual participant data* that the user has filtered

All output data in the portal (i.e. summary statistics, graphs, maps, and the data download set) should update dynamically as the user updates the query filters.

[Insert wireframes]

The analysis app should be completed in three iterations, accounting for feedback from interested parties at each iteration.

\* The data will not include any data that allows identification of an individual as the platform will not collect this data (e.g. name, address etc.) in the first place

##Functional requirements

* Build basic API abstraction (for the rest of the app to use)
* Build filters – individual solution for each filter, e.g. *age range* needs a different filtering mechanism to *location*
* Build summary statistics
* Build map
* Build summary charts
* Build "single project" view
* Build CSV extract functionality. This needs to take the returned JSON (which is displayed in the stats and charts) and transpose it into CSV

##Technical solution

Like Phase 2, Phase 3 should use the public REST API directly. Also like Phase 2, Phase 3 should use a client-side JavaScript framework, such as React or Angular to keep the interface fast and fluid.

The portal should be implemented as a single-page app; however, filtering should push URL parameters so that a particular filtered query can be bookmarked, shared and revisited.

##Technical implementation – estimated person-days

Activity | Estimated days
--- | ---
API abstraction for app | 3
Core app data model | 8
Filters | 10
Map | 5
"Single project" view | 5
CSV extract | 5
Design and layout | 10
**Total** | **47 days**

##Technical implmentation – estimated elapsed time

6 – 8 months.

##On-going effort

The ongoing effort for Phase 3 will be similar to Phase 2, at perhaps 0.5 day per project added to the platform.

##Advantages

* Comprehensive self-service for funding organisations, arts organsations and the general public to query and draw their own conclusions on the efficacy of community arts projects
* Full open data. Data sets can be refined and downloaded as required from the portal

##Disadvantages

* Implementation cost and effort