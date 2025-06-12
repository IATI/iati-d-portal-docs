****************
Filter glossary
****************

This page provides more detail on the filters and options available in d-portal's search function. 
Definitions of the codes used in each filter dropdown can be found in the `IATI Standard <https://iatistandard.org/en/iati-standard/203/activity-standard/>`_. 

Settings:
-------------------

ABC - 123
    This button determines the sort order of the dropdown menus; in alphabetical order, or numerical. 
    For example, alphabetically by DAC 3 digit sector codenames, or numerically by sector codes.

Filters:
-------------------

`Activity Status <https://iatistandard.org/en/iati-standard/203/codelists/activitystatus/>`_
	A code defining the current status of an activity.

`Collaboration Type	<https://iatistandard.org/en/iati-standard/203/codelists/collaborationtype/>`_
    A code defining the type of collaboration involved in an activity's disbursements, for example bilateral or multilateral.

`Default Aid Type <https://iatistandard.org/en/iati-standard/203/codelists/aidtype/>`_	
    A code specifying the default type of aid being supplied in an activity, such as project-type intervention or budget support.
    Individual transactions may have a different code for this element.

`Default Finance Type <https://iatistandard.org/en/iati-standard/203/codelists/financetype/>`_
    A code specifying the default type of finance being described in an activity, such as grants or loans.   
    Individual transactions may have a different code for this element.

`Default Flow Type <https://iatistandard.org/en/iati-standard/203/codelists/flowtype/>`_
    A code defining the default resource flow type for an activity, for example Official Development Assistance (ODA).
    Individual transactions may have a different code for this element.

`Default Tied Status <https://iatistandard.org/en/iati-standard/203/codelists/tiedstatus/>`_	
    A code defining the default tied status of an activity; untied, tied, or partially tied.
    Individual transactions may have a different code for this element.

`Document Category <https://iatistandard.org/en/iati-standard/203/codelists/documentcategory/>`_	
    A code defining the category of documents linked to an activity.

`Humanitarian Activity <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/>`_
    A flag which indicates an activity and/or transaction relates entirely or partially to humanitarian aid.

`Humanitarian Scope Vocab <https://iatistandard.org/en/iati-standard/203/codelists/humanitarianscopevocabulary/>`_
    A code for a recognised vocabulary used to classify emergencies, appeals, and other humanitarian events and actions.

`Participating Organisation <https://iatiregistry.org/publisher/>`_
    Organisations involved in an activity. This filter is not extensive, and only includes Reporting Organisations who have registered data on the IATI registry.
    
.. tip::
    To search for participating organisations not included in the dropdown menu, you can insert their organisation-identifier (org-id) directly into the d-portal url as follows:

        :samp:`d-portal.org/ctrack.html?&/participating-org@ref={org-id}#view=main`

Policy Marker
    A combination of `Policy Significance <https://iatistandard.org/en/iati-standard/203/codelists/policysignificance/>`_ and 
    `Policy Marker <https://iatistandard.org/en/iati-standard/203/codelists/policymarker/>`_ codes. These define a policy or theme addressed by the activity, and 
    the significance of the policy marker for this activity. For example, the code **0_4** filters for "not targeted, Trade Development", while **2_4** filters 
    for "principal objective, Trade Development".

`Reporting Organisation	<https://iatiregistry.org/publisher/>`_
    The organisation reporting an activity, taken from the IATI Registry.

`Recipient Country <https://iatistandard.org/en/iati-standard/203/codelists/country/>`_
    A ISO 3166-1 alpha-2 code specifying the recipient country of an activity or transaction.

`Related Activity Type <https://iatistandard.org/en/iati-standard/203/codelists/relatedactivitytype/>`_
    A code defining the relationship between an IATI activity and another, separately reported IATI activity.
    
`Result Type <https://iatistandard.org/en/iati-standard/203/codelists/resulttype/>`_
    A code defining the type of result being reported in an activity.

`Sector	<https://iatistandard.org/en/iati-standard/203/codelists/sector/>`_
    An OECD DAC 5-digit code classifying the purpose of an activity or transaction.

`Sector Group <https://iatistandard.org/en/iati-standard/203/codelists/sectorcategory/>`_	
    An OECD DAC 3-digit code classifying the purpose of an activity or transaction.

`Tag Vocabulary <https://iatistandard.org/en/iati-standard/203/codelists/tagvocabulary/>`_
    A code defining the tag classification vocabulary used in an activity. For example, the UN Sustainable Development Goals codelist.

Total Outgoing Commitment	
    The sum of all outgoing commitment `type transactions <https://iatistandard.org/en/iati-standard/203/codelists/transactiontype/>`_ in an activity. 
    This can be used to filter activities by minimum and/or maximum total Outgoing Commitment.

`Transaction Type <https://iatistandard.org/en/iati-standard/203/codelists/transactiontype/>`_	
    A code defining the type of transactions in an activity, for example disbursements, or incoming commitments.

Year Range	
    The start and/or end year of an activity, taken from actual and planned `activity dates <DAC 3 digit sector>`_. 
    The filter looks for activities that were active in the period between the minimum and maximum year. 
    So activities that started before the end of the max year and ended after the start of the minimum year will be returned.

