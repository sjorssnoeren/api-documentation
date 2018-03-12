.. _checkout:

Mollie Checkout
===============

Personalize your checkout
-------------------------

It is possible to customize your `Mollie Checkout <https://www.mollie.com/en/features/checkout>`_ by adding your own
brand images. You can upload a logo and a wallpaper. The example below shows a fully branded checkout page.

#. Go to your `Profiles <https://www.mollie.com/dashboard/settings/profiles>`_.
#. Click on a **Personalize Checkout** button.
#. Upload images within the specified restrictions.

.. image:: images/mollie-checkout-example-a@2x.jpg

Benefits of payments via the Mollie Checkout
--------------------------------------------

* The payment screens are suitable for web, smartphones and tablets.

* All payment methods you have enabled are – when relevant – shown to your customers. A newly activated payment method is
  available immediately for all of your visitors.

* If the customer's first choice of payment method is not successful, it's very easy for the customer to select and try
  another one. If a customer appears to not have sufficient credit on a checking account a retry by credit card could
  easily be attempted. We handle this for you without asking you to implement any extra APIs.

* Full support for QR codes and other conversion rate improving features.

* Mollie optimizes the order of payment methods. For Dutch customers we know to list iDEAL at the top while for
  Belgians we start off with the payment method Bancontact. A lot of effort goes into this and we optimize this using
  A/B-testing. This way we improve your conversion without your effort.


Single Click payments for returning customers
---------------------------------------------
Single Click payments increase conversion. This feature allows your customers who have paid with `credit card <https://www.mollie.com/en/payments/credit-card>`_
to complete their next payments with just one click. A recognizable credit card with information gathered from previous
payments is presented securely through unique customer and device detection.

#. Create a unique customer using the Customer API.
#. Store the customer's ``id`` safely in your database. It's needed for performing Customer Payments API calls.
#. Specify the ``customerId`` parameter each time you create a payment for this customer.
#. Returning customers are now shown the credit cards they have used in the past, enabling them to charge their card of
   choice with a single click.

.. image:: images/mollie-checkout-example-b@2x.jpg