#Phase 2 – Build a platform to serve the data model

##Phase overview

Build a permanent home for the data that replicates the data model prototyped in Phase 1. AirTable is great for mocking up data models, but has a number of shortcomings:

* No multilingual support
* No ability to build a wider "site" around the data
* No ability to customise API

The purpose of this phase is to build a platform that's a permanent home for the data – and addresses the shortcomings of AirTable. The platform will be built by customising an existing web framework, such as WordPress or a NodeJS stack. The rest of this document will assume WordPress (due to its built-in admin interface). The phase needs to build a platform that:

* Gives administrators an interface to enter data
* Serves that data back out to the world using a JSON API

The rest of this solution assumes WordPress as the platform as:

* It's open source
* Has a large pool of potential developers
* Already runs 26% of the web
* Is extendable with the WP-API (a REST API for WordPress)

However, this platform could be built on other software, such as the MEAN stack for NodeJS, without issue.

This phase doesn't include end-user-friendly data entry ([phase 3]((../master/phases/3-input-form.md))). Because this phase does not have front-end data entry for end users, data would be entered by a skilled administrator directly into the WordPress dashboard. The site's data, would then be available through a [REST API](https://en.wikipedia.org/wiki/Representational_state_transfer) and a CSV download.

This phase would also implement a basic "marketing site" for the data platform to:

* Advertise the service's existence
* Explain what the service is for
* Explain how to add data to the project (i.e. contact the administrator, in this phase)
* Explain how to get data out (document the API endpoints)

##Functional requirements

* Define post types
* Define custom fields
* Write API endpoints (`/organisations`, `/participants`, `/projects`) – `GET` requests only
* Write filters/queries on `/participants` endpoint
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

##Technical implementation – estimated elapsed time

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