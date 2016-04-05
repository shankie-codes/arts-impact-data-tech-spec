#Phase 1 – Minimum viable product (MVP)

##Phase overview

Build a WordPress data store for arts impact data. The MVP is to build a WordPress site that stores the data and serves it out to the public – but doesn't include the user-friendly data ingestion ([phase 2]((../master/phases/2-input-form-and-api.md))) or data analysis/export ([phase 3]((../master/phases/3-adds-analysis-app.md))) as these are significant pieces of work in their own right.

Because the MVP would not have front-end data entry for end users, data would be entered by a skilled administrator directly into the WordPress dashboard. The site's data, in the MVP, would be available through a [REST API](https://en.wikipedia.org/wiki/Representational_state_transfer) and a CSV download.

The purpose of this phase is to prove the data model matches the reality, i.e. an administrator can use the system to describe the outcomes of a real-world project.

The MVP would also implement a basic "marketing site" for the data platform to:

* Adverstise the service's existance
* Explain what the service is for
* Explain how to add data to the project (i.e. contact the administrator, in this phase)
* Explain how to get data out (document the API endpoints)

##Functional requirements

* Define post types
* Define custom fields
* Write API endpoints (`/organisations`, `/participants`, `/projects`) – `GET` requests only
* Write filters/queries on `/participants` endpoing
  * Participant age (range – min/max)
  * Art form (ID of `/artforms`)
  * Funding org (ID of `/organisations`)
  * Deliver org (ID of `/organisations`)
  * Project cost (range – min/max)
  * Number of participants (range – min/max)
  * Outcome (ID of `/outcomes`)
* Build CSV download
* Build basic "marketing" site to:
  * Introduce the project
  * State the project's objectives
  * Show how to contribute
  * Show how to get data

## Technical solution

This phase will use:

* WordPress
* WordPress custom post types
* Advanced Custom Fields (ACF) for WordPress
* WordPress REST API (new feature in core or plugin, as required)

##Technical implementation – estimated person-days

Activity | Estimated days
--- | ---
Define post types | 0.5
Define custom fields | 0.5
Write API endpoints | 3
Document API endpoints | 2
Write API filters/queries | 4
Build CSV download | 2
Build marketing site | 5
Implement multilingual functionality | 3
**Total** | **20 days**

##Technical implmentation – estimated elapsed time

6 weeks

##On-going effort

This phase would require a part-time data administer to collect, enter and manage data into the system. Suggest a budget of 2 person-days per arts project added.

##Advantages

* Quick to specify
* Quick to build
* Lowest implementation cost

##Disadvantages

* Minimal use to non-technical users (only serves an API)
* Arts organisations would have to contact the central team to add data. As a result:
  * High ongoing administrative effort
  * Potential for data entry errors