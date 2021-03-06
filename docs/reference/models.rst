Models
======

Models hold the bulk of the functionality included in the dj-stripe package.
Each model is tied closely to its corresponding object in the stripe dashboard.
Fields that are not implemented for each model have a short reason behind the decision
in the docstring for each model.

Last Updated 2019-12-21


Core Resources
~~~~~~~~~~~~~~

Balance Transaction
-------------------
.. autoclass:: djstripe.models.BalanceTransaction


.. automethod:: djstripe.models.BalanceTransaction.api_list
.. automethod:: djstripe.models.BalanceTransaction.api_retrieve
.. automethod:: djstripe.models.BalanceTransaction.get_stripe_dashboard_url

.. automethod:: djstripe.models.BalanceTransaction.sync_from_stripe_data

Charge
------
.. autoclass:: djstripe.models.Charge


.. automethod:: djstripe.models.Charge.api_list
.. automethod:: djstripe.models.Charge.api_retrieve
.. automethod:: djstripe.models.Charge.get_stripe_dashboard_url

.. autoattribute:: djstripe.models.Charge.disputed

.. automethod:: djstripe.models.Charge.refund
.. automethod:: djstripe.models.Charge.capture

.. automethod:: djstripe.models.Charge.str_parts
.. automethod:: djstripe.models.Charge.sync_from_stripe_data


Customer
--------
.. autoclass:: djstripe.models.Customer


.. automethod:: djstripe.models.Customer.api_list
.. automethod:: djstripe.models.Customer.api_retrieve
.. automethod:: djstripe.models.Customer.get_stripe_dashboard_url

.. automethod:: djstripe.models.Customer.get_or_create
.. autoattribute:: djstripe.models.Customer.legacy_cards
.. autoattribute:: djstripe.models.Customer.credits
.. autoattribute:: djstripe.models.Customer.customer_payment_methods
.. autoattribute:: djstripe.models.Customer.pending_charges
.. automethod:: djstripe.models.Customer.subscribe
.. automethod:: djstripe.models.Customer.charge
.. automethod:: djstripe.models.Customer.add_invoice_item
.. automethod:: djstripe.models.Customer.add_card
.. automethod:: djstripe.models.Customer.add_payment_method
.. automethod:: djstripe.models.Customer.purge
.. automethod:: djstripe.models.Customer.has_active_subscription
.. automethod:: djstripe.models.Customer.has_any_active_subscription
.. autoattribute:: djstripe.models.Customer.active_subscriptions
.. autoattribute:: djstripe.models.Customer.valid_subscriptions
.. autoattribute:: djstripe.models.Customer.subscription
.. automethod:: djstripe.models.Customer.can_charge
.. automethod:: djstripe.models.Customer.send_invoice
.. automethod:: djstripe.models.Customer.retry_unpaid_invoices
.. automethod:: djstripe.models.Customer.has_valid_source
.. automethod:: djstripe.models.Customer.add_coupon
.. automethod:: djstripe.models.Customer.upcoming_invoice

.. automethod:: djstripe.models.Customer.str_parts
.. automethod:: djstripe.models.Customer.sync_from_stripe_data


Dispute
-------
.. autoclass:: djstripe.models.Dispute


.. automethod:: djstripe.models.Dispute.api_list
.. automethod:: djstripe.models.Dispute.api_retrieve
.. automethod:: djstripe.models.Dispute.get_stripe_dashboard_url

.. automethod:: djstripe.models.Dispute.str_parts
.. automethod:: djstripe.models.Dispute.sync_from_stripe_data


Event
-----
.. autoclass:: djstripe.models.Event


.. automethod:: djstripe.models.Event.api_list
.. automethod:: djstripe.models.Event.api_retrieve

.. automethod:: djstripe.models.Event.process
.. automethod:: djstripe.models.Event.invoke_webhook_handlers
.. autoattribute:: djstripe.models.Event.parts
.. autoattribute:: djstripe.models.Event.category
.. autoattribute:: djstripe.models.Event.verb
.. autoattribute:: djstripe.models.Event.customer

.. automethod:: djstripe.models.Event.str_parts
.. automethod:: djstripe.models.Event.sync_from_stripe_data


File Upload
-----------
.. autoclass:: djstripe.models.FileUpload


.. automethod:: djstripe.models.FileUpload.api_list
.. automethod:: djstripe.models.FileUpload.api_retrieve

.. automethod:: djstripe.models.FileUpload.sync_from_stripe_data


Payout
------
.. autoclass:: djstripe.models.Payout


.. automethod:: djstripe.models.Payout.api_list
.. automethod:: djstripe.models.Payout.api_retrieve
.. automethod:: djstripe.models.Payout.get_stripe_dashboard_url

.. automethod:: djstripe.models.Payout.str_parts
.. automethod:: djstripe.models.Payout.sync_from_stripe_data


PaymentIntent
-------------
.. autoclass:: djstripe.models.PaymentIntent


.. automethod:: djstripe.models.PaymentIntent.api_list
.. automethod:: djstripe.models.PaymentIntent.api_retrieve
.. automethod:: djstripe.models.PaymentIntent.get_stripe_dashboard_url

.. automethod:: djstripe.models.PaymentIntent.str_parts
.. automethod:: djstripe.models.PaymentIntent.sync_from_stripe_data


Product
-------
.. autoclass:: djstripe.models.Product


.. automethod:: djstripe.models.Product.api_list
.. automethod:: djstripe.models.Product.api_retrieve
.. automethod:: djstripe.models.Product.get_stripe_dashboard_url

.. automethod:: djstripe.models.Product.sync_from_stripe_data


Refund
------
.. autoclass:: djstripe.models.Refund


.. automethod:: djstripe.models.Refund.api_list
.. automethod:: djstripe.models.Refund.api_retrieve
.. automethod:: djstripe.models.Refund.get_stripe_dashboard_url

.. automethod:: djstripe.models.Refund.sync_from_stripe_data


Payment Methods
~~~~~~~~~~~~~~~

BankAccount
-----------
.. autoclass:: djstripe.models.BankAccount


.. automethod:: djstripe.models.BankAccount.api_list
.. automethod:: djstripe.models.BankAccount.api_retrieve
.. automethod:: djstripe.models.BankAccount.get_stripe_dashboard_url

.. automethod:: djstripe.models.BankAccount.str_parts
.. automethod:: djstripe.models.BankAccount.sync_from_stripe_data


Card
----
.. autoclass:: djstripe.models.Card


.. automethod:: djstripe.models.Card.api_list
.. automethod:: djstripe.models.Card.api_retrieve
.. automethod:: djstripe.models.Card.get_stripe_dashboard_url

.. automethod:: djstripe.models.Card.remove
.. automethod:: djstripe.models.Card.create_token

.. automethod:: djstripe.models.Card.str_parts
.. automethod:: djstripe.models.Card.sync_from_stripe_data

PaymentMethod
-------------
.. autoclass:: djstripe.models.PaymentMethod


.. automethod:: djstripe.models.PaymentMethod.api_list
.. automethod:: djstripe.models.PaymentMethod.api_retrieve
.. automethod:: djstripe.models.PaymentMethod.get_stripe_dashboard_url

.. automethod:: djstripe.models.PaymentMethod.attach
.. automethod:: djstripe.models.PaymentMethod.detach

.. automethod:: djstripe.models.PaymentMethod.str_parts
.. automethod:: djstripe.models.PaymentMethod.sync_from_stripe_data

Source
------
.. autoclass:: djstripe.models.Source


.. automethod:: djstripe.models.Source.api_list
.. automethod:: djstripe.models.Source.api_retrieve
.. automethod:: djstripe.models.Source.get_stripe_dashboard_url

.. automethod:: djstripe.models.Source.detach

.. automethod:: djstripe.models.Source.str_parts
.. automethod:: djstripe.models.Source.sync_from_stripe_data


Billing
~~~~~~~

Coupon
------
.. autoclass:: djstripe.models.Coupon


.. automethod:: djstripe.models.Coupon.api_list
.. automethod:: djstripe.models.Coupon.api_retrieve
.. automethod:: djstripe.models.Coupon.get_stripe_dashboard_url

.. autoattribute:: djstripe.models.Coupon.human_readable_amount
.. autoattribute:: djstripe.models.Coupon.human_readable

.. automethod:: djstripe.models.Coupon.str_parts
.. automethod:: djstripe.models.Coupon.sync_from_stripe_data


Invoice
-------
.. autoclass:: djstripe.models.Invoice


.. automethod:: djstripe.models.Invoice.api_list
.. automethod:: djstripe.models.Invoice.api_retrieve
.. automethod:: djstripe.models.Invoice.get_stripe_dashboard_url

.. automethod:: djstripe.models.Invoice.upcoming
.. automethod:: djstripe.models.Invoice.retry
.. autoattribute:: djstripe.models.Invoice.plan

.. automethod:: djstripe.models.Invoice.str_parts
.. automethod:: djstripe.models.Invoice.sync_from_stripe_data


InvoiceItem
-----------
.. autoclass:: djstripe.models.InvoiceItem


.. automethod:: djstripe.models.InvoiceItem.api_list
.. automethod:: djstripe.models.InvoiceItem.api_retrieve
.. automethod:: djstripe.models.InvoiceItem.get_stripe_dashboard_url

.. automethod:: djstripe.models.InvoiceItem.sync_from_stripe_data

InvoiceItem
-----------
.. autoclass:: djstripe.models.InvoiceItem


.. automethod:: djstripe.models.InvoiceItem.api_list
.. automethod:: djstripe.models.InvoiceItem.api_retrieve
.. automethod:: djstripe.models.InvoiceItem.get_stripe_dashboard_url

.. automethod:: djstripe.models.InvoiceItem.str_parts
.. automethod:: djstripe.models.InvoiceItem.sync_from_stripe_data


Plan
----
.. autoclass:: djstripe.models.Plan


.. automethod:: djstripe.models.Plan.api_list
.. automethod:: djstripe.models.Plan.api_retrieve
.. automethod:: djstripe.models.Plan.get_stripe_dashboard_url

.. automethod:: djstripe.models.Plan.get_or_create
.. autoattribute:: djstripe.models.Plan.amount_in_cents
.. autoattribute:: djstripe.models.Plan.human_readable_price

.. automethod:: djstripe.models.Plan.str_parts
.. automethod:: djstripe.models.Plan.sync_from_stripe_data


Subscription
------------
.. autoclass:: djstripe.models.Subscription


.. automethod:: djstripe.models.Subscription.api_list
.. automethod:: djstripe.models.Subscription.api_retrieve
.. automethod:: djstripe.models.Subscription.get_stripe_dashboard_url

.. automethod:: djstripe.models.Subscription.update
.. automethod:: djstripe.models.Subscription.extend
.. automethod:: djstripe.models.Subscription.cancel
.. automethod:: djstripe.models.Subscription.reactivate
.. automethod:: djstripe.models.Subscription.is_period_current
.. automethod:: djstripe.models.Subscription.is_status_current
.. automethod:: djstripe.models.Subscription.is_status_temporarily_current
.. automethod:: djstripe.models.Subscription.is_valid

.. automethod:: djstripe.models.Subscription.str_parts
.. automethod:: djstripe.models.Subscription.sync_from_stripe_data


SubscriptionItem
----------------
.. autoclass:: djstripe.models.SubscriptionItem


.. automethod:: djstripe.models.SubscriptionItem.api_list
.. automethod:: djstripe.models.SubscriptionItem.api_retrieve
.. automethod:: djstripe.models.SubscriptionItem.get_stripe_dashboard_url

.. automethod:: djstripe.models.SubscriptionItem.sync_from_stripe_data


TaxRate
-------
.. autoclass:: djstripe.models.TaxRate


.. automethod:: djstripe.models.TaxRate.api_list
.. automethod:: djstripe.models.TaxRate.api_retrieve
.. automethod:: djstripe.models.TaxRate.get_stripe_dashboard_url

.. automethod:: djstripe.models.TaxRate.sync_from_stripe_data


UpcomingInvoice
---------------
.. autoclass:: djstripe.models.UpcomingInvoice


.. automethod:: djstripe.models.UpcomingInvoice.api_list
.. automethod:: djstripe.models.UpcomingInvoice.api_retrieve
.. automethod:: djstripe.models.UpcomingInvoice.get_stripe_dashboard_url

.. autoattribute:: djstripe.models.UpcomingInvoice.invoiceitems

.. automethod:: djstripe.models.UpcomingInvoice.str_parts
.. automethod:: djstripe.models.UpcomingInvoice.sync_from_stripe_data


UsageRecord
-----------
.. autoclass:: djstripe.models.UsageRecord


.. automethod:: djstripe.models.UsageRecord.api_list
.. automethod:: djstripe.models.UsageRecord.api_retrieve
.. automethod:: djstripe.models.UsageRecord.get_stripe_dashboard_url

.. automethod:: djstripe.models.UsageRecord.sync_from_stripe_data


Connect
~~~~~~~

Account
-------
.. autoclass:: djstripe.models.Account


.. automethod:: djstripe.models.Account.api_list
.. automethod:: djstripe.models.Account.api_retrieve
.. automethod:: djstripe.models.Account.get_stripe_dashboard_url

.. automethod:: djstripe.models.Account.get_connected_account_from_token
.. automethod:: djstripe.models.Account.get_default_account

.. automethod:: djstripe.models.Account.str_parts
.. automethod:: djstripe.models.Account.sync_from_stripe_data


Application Fee
---------------
.. autoclass:: djstripe.models.ApplicationFee


.. automethod:: djstripe.models.ApplicationFee.api_list
.. automethod:: djstripe.models.ApplicationFee.api_retrieve
.. automethod:: djstripe.models.ApplicationFee.get_stripe_dashboard_url

.. automethod:: djstripe.models.ApplicationFee.sync_from_stripe_data


Country Spec
------------
.. autoclass:: djstripe.models.CountrySpec


.. automethod:: djstripe.models.CountrySpec.api_list
.. automethod:: djstripe.models.CountrySpec.api_retrieve
.. automethod:: djstripe.models.CountrySpec.get_stripe_dashboard_url

.. automethod:: djstripe.models.CountrySpec.sync_from_stripe_data


Transfer
--------
.. autoclass:: djstripe.models.Transfer


.. automethod:: djstripe.models.Transfer.api_list
.. automethod:: djstripe.models.Transfer.api_retrieve
.. automethod:: djstripe.models.Transfer.get_stripe_dashboard_url

.. automethod:: djstripe.models.Transfer.str_parts
.. automethod:: djstripe.models.Transfer.sync_from_stripe_data


Transfer Reversal
-----------------
.. autoclass:: djstripe.models.TransferReversal


.. automethod:: djstripe.models.TransferReversal.api_list
.. automethod:: djstripe.models.TransferReversal.api_retrieve
.. automethod:: djstripe.models.TransferReversal.get_stripe_dashboard_url

.. automethod:: djstripe.models.TransferReversal.sync_from_stripe_data


Fraud
~~~~~

TODO

Orders
~~~~~~

TODO

Sigma
~~~~~

ScheduledQueryRun
-----------------
.. autoclass:: djstripe.models.ScheduledQueryRun


.. automethod:: djstripe.models.ScheduledQueryRun.api_list
.. automethod:: djstripe.models.ScheduledQueryRun.api_retrieve

.. automethod:: djstripe.models.ScheduledQueryRun.sync_from_stripe_data

Webhooks
~~~~~~~~

WebhookEventTrigger
-------------------
.. autoclass:: djstripe.models.WebhookEventTrigger


.. autoattribute:: djstripe.models.WebhookEventTrigger.json_body
.. autoattribute:: djstripe.models.WebhookEventTrigger.is_test_event
.. automethod:: djstripe.models.WebhookEventTrigger.from_request
