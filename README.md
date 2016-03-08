#Arts Impact Data (Wales) Technical Specification

The purpose of this repo is to document the technical solution for the Arts Impact Data project. Solutions needs to:

* Allow for easy upload of project and participant data by community arts organisations and public agencies
* Allow for the uploaded data to be shared
* Provide an online data analysis facility

This repo provides three potential solutions. All solutions are based with WordPress at its core as it is:

* Open source
* Has a large pool of potential developers
* Already runs 26% of the web
* Is extentable with the WP-API (a REST API for WordPress)

Each solution below builds on the one that came before it; however, each solution provides a solution to the problem of "how to store and report arts impact data" in its own right. The solutions:

1. [Minimum viable product](../master/solutions/1-minimum-viable-product.md) (MVP). A WordPress application serving a [REST API](https://en.wikipedia.org/wiki/Representational_state_transfer) – with manual data entry by a system administrator.
2. [Adds input form and "my data" portal](../master/solutions/2-adds-input-form.md) (MVP). Takes the first solution and adds an easy-to-use front-end form so that individual arts projects can upload their own data. Also adds a "my data" portal so that arts organisations can manage their own data
3. [Adds analysis app](../master/solutions/3-adds-analysis-app.md) (MVP). Takes the second solution and adds a comprehensive reporting, analysis and data downloading web app

While we assume that WordPress will form the core of the data store, all interactive sections of the application (i.e. the bulk of Solution 2 and Solution 3) should use a client-side JavaScript framework, such as React or Angular, to ensure the most fluid user experience.

The platform should provide a first-class user experience on any modern device (desktop, tablet or phone) using modern-ish browsers. To focus the developers on implementing features rather than supporting old browsers, the platform should support all [evergreen browsers](http://eisenbergeffect.bluespire.com/evergreen-browsers/) (i.e. Chrome, Safari, Firefox, Opera, Edge) plus Internet Explorer 10 and above.

##Solution assumptions

The following assumptions apply to all solutions:

* **Each funding source (*fund* in the terminology used here) has a single outcome/objective**. Although we recognise that funds may have multiple objectives, this solution assumes that they have a primary objective against which projects can manage their success (e.g. *reduction in unemployment*, *improved life satisfaction*, *reduced obesity* etc.). This assumption is critical as it allows vastly simplified analysis and reporting. This is easier to explain if we give a counter-example: if a funding source (and by extension a project calling on that funding source) has multiple objectives, there's no way to conclusively establish a relationship between the outcomes (e.g. 70% of participants showed an improvement in their life satisfaction) and the cost per head of the programme

##Implementation cost

Each proposed solution includes an estimated number of person-days to implement that solution, including previous solution steps, i.e. the estimate for *solution 2* also includes the estimated days for *solution 1* as *solution 1* is a pre-requisite for *solution 2*.

##Ongoing hosting and technical support
The solution will need hosting (its own virtual server) and technical support. The project should budget at least £50/month for this on an ongoing basis.