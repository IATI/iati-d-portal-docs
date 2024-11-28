**************
Data Validity and Logs
**************

D-portal includes tools which can be used to investigate missing data and errors.

`Dash <https://d-portal.org/ctrack.html?#view=dash>`_ 
    Dash provides an overview of the data populating d-portal from individual reporting organisations. This includes summary statistics, and reports on errors such as invalid recipient countries.
    By showing where invalid data is reported, Dash can help to explain gaps in the data.

`d-portal Logs <https://xriss.github.io/D-Portal-Logs/>`_
    The d-portal logs site hosts two tools; Database Logs and Xpath Stats.

    Database Logs provides a snapshot of all data found in the live d-portal database. This updates nightly, and can be viewed as a table or historical charts.

    Xpath Stats show how much each element of the IATI standard is used in activity or organisation data. This can be viewed as a percentage or as a historical timeline of use. 
    Individual reporting organisations use of the IATI standard elements can also be explored.

`Cleanerr <https://notshi.github.io/cleanerr/>`_
    Cleanerr reports issues with individual datasets. 
    These include:

    - Duplicate organisation identifiers
    - Duplicate activity identifiers
    - Download and import errors
