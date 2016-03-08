#Solution 2 – Adds input form and "My Data" portal

##Solution overview

([Solution 1]((../master/solutions/1-minimum-viable-product.md))) has three major shortcomings:

1. Arts organisations have to contact the system administrator to add their data – they can't do it themselves
2. Arts organisations can't see what they've already submitted
3. End-users (i.e. any consumer of *open data* – arts organisations, government departments, other funders, interested individuals etc.) can't easy query and report on the data without fairly advanced technical skills

This solution addresses points (1) and (2) above by:

* Adding a comprehensive data submission form
* Adding a "My Data" portal where arts organisations can manage their existing data

##Functional requirements

The form built in this stage needs to be able to populate all objects in the data model (approximately represented by the [Mock API](../master/mocked-api))\*:

* Build user registration process
* Build data review/approval process – analogous to editorial flow. New data submissions aren't immediately published, but go into a holding area
* Build data entry process
  * Project information
    * Funding organisation (choose from list defined at `/organisations`)
    * Funding source (choose from list defined at `/funds`)
    * Outcome (choose from list defined at `/outcomes`)
    * Project contacts
      * Name
      * Email
      * etc.
    * Location (exact spec of location to be determined)
    * Title
    * Description
    * Delivery organisation (choose from list defined at `/organisations`)
  * Participant information (a single "row" per participant with the following information)
    * Gender
    * Age
    * Result. This *result* section forms the core of the performance data against which most reporting and analysis will be performed. Suggest a set of generic indicators to indicate how the person performed relative to the desired outcomes, e.g.:
      1. Did not meet
      2. Partially met
      3. Met
      4. Exceeded
      5. Significantly exceeded
    * Other socioeconomic indicators if required
* Build "my data portal"
  * Show existing submissions
  * Edit existing submissions
  * Edit contact details
  * Edit details for "my organisation"

\* The exceptions are the [Outcomes](../master/mocked-api/outcomes.json) and [Artforms](../master/mocked-api/artforms.json) objects. These objects exist in order to help group the projects, and so need to be centrally managed by the project adminstrator to ensure data normality.

##Technical implementation – estimated person-days

Activity | Estimated days
--- | ---
Build solution 1 | 20
Build registration | 3
Build review/approval process | 3
Build data entry forms | 15
Build portal | 10
**Total** | **51 days**

##Technical implmentation – estimated elapsed time

3-4 months, including build of *Solution 1*

##On-going effort

While there's less administrative overhead than Solution 1, some small amount of review/approval and querying will be needed for self-submitted data. We suggest 0.5 days per arts project added.

##Advantages

* Reduced reliance on a central administrator
* Greater engagement of arts organisations – they can manage their own data

##Disadvantages

* Increased cost
* Reporting and analysis still relies on technical know-how