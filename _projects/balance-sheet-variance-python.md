---
layout: page
title: Balance Sheet Variance Analysis — Python
description: A month-over-month statistical variance analysis of every balance sheet account, built in pandas and Plotly on the Fake, Inc. general ledger
img: assets/img/variance-analysis-cover.png
importance: 2
category: Python
related_publications: false
---

A single annual Trial Balance tells you where an account started and ended — it can't tell you *when* something moved, or whether that movement was normal for that account. This project rebuilds the full monthly path for every balance sheet account in the **[Fake, Inc.](/projects/fake-inc-excel-company/)** general ledger and statistically flags the months worth asking about.

The question this answers isn't "does the balance sheet balance" — it always should. It's "does every material movement have an explanation I could give an auditor right now."

## How it works

The notebook pulls the same Allocated Transactions and Chart of Accounts data behind the Excel model, builds a running monthly ending balance for every asset, liability, and equity account, computes month-over-month change, and flags any month where an account's movement exceeds 1.5 standard deviations from that account's own typical pattern — not a flat dollar threshold, since a $5,000 swing means something very different for Petty Cash than for Accounts Payable.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/html/balance_sheet_variance_analysis.html' | relative_url }}"
            width="100%" height="900" style="border:none;" loading="lazy">
    </iframe>
  </div>
</div>
<div class="caption">
    The full analysis, code included — every account's monthly balance, the flagged variances, and an interactive chart of Grants Receivable, one of the accounts the analysis correctly flagged.
</div>

## The chart, standalone

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <iframe src="{{ '/assets/plotly/balance_sheet_variance_chart.html' | relative_url }}"
            width="100%" height="520" style="border:none;" loading="lazy">
    </iframe>
  </div>
</div>
<div class="caption">
    Grants Receivable — monthly ending balance, with the flagged month marked.
</div>

## What it found

Fifteen flagged account-months out of 234 total, and every one traces to a real, explainable event: an $18,500 equipment purchase, a $40,000 draw on a note payable, a $70,000 restricted grant recognized mid-year, a $25,000 deferred revenue release. That's the analysis working correctly — catching genuine events, not noise.

## The Potential

The potential for this kind of code is that it can flag when balance sheet accounts change. It can also go backwards, tracing when certain pledges are made, for example, and what can be potentially written off as uncollectible or bad debt. For accountants, this tool can help us trace back liability accounts that may have been building large balances without being properly expensed, or lowered, over time. It's a great tool for catching problems and keeping a clean balance sheet.

## View the code directly

<div class="text-center mt-3">
    <a href="{{ '/assets/jupyter/balance_sheet_variance_analysis.ipynb' | relative_url }}" class="btn btn-outline-primary" role="button">Download the notebook (.ipynb)</a>
</div>

**A note on the data:** this analysis runs on the same fictional dataset as the Fake, Inc. Excel model — every transaction is invented for demonstration purposes.
