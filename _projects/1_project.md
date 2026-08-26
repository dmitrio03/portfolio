---
layout: page
title: Fake, Inc. — A Complete Nonprofit Financial Model
description: A full-year, GAAP-compliant fictional accounting workbook built to demonstrate how I think, reconcile, and communicate as an accountant
img: assets/img/Fake, Inc thumbnail.jpg
importance: 1
category: Excel
related_publications: false
---

Numbers on a page don't tell you much on their own. What tells you something is whether the person behind them can walk into a room — a board meeting, a one-on-one with a CEO, an audit fieldwork session — and make those numbers make sense to everyone at the table, not just the accountants.

This project is a complete, self-consistent set of books for **Fake, Inc.**, a fictional international development nonprofit. Every employee, salary, grant, vendor, and dollar figure is invented — but the mechanics underneath are real: GAAP-compliant depreciation schedules, PTO accrual tied to actual headcount, restricted vs. unrestricted net asset tracking, indirect cost allocation, and a Trial Balance that ties to the penny.

## Cash Flow Forecast

A twelve-month rolling cash forecast built from known recurring expenses and expected revenue — hover over any point for the exact ending balance.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/plotly/cash_forecast_chart.html' | relative_url }}"
            width="100%" height="520" style="border:none;" loading="lazy">
    </iframe>
  </div>
</div>
<div class="caption">
    Ending cash balance by month, FY2026.
</div>

## Variance by Department

Actual spending against approved budget, by month, across all departments — the first thing a board usually wants to see.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/plotly/variance_department_chart.html' | relative_url }}"
            width="100%" height="520" style="border:none;" loading="lazy">
    </iframe>
  </div>
</div>
<div class="caption">
    Total expense, actual vs. budget, all 12 months of FY2026.
</div>

## Variance by Program

The same comparison, viewed by program instead of department — this is where operational decisions live, and where a COO or CEO would want to dig in.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/plotly/variance_program_chart.html' | relative_url }}"
            width="100%" height="520" style="border:none;" loading="lazy">
    </iframe>
  </div>
</div>
<div class="caption">
    Total FY2026 expense by program region.
</div>

## How I'd use this in the room

In a **board meeting**, I'd open on the Cash Flow Forecast and Variance tabs — board members want to know if the organization is going to run out of money, and whether it's spending what it said it would. In a **1:1 with a CEO or COO**, I'd go deeper into Variance by Program, since that's where operational decisions live. With an **auditor**, I'd start at the Trial Balance and walk backward: every balance traces to a schedule, every schedule traces to a documented assumption, and every assumption is labeled as exactly that — an assumption, not a fact dressed up as one.

## Explore the full workbook

This project is best explored directly. Every tab, every formula, every reconciliation is real and functional.

<div class="text-center mt-3">
    <a href="{{ 'assets/Fake, Inc - FY2026.xlsx' | relative_url }}" class="btn btn-outline-primary" role="button">Download the full workbook (.xlsx)</a>
</div>

**A note on the data:** every employee name, salary, grant, vendor, and dollar figure in this workbook is fictional, built for demonstration purposes only.
