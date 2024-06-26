=============
Multi-company
=============

.. |mcd| replace:: multi-company database

In Odoo, multiple companies can exist within a single database. This allows for some data to be
shared among companies, while still maintaining some level of separation between entities.

Before deciding to use the multi-company feature, there are several factors to consider.

.. important::
   Multi-company is **only** available in One-app free databases, or with
   `Custom <https://www.odoo.com/pricing-plan>`_ plans.

Sharing data
============

In a |mcd|, certain records are able to be utilized by all of the companies (or several, based on
permissions).

Products
--------

In an |mcd|, new products are created with the :guilabel:`Company` field blank, by default. This
enables
:ref:`company field <general/active-companies>`

Contacts
--------

Inter-company transactions
--------------------------

The :ref:`Inter-Company Transactions <general/inter-company>` feature allows for one company in the
database to sell or purchase goods and services from another company within the same database.
Counterpart documents for orders and invoices can be automatically generated and synchronized,
depending on the configuration settings.

Accessing multiple companies
============================

The list of companies an employee :ref:`has access <general/employee-access>` to in a |mcd| can be
found at the top-right of the main Odoo menu bar, where the active company is listed. Click on the
company name to reveal a list of all allowed companies. To switch to a different company, click on
the company name. To enable multiple companies at once, tick the checkbox next to each applicable
company name.

.. note::
   The database may refresh after each checkbox is ticked.

.. _general/active-companies:

Multiple active companies
-------------------------

If more than one company is active at a time, one company is highlighted in purple, and is listed on
the menu bar. This is the considered the *current* company.

When creating a new record, the *current* company is added to the record in the :guilabel:`Company`
field, except under the following circumstances:

- The :guilabel:`Company` field for a new product or a new contact is left blank.
- If there is a related document already in the system, the :guilabel:`Company` field on the new
  record defaults to the same company.

.. example::
   Mitchell Admin has multiple companies enabled, but the active company is `My Company (Chicago)`.
   When he creates a new product record, the :guilabel:`Company` field is left blank by default.

   When he creates a new sales team, the :guilabel:`Company` field automatically defaults to `My
   Company (Chicago)`.

