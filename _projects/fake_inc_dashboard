---
layout: page
title: "Financial Dashboard - Power BI"
description: "An interactive Power BI dashboard built on Fake, Inc.'s general ledger, comparing budget to actual by fiscal quarter across cost centers"
img: assets/img/powerbi-cover.png
importance: 3
category: PowerBI
related_publications: false
---

Spreadsheets and notebooks are built for depth. A board or operations meeting needs something different: click a filter, see the picture change, move on. This dashboard is the same Fake, Inc. general ledger data behind the Excel model and the Python variance analysis, rebuilt in Power BI to show that same information the way a board or program lead would actually want to explore it live in a meeting.

## What it shows

A revenue and expense trend line across all cost centers, with a slicer that filters down to Admin, Programs, or any individual cost center. Below that, a budget-versus-actual comparison by fiscal quarter, along with the variance between the two, so it is immediate whether a quarter came in over or under plan and by how much.

Since the underlying fiscal year runs July through June rather than the calendar year, the quarters are calculated to match: Q1 is July through September, Q2 is October through December, Q3 is January through March, and Q4 is April through June.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <video autoplay loop muted playsinline width="100%">
      <source src="{{ '/assets/plotly/powerbi_demo.mp4' | relative_url }}" type="video/mp4">
    </video>
  </div>
</div>
<div class="caption">
    Filtering the slicer between cost centers updates the revenue and expense trend, the budget versus actual comparison, and the variance chart together.
</div>

## How it was built

The report connects directly to the same Allocated Transactions, Chart of Accounts, and Cost Centers data used throughout the Fake, Inc. model, along with the Budget Data used for the comparison. Account Type and Cost Center Type flow through relationships built in Power BI's data model, so a single slicer selection filters every visual on the page at once.

## A note on hosting

Power BI's live, interactive embedding requires a Power BI Pro subscription, which is not included in a standard Microsoft 365 plan. Rather than pay an ongoing fee to keep a single portfolio page live, the video above shows the actual dashboard in use, and the working file is available to open directly in Power BI Desktop, which is free.

## View the file directly

<div class="text-center mt-3">
    <a href="{{ '/assets/jupyter/fake_inc_dashboard.pbix' | relative_url }}" class="btn btn-outline-primary" role="button">Download the Power BI file (.pbix)</a>
</div>

Note: this dashboard runs on the same fictional Fake, Inc. dataset used throughout this portfolio. Every transaction, account, and dollar figure is invented for demonstration purposes.
