.. _v2/settlements-get-open:

Get open settlement
===================
.. api-name:: Settlements API
   :version: 2

.. endpoint::
   :method: GET
   :url: https://api.mollie.com/v2/settlements/open

.. authentication::
   :api_keys: false
   :oauth: true

Retrieve the details of the open balance of the organization. This will return a settlement object representing your
organization's balance.

Response
--------
``200`` ``application/hal+json; charset=utf-8``

The open balance settlement is returned in the same fashion as the :ref:`Get settlement <v2/settlements-get>` endpoint.

Example
-------

Request
^^^^^^^
.. code-block:: bash
   :linenos:

   curl -X GET https://api.mollie.com/v2/settlements/open \
       -H "Authorization: Bearer access_Wwvu7egPcJLLJ9Kb7J632x8wJ2zMeJ"

Response
^^^^^^^^
.. code-block:: http
   :linenos:

   HTTP/1.1 200 OK
   Content-Type: application/hal+json; charset=utf-8

   {
       "resource": "settlement",
       "id": "open",
       "reference": null,
       "createdAt": "2018-04-06T06:00:01.0Z",
       "settledAt": null,
       "amount": {
           "currency": "EUR",
           "value": "39.75"
       },
       "periods": {
           "2018": {
               "4": {
                   "revenue": [
                       {
                           "description": "iDEAL",
                           "method": "ideal",
                           "count": 6,
                           "amountNet": {
                               "currency": "EUR",
                               "value": "86.1000"
                           },
                           "amountVat": null,
                           "amountGross": {
                               "currency": "EUR",
                               "value": "86.1000"
                           }
                       },
                       {
                           "description": "Refunds iDEAL",
                           "method": "refund",
                           "count": 2,
                           "amountNet": {
                               "currency": "EUR",
                               "value": "-43.2000"
                           },
                           "amountVat": null,
                           "amountGross": {
                               "currency": "EUR",
                               "value": "43.2000"
                           }
                       }
                   ],
                   "costs": [
                       {
                           "description": "iDEAL",
                           "method": "ideal",
                           "count": 6,
                           "rate": {
                               "fixed": {
                                   "currency": "EUR",
                                   "value": "0.3500"
                               },
                               "percentage": null
                           },
                           "amountNet": {
                               "currency": "EUR",
                               "value": "2.1000"
                           },
                           "amountVat": {
                               "currency": "EUR",
                               "value": "0.4410"
                           },
                           "amountGross": {
                               "currency": "EUR",
                               "value": "2.5410"
                           }
                       },
                       {
                           "description": "Refunds iDEAL",
                           "method": "refund",
                           "count": 2,
                           "rate": {
                               "fixed": {
                                   "currency": "EUR",
                                   "value": "0.2500"
                               },
                               "percentage": null
                           },
                           "amountNet": {
                               "currency": "EUR",
                               "value": "0.5000"
                           },
                           "amountVat": {
                               "currency": "EUR",
                               "value": "0.1050"
                           },
                           "amountGross": {
                               "currency": "EUR",
                               "value": "0.6050"
                           }
                       }
                   ]
               }
           }
       },
       "_links": {
           "self": {
               "href": "https://api.mollie.com/v2/settlements/next",
               "type": "application/hal+json"
           },
           "documentation": {
               "href": "https://docs.mollie.com/reference/v2/settlements-api/get-open-settlement",
               "type": "text/html"
           }
       }
   }
