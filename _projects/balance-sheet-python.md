---
layout: page
title: "Balance Sheet Variance Analysis - Python"
description: "A month-over-month statistical variance analysis of every balance sheet account, built in pandas and Plotly on the Fake, Inc. general ledger"
img: assets/img/variance-analysis-cover.png
importance: 2
category: Python
related_publications: false
---

If you're looking at a company's trial balance for the year, it can tell you where an account started and ended. It cannot tell you when something moved, or where exactly the account fell or jumped in value. The way accountants have typically solved this is by running monthly balance sheets, saving the files in Excel, then pulling the files up one after the other to find the movement in value. It's not a great use of time, and we spend a lot of that time thinking "there has to be a better way." Well, there is. This project rebuilds the full monthly path for every balance sheet account in the Fake, Inc. general ledger and statistically flags the months worth asking about.

To be clear: the question this answers is not "does the balance sheet balance." It always should. The real question is, "does every material movement have an explanation?"

## How it works

The notebook pulls the same general ledger transactions and Chart of Accounts data behind the Excel model, builds a running monthly ending balance for every asset, liability, and equity account, computes month-over-month change, and flags any month where an account's movement exceeds 1.5 standard deviations from that account's own typical pattern.

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

Fifteen flagged account-months out of 234 total (all balance sheet accounts * 12), and every one traces to a real, explainable event: an $18,500 equipment purchase, a $40,000 draw on a note payable, a $70,000 restricted grant recognized mid-year, a $25,000 deferred revenue release. These all make great footnotes for the balance sheet at year-end, since these jumps in value count as anomalies. Board members and executives should know why these are here.

## The potential

This kind of code flags when balance sheet accounts change unexpectedly. It could also be used to trace the accounts backwards, checking when certain transactions were made in prior fiscal years. For example: a pledge for a donation more than five years back--which might be at risk of being uncollectible. For accountants, this tool can also help trace liability accounts that may have been building large balances without being properly expensed or reduced over time.

## View the code directly

<div class="text-center mt-3">
    <a href="{{ '/assets/jupyter/balance_sheet_variance_analysis.ipynb.txt' | relative_url }}" class="btn btn-outline-primary" role="button">Download the notebook</a>
</div>

Note: this analysis runs on the same fictional dataset as the Fake, Inc. Excel model. Every transaction is invented for demonstration purposes.
