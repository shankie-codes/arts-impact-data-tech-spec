#Arts Impact Data (Wales) Technical Specification

The purpose of this repo is to document the technical solution for the Arts Impact Data project. Solutions needs to:

* Allow for easy upload of project and participant data by community arts organisations and public agencies
* Allow for the uploaded data to be shared
* Provide an online data analysis facility

This repo provides three potential solutions. All solutions are based with WordPress at its core as it is:

* Open source
* Has a large pool of potential developers
* Already runs 22% of the web
* Is extentable with the WP-API (a REST API for WordPress)

Each solution below builds on the one that came before it; however, each solution provides value in its own right. The solutions:

1. [Minimum viable product](../blob/master/solutions/1-minimum-viable-product.md) (MVP). A WordPress application serving a [REST API](https://en.wikipedia.org/wiki/Representational_state_transfer) – with manual data entry by a system administrator.
2. [Adds input form](../blob/master/solutions/2-adds-input-form.md) (MVP). Takes the first solution and adds an easy-to-use front-end form so that individual arts projects can upload their own data
3. [Adds analysis app](../blob/master/solutions/3-adds-analysis-app.md) (MVP). Takes the second solution and adds a comprehensive reporting, analysis and data downloading web app

## Implementation cost

Each proposed solution includes an estimated number of person-days to implement that solution, including previous solution steps, i.e. the estimate for *solution 2* also includes the estimated days for *solution 1* as *solution 1* is a pre-requisite for *solution 2*.