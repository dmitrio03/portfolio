---
layout: page
title: "Balance Sheet Variance Analysis - Python"
description: "A month-over-month statistical variance analysis of every balance sheet account, built in pandas and Plotly on the Fake, Inc. general ledger"
img: assets/img/variance-analysis-cover.png
importance: 2
category: Python
related_publications: false
---

A single annual Trial Balance tells you where an account started and ended. It cannot tell you when something moved, or whether that movement was normal for that account. This project rebuilds the full monthly path for every balance sheet account in the Fake, Inc. general ledger and statistically flags the months worth asking about.

The question this answers is not "does the balance sheet balance." It always should. The real question is: does every material movement have an explanation ready before someone asks.

## How it works

The notebook pulls the same Allocated Transactions and Chart of Accounts data behind the Excel model, builds a running monthly ending balance for every asset, liability, and equity account, computes month-over-month change, and flags any month where an account's movement exceeds 1.5 standard deviations from that account's own typical pattern.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/html/balance_sheet_variance_analysis.html' | relative_url }}" width="100%" height="900" style="border:none;" loading="lazy"></iframe>
  </div>
</div>
<div class="caption">
    The full analysis, code included.
</div>

## The chart, standalone

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/plotly/balance_sheet_variance_chart.html' | relative_url }}" width="100%" height="520" style="border:none;" loading="lazy"></iframe>
  </div>
</div>
<div class="caption">
    Grants Receivable, monthly ending balance, with the flagged month marked.
</div>

## What it found

Fifteen flagged account-months out of 234 total, and every one traces to a real, explainable event: an $18,500 equipment purchase, a $40,000 draw on a note payable, a $70,000 restricted grant recognized mid-year, a $25,000 deferred revenue release.

## The potential

This kind of code can flag when balance sheet accounts change unexpectedly. It can also trace backward, checking when certain pledges were made and what might be at risk of becoming uncollectible. For accountants, this tool can help trace liability accounts that may have been building large balances without being properly expensed or reduced over time.

## View the code directly

<div class="text-center mt-3">
    <a href="{{ '/assets/jupyter/balance_sheet_variance_analysis.ipynb' | relative_url }}" class="btn btn-outline-primary" role="button">Download the notebook</a>
</div>

Note: this analysis runs on the same fictional dataset as the Fake, Inc. Excel model. Every transaction is invented for demonstration purposes.
