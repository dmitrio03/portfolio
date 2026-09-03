---
layout: page
title: "Financial Dashboard - Power BI"
description: "An interactive Power BI dashboard built on Fake, Inc.'s general ledger, comparing budget to actual by fiscal quarter across cost centers"
img: "assets/img/Fake, Inc dashboard thumbnail.jpg"
importance: 3
category: PowerBI
related_publications: false
---

I find myself often wanting to share something broadly--I want anyone to be able to open the thing I make and intuitively understand it. Spreadsheets can do that, because everyone has Excel, but the notebook is built for depth. Non-financial people need to be able to click a filter, see the picture change, isolate certain costs, and get what's happening. 

Hence the need for Power BI. This program comes with standard Microsoft packages, so most employees will be able to open up a file and see the visualizations. I built a simple dashboard with the same Fake, Inc. general ledger data behind the Excel model and the Python analysis.

## What it shows

A revenue and expense trend line across all cost centers, with a slicer that filters down to Admin, Programs, or any individual cost center. Below that, a budget-versus-actual comparison by fiscal quarter, along with the variance between the two, so it is immediate whether a quarter came in over or under budget and by how much. This is much more extensive than an Excel chart, which is not interactive. If something like this were built in Excel, it would take the place of 12 different charts: across all cost centers + the programs and administrative departments.

Since the fiscal year runs July through June rather than the calendar year, the quarters are calculated to match: Q1 is July through September, Q2 is October through December, Q3 is January through March, and Q4 is April through June.

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

The report connects directly to the same general ledger transactions from the Fake, Inc. model, along with the Budget Data used for the comparison. Relationships were made to connect all disparate data with key columns.

## View the file directly

<div class="text-center mt-3">
    <a href="{{ '/assets/jupyter/fake_inc_dashboard.pbix' | relative_url }}" class="btn btn-outline-primary" role="button">Download the Power BI file (.pbix)</a>
</div>

Note: this dashboard runs on the same fictional Fake, Inc. dataset used throughout this portfolio. Every transaction, account, and dollar figure is invented for demonstration purposes.
