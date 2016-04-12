#Phase 1 – Prototype using off the shelf services

##Phase overview

Develop a data model, mock it up, and test it using an off-the shelf product. This repo contains a first guess at a data model for Arts Impact Data; however, this model hasn't been validated with either data providers or data consumers. This first phase should validate that the model we've imagined works and changed it if it doesn't.

Rather than build the data model into a platform, we suggest using an off-the-shelf tool called [AirTable](https://airtable.com/). AirTable allows us to mock up the data model very quickly using an app that looks like a spreadsheet – but gives us both a data entry form and JSON API for free, allowing us to quickly iterate the model at test the outputs.

This stage has minimal development, but serves to lock down the data model before building the platform.

## Technical solution

This phase will use:

* Airtable (or similar)
* Postman API client for validating output

##Technical implementation – estimated person-days

Activity | Estimated days
--- | ---
Refine data model (1st iteration) | 4
Refine data model (2nd iteration) | 2
Refine data model (3rd iteration) | 2
**Total** | **8 days**

##Technical implementation – estimated elapsed time

6 weeks

##On-going effort

None anticipated.

##Advantages

* No code
* Quick turnaround, easy to make changes
* Mock-up data entry forms and API for free

##Disadvantages

* Single language
* No page content, marketing information or branding – uses AirTable only