# REDCap Automated Billing

## Overview

REDCap Automated Billing is an automated, data-driven service billing system for a REDCap system. The University of Florida’s CTS-IT designed and wrote this system to charge a modest annual fee for each project and bill for customer support work logged in a REDCap-based service request system. This generates revenue, reduces data privacy risks by incentivizing the deletion of abandoned projects, and improves the quality of research productivity metrics.

## Motivation
- Generate revenue to offset costs and improve service.
- Reduce data exposure risk via deletion of unneeded things.
- Improve the quality of metrics by not counting junk projects.
- Reduce support staff workload.

## What we learned
- We can make money by charging for REDCap services.
- Charges are a tool to incentivize customer behavior.
- Good people data and project ownership data are required.
- There is no such thing as over-communication.
- Partner with your fiscal team.
- Use an incremental and iterative approach.
- Automate everything.

## Novel Concepts

REDCap Automated Billing introduces some concepts outside the normal scope of a REDCap system. These are described in [Novel Concepts](https://ctsit.github.io/rcc.billing/articles/novel_concepts.html)

## Billing for support work

The complexities of billing for REDCap support work are described in [Billing for REDCap support work](https://ctsit.github.io/rcc.billing/articles/billing_for_support.html)

## Business workflows
- Cleaning person data
  - [cleanup_bad_email_addresses](https://ctsit.github.io/rcc.billing/articles/cleanup_bad_email_addresses.html)
  - [cleanup_bad_project_pi_email_addresses](https://ctsit.github.io/rcc.billing/articles/cleanup_bad_project_pi_email_addresses.html)
  
- Cleaning ownership data
  - [cleanup_project_ownership_table](https://ctsit.github.io/rcc.billing/articles/cleanup_project_ownership_table.html)
  - Ban accounts/emails of people who left your institution. See  [update_invoice_line_items_with_invoicing_details](https://ctsit.github.io/rcc.billing/articles/update_invoice_line_items_with_invoicing_details.html)


- Exempt special people and special projects from billing
  - [update_project_billable_attribute](https://ctsit.github.io/rcc.billing/articles/update_project_billable_attribute.html)  


- Manage abandoned projects
  - [delete_abandoned_projects](https://ctsit.github.io/rcc.billing/articles/delete_abandoned_projects.html)
  - [sequester_orphans](https://ctsit.github.io/rcc.billing/articles/sequester_orphans.html)

- Create & Manage charging records
  - [create_and_send_new_invoice_line_items](https://ctsit.github.io/rcc.billing/articles/create_and_send_new_invoice_line_items.html)
  - [update_invoice_line_items_with_invoicing_details](https://ctsit.github.io/rcc.billing/articles/update_invoice_line_items_with_invoicing_details.html)
  - [sequester_unpaid_projects](https://ctsit.github.io/rcc.billing/articles/sequester_unpaid_projects.html)
  - cancel_invoice_line_items (Ad hoc)

- Manage organizational data
  - write_uf_fiscal_orgs_to_org_hierarchies (temporarily disabled)
  - write_uf_fiscal_orgs_to_person_org (temporarily disabled)

- Manage pro bono service request work
  - [update_free_support_time_remaining](https://ctsit.github.io/rcc.billing/articles/update_free_support_time_remaining.html)
  - [update_probono_service_request_records](https://ctsit.github.io/rcc.billing/articles/update_probono_service_request_records.html)

- Internal reporting
  - [billable_candidates](https://ctsit.github.io/rcc.billing/articles/billable_candidates.html)
  - [revenue_status_and_projections](https://ctsit.github.io/rcc.billing/articles/revenue_status_and_projections.html)

- Manage customer communications
  - [remind_owners_to_review_ownership](https://ctsit.github.io/rcc.billing/articles/remind_owners_to_review_ownership.html)
  - [request_correction_of_bad_ownership_data](https://ctsit.github.io/rcc.billing/articles/request_correction_of_bad_ownership_data.html)
  - [warn_owners_of_impending_bill](https://ctsit.github.io/rcc.billing/articles/warn_owners_of_impending_bill.html)


## When jobs run

Most ETLs and reports are run in a regular basis via Cron. The schedule of those events can be found at [When jobs run](https://ctsit.github.io/rcc.billing/articles/when_jobs_run.html)
