###################
Technical FAQs
###################

1. :ref:`Which transaction types are used in summary tables? <faq_a>`
2. :ref:`How is the data cleaned? <faq_b>`
3. :ref:`How is data assigned to a specific year? <faq_c>`
4. :ref:`How are exchange rates calculated? <faq_d>`
5. :ref:`Why is my organisation's data missing from a recipient country's chart/table/map? <faq_e>`
6. :ref:`Why are graphs missing from my activity? <faq_f>`
7. :ref:`Why do graphs start at 1970-01-01 for my activity? <faq_g>`
8. :ref:`What is the source of country codes and descriptions? <faq_h>`
9. :ref:`Where is the additional data used in d-portal stored? <faq_i>`
10. :ref:`Why are sectors aggregated using DAC 3 Digit codes? <faq_j>`
11. :ref:`How are results percentages calculated? <faq_k>`

| 

---------

| 

.. _faq_a: 

<<<<<<< formatting
\1. Which :iati-reference:`transaction/transaction-type` are used in summary tables?
=======
\1. Which `transaction types <https://iatistandard.org/en/iati-standard/203/codelists/transactiontype/>`_ are used in summary tables?
>>>>>>> main
    - Spend data is the sum of expenditure and disbursements. If these are not published, outgoing commitments will be used. 
    - Total commitment is the sum of outgoing commitments. If these are not published, expenditure and disbursements will be used.
    - Budget is the sum of  :iati-reference:`budget/value`. If these are not published, :iati-reference:`planned-disbursement/value` will be used.

.. _faq_b: 

\2. How is the data cleaned?
    To be updated following finalisation of new data policy.

.. _faq_c: 

\3. How is data assigned to a specific year?
    - For transactions, using :iati-reference:`transaction/transaction-date`, else :iati-reference:`transaction/value/@value-date`.
    - For budgets, using :iati-reference:`budget/period-end`.

.. _faq_d: 

\4. How are exchange rates calculated?
    Exchange rates are taken from the `Freechange <https://xriss.github.io/freechange-charts/>`_ application. Freechange uses a number of sources for exchange rates, depending on data availability. These are fully described in the `Freechange Github repository <https://github.com/xriss/freechange?tab=readme-ov-file#sources>`_.

    For USD, GBP, EUR, and CAD, currency conversion is carried out when transactions and budgets are imported into d-portal. The `value-date element <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/transaction/value/>`_ is used as the exchange date.

    For all other currencies, transactions and budgets are initially converted into USD. They are then converted into the target currency using today's exchange rate. These values are estimates, and will be less accurate for older transactions. 

.. _faq_e: 

\5. Why is my organisation's data missing from a recipient country's chart/table/map?
    - Charts need a transaction with a :iati-reference:`transaction/transaction-date` in the relevant year, with a valid :iati-reference:`recipient-country/@code` or :iati-reference:`sector/@code`.
    - Tables need a transaction with a :iati-reference:`transaction/transaction-date`in the relevant year, with a valid :iati-reference:`recipient-country/@code` or :iati-reference:`sector/@code`.
    - Maps need transactions with a valid :iati-reference:`location/point/pos` and :iati-reference:`recipient-country/@code`.

.. _faq_f: 

\6. Why are graphs missing from my activity?
    Graphs are only shown for an activity if all transactions are in the same currency.

.. _faq_g: 

\7. Why do graphs start at 1970-01-01 for my activity?
    D-portal does not adjust the x-axis when there is only one transaction of a given type, or if all transactions are on the same date.
    The axis will be adjusted when more transactions are added.

.. _faq_h: 

\8. What is the source of country codes and descriptions?
    The `ISO 3166-2 Wikipedia page <https://en.wikipedia.org/wiki/ISO_3166-2>`_.

.. _faq_i: 

\9. Where is the additional data used in d-portal stored?
    In `github <https://github.com/IATI/D-Portal/tree/master/dstore/csv>`_. This includes:

    - List of Reporting Organisation IDs
    - Currencies
    -  Exchange rates
    - Sector codes

.. _faq_j: 

<<<<<<< formatting
\10. Why are :iati-reference:`sector/@code` aggregated using `DAC 3 Digit <https://iatistandard.org/en/iati-standard/203/codelists/sectorcategory/>`_ codes? 
=======
\10. Why are `sectors <https://iatistandard.org/en/iati-standard/203/activity-standard/iati-activities/iati-activity/sector/>`_ aggregated using `DAC 3 Digit <https://iatistandard.org/en/iati-standard/203/codelists/sectorcategory/>`_ codes? 
>>>>>>> main
    Some organisations only publish data with DAC 3 Digit codes. DAC 5 Digit codes are converted to 3 digits for d-portal visualisations.

.. _faq_k:

\11. How are results percentages calculated? 
    The results percentage is the :iati-reference:`result/indicator/period/actual/@value`, expressed as a percentage from the :iati-reference:`result/indicator/baseline/@value` 
    to the :iati-reference:`result/indicator/period/target`. 
    
    It is clamped from 0 to 100.
    If the target or actual value is less than the baseline value, the percentage will be 0%.

    For example, a result could have baseline of 10, a target of 100, and an actual value of 50. 

    - The baseline to target value change is: ``100 - 10 = 90``
    - The baseline to actual value change is: ``50 - 10 = 40``
    - The results percentage is therefore: ``40/90 x 100 = 44%``
