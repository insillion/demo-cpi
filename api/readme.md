# API kit

There are 300+ APIs available in Insillion, we would be focussing on API's needed for integrating with an Agent/Broker portal (B2B user) or Customer portal (B2C user).
This section is used by an implementation team that wishes to build its own Front-end portal connecting to the Carrier's Commmercial Property Insurance backend for Rating, underwriting, submission, bind, payment and administration. Below are the brief list of APIs:

|# | API | Description |
|:--:|:--:|:--|
|01|[auth](01-auth.md)| Authentication request & response|
|02|[master](./)| Master request & response|
|03|[Premium Calculation](03-premium-calc.md)|Premium Calculation or Rating API to get the price|
|04|[Quote Save ](04-quote-save.md)| Create new Quote or Save existing quote|
|05|[View Quote](05-view-quote.md)| View existing Quote|
|06|[Finalize Quote ](06-quote-finalize.md)| Submit Quote or lock the quote edits|
|07|[Quote PDF](07-quote-pdf.md)| Download Quote PDF|
|10|[Payment](10-confirm-pay.md)| Cash payment and Stripe (online) Payment requests|

Shortly, more API's would be made available - for Issuance, Policy PDFs, Endorsements, Renewals etc.
