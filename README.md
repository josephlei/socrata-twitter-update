# Socrata Twitter Update Application
####Python + flask application that tweets daily updates of new/modified SOCRATA datasets

Initial version created at the Health 2.0 National Day of Civic Hacking, made available for public use.

This python application checks the metadata of a specified Socrata Open Data Portal and identifies datasets that have are new or have been modified in the last day.  It creates a stack of tweets containing the title and a link to the dataset, then tweets it to Twitter via API.  

We are working to develop a lightweight container for it via Flask and will be posting updates as available; All collaboration is welcome and appreciated!

Known bugs:
* Does not yet check str len to ensure it is under 140 chars, we are writing code to check and truncate long titles
