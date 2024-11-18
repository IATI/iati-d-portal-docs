###################
Technical FAQs
###################

Which `transaction types <https://iatistandard.org/en/iati-standard/203/codelists/transactiontype/>`_ are used in summary tables?
    - Spend data is the sum of expenditure and disbursments. If these are not published, outgoing commitments will be used. 
    - Total commitment is the sum of outgoing commitments. If these are not published, expenditure and disbursments will be used.
    - Budget is the sum of `budgets <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/budget/>`_. If these are not published, `planned disbursements <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/planned-disbursement/>`_ will be used.

How is the data cleaned?
    TO BE UPDATED following release of the data policy.

How is data assigned to a specific year?
    - For transactions, using the value or transaction date.
    - For budgets, using the end date.

How are exchange rates calculated?
    Exchange rates are taken from the `Freechange <https://xriss.github.io/freechange-charts/>`_ application. Freechange uses a number of sources for exchange rates, depending on data availability. These are fully described in the `Freechange Github repository <https://github.com/xriss/freechange?tab=readme-ov-file#sources>`_.

    For USD, GBP, EUR, and CAD, currency conversion is carried out when transactions and budgets are imported into d-portal. The `value-date element <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/transaction/value/>`_ is used as the exchange date.

    For all other currencies, transactions and budgets are initially converted into USD. They are then converted into the target currency using today's exchange rate. These values are estimates, and will be less accurate for older transactions. 

Why is my organisation's data missing from a recipient countries chart/table/map?
    - Charts need a transaction with a transaction date in the relevant year, with a valid recipient country code or sector code.
    - Tables need a transaction with a transaction date in the relevant year, with a valid recipient country code or sector code.
    - Maps need transactions with a valid location tag and recipient country code.

Why are graphs missing from my activity?
    Graphs are only shown for an activity if all transactions are in the same currency.

What is the source of country codes and descriptions?
    The `ISO 3166-2 Wikipedia page <https://en.wikipedia.org/wiki/ISO_3166-2>`_.

Where is the additional data used in d-portal stored?
    In `github <https://github.com/IATI/D-Portal/tree/master/dstore/csv>`_. This includes:

    - List of Reporting Organisation IDs
    - Currencies
    -  Exchange rates
    - Sector codes

Why are `sectors <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/sector/>`_ aggregated using `DAC 3 Digit <https://iatistandard.org/en/iati-standard/203/codelists/sectorcategory/>`_ codes?
    Some organisations only publish data with DAC 3 Digit codes. DAC 5 Digit codes are converted to 3 digits for d-portal visualisations.
