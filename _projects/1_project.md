---
layout: page
title: Fake, Inc. — A Complete Nonprofit Financial Model
description: A full-year, GAAP-compliant fictional accounting workbook built to demonstrate how I think, reconcile, and communicate as an accountant
img: assets/img/fake-inc-cover.png
importance: 1
category: Excel
related_publications: false
---

Numbers on a page don't tell you much on their own. What tells you something is whether the person behind them can walk into a room — a board meeting, a one-on-one with a CEO, an audit fieldwork session — and make those numbers make sense to everyone at the table, not just the accountants.

This project is a complete, self-consistent set of books for **Fake, Inc.**, a fictional international development nonprofit. Every employee, salary, grant, vendor, and dollar figure is invented — but the mechanics underneath are real: GAAP-compliant depreciation schedules, PTO accrual tied to actual headcount, restricted vs. unrestricted net asset tracking, indirect cost allocation, and a Trial Balance that ties to the penny.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/fake-inc-landing.png" title="Company Overview landing page" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The workbook opens on a plain-language landing page — the story behind the project, how to navigate it, and a tab-by-tab guide written for stakeholders without a finance background.
</div>

## What's inside

Fake, Inc. runs programs in five regions (Latin America, MENA, Sub-Saharan Africa, Europe, and SE Asia) with a small administrative core. Behind the scenes, the workbook tracks a full fiscal year: payroll, revenue recognition, restricted grant accounting, depreciation, PTO accrual, insurance amortization, and indirect cost allocation — all rolling up into a Trial Balance and a GAAP-format Statement of Activities.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/fake-inc-trial-balance.png" title="Trial Balance" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/fake-inc-cash-forecast.png" title="Cash Flow Forecast" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: the Trial Balance, the single source of truth for every account. Right: a twelve-month rolling cash forecast built from known recurring expenses and expected revenue.
</div>

## How I'd use this in the room

In a **board meeting**, I'd open on the Cash Flow Forecast and Variance tabs — board members want to know if the organization is going to run out of money, and whether it's spending what it said it would. In a **1:1 with a CEO or COO**, I'd go deeper into Variance by Program, since that's where operational decisions live. With an **auditor**, I'd start at the Trial Balance and walk backward: every balance traces to a schedule, every schedule traces to a documented assumption, and every assumption is labeled as exactly that — an assumption, not a fact dressed up as one.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/fake-inc-fixed-assets.png" title="Fixed Asset Depreciation Schedule" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/fake-inc-statement-activities.png" title="Statement of Activities" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Every fixed asset traces back to the Trial Balance's Property and Equipment and Accumulated Depreciation balances, down to the dollar — the kind of backup an auditor asks for first.
</div>

## Explore the full workbook

This project is best explored directly. Every tab, every formula, every reconciliation is real and functional.

<div class="text-center mt-3">
    <a href="{{ '/assets/files/Fake-Inc-FY2026.xlsx' | relative_url }}" class="btn btn-outline-primary" role="button">Download the full workbook (.xlsx)</a>
</div>

**A note on the data:** every employee name, salary, grant, vendor, and dollar figure in this workbook is fictional, built for demonstration purposes only.
