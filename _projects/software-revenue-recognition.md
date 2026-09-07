---
layout: page
title: "How Software Revenue Actually Gets Booked - Fake Telemedicine, Inc."
description: "A plain-language walkthrough of ASC 606 revenue recognition, cost-to-cost accounting, and software capitalization for a technology company with both license and grant-funded development revenue"
img: assets/img/software-revenue-cover.jpg
importance: 4
category: Excel
related_publications: false
---

Most people who have never worked in finance assume revenue is simple: a client signs a contract, the company gets paid, that payment is the revenue. For a technology company like Fake Telemedicine, Inc., that assumption is wrong in almost every case, and the gap between "money received" and "revenue earned" is exactly where a lot of financial statements go wrong, and exactly where an accountant earns their keep.

This page walks through how Fake Telemedicine, Inc. actually recognizes revenue across its two very different business lines, why the accounting has to work this way under GAAP, and how the cost of building software flows through the balance sheet before it ever becomes a finished, income-generating asset. None of this is abstract theory. It is built from a real, working dataset, with real dollar figures, that you can see for yourself.

## The two ways this company earns money

Fake Telemedicine, Inc. sells electronic health record software to two very different kinds of customers, and that difference matters enormously for how the accounting works.

**State and county health departments** pay for a **license** to use the platform. This is a subscription-style, hosted arrangement. The customer never owns the software or takes it home; they pay for ongoing access, support, and use, typically over a term of two to five years.

**Foundations** — the Gates Foundation, the Dell Foundation, the Commonwealth Fund, and others in this dataset — pay to fund **new software development**. These are grants that fund the actual building of a specific product: a maternal health registry, an immunization tracking system, a behavioral health data exchange. The foundation is not paying for access to something that already exists. It is paying the company to build something that does not exist yet.

Under the accounting standard that governs all of this, ASC 606, these two situations require two completely different recognition methods, and mixing them up would materially misstate the company's financial position.

## License revenue: recognized over time, straight-line

When a state health department signs a five-year license, the company does not book the entire contract value as revenue the day the contract is signed, and it also does not wait until year five to book anything. Instead, revenue is recognized **ratably, month by month, over the life of the contract**, because the company is providing continuous access and continuous value the entire time the contract is active.

The math is simple in concept: divide the total contract value by the number of months in the term, and recognize that amount every month the contract is in force. If a five-year license is worth $600,000, the company recognizes $10,000 of revenue every single month, regardless of when or how often the customer is actually billed.

That last point is important, because it creates a second, separate question: when does the company actually invoice the customer, and what happens to the gap between what has been billed and what has been earned?

## Why deferred revenue and accrued income exist

Billing and earning almost never happen on the same schedule, and this is the single most misunderstood part of software accounting for people without a finance background.

If a health department pays its entire first year of license fees upfront — a very common government billing practice — the company has now **received cash for work it has not yet fully performed**. Under GAAP, that cash cannot be counted as revenue yet. It sits on the balance sheet as a liability called **Deferred Revenue**, because the company technically owes the customer twelve months of service in exchange for that payment. Each month, as the company actually delivers that access, a portion of the deferred revenue balance converts into real, recognized revenue.

The opposite situation also happens, more often on the development side. If the company has done real, billable work — developers have written code, cloud infrastructure has been used, a milestone has genuinely been achieved — but has not yet sent an invoice for it, that earned-but-unbilled value sits on the balance sheet as an asset called **Accrued Income**. The company has done the work and is owed the money; it just has not gotten around to billing for it yet.

Both of these accounts exist for the same reason: to keep the income statement honest about what was actually earned in a given period, completely separate from the timing of cash changing hands. A company that only tracked cash received would show wildly distorted, lumpy revenue every time a big invoice landed, even in months where very little new work actually happened.

## Development revenue: recognized as work is completed, not as time passes

This is the part of the accounting that is genuinely more complex, and it is where a purely time-based shortcut — dividing a contract by its number of months, the same way license revenue works — would be **the wrong method entirely**, even though it looks similar on the surface.

A grant-funded software development project does not deliver value at a steady, predictable pace the way a hosted subscription does. Some months involve intense design and engineering work; others might be lighter, waiting on a partner's feedback or a compliance review. Recognizing revenue based purely on the calendar would completely disconnect the company's reported earnings from its actual progress. Under ASC 606, work performed "over time" — which most custom software development qualifies as — has to be measured using either an **input method** or an **output method**, and Fake Telemedicine, Inc. uses the input method known as **cost-to-cost**.

The formula looks like this:

**Percent Complete = Costs Incurred to Date ÷ Total Estimated Cost of the Project**

And once percent complete is known:

**Revenue Recognized to Date = Contract Value × Percent Complete**

The entire calculation depends on one thing: knowing, with real accuracy, how much the project has actually cost to build so far. That number does not come from a spreadsheet estimate or a guess. It comes from the same kind of underlying records any accountant would recognize immediately.

## What actually goes into "Costs Incurred"

This is the piece that people with no accounting background almost never think about, and it is the entire foundation the revenue recognition above depends on.

**Time and effort.** Every developer, designer, and engineer working on a specific grant-funded project logs their time against that project. Their hours, multiplied by their fully-loaded cost to the company (salary, benefits, payroll taxes), become a real dollar cost tied to that specific piece of software — not a general company expense, but a cost that belongs to one contract.

**Cloud computing and infrastructure.** Development and testing environments cost real money to run, and a company building several different products at once needs to know how much of its cloud bill belongs to each individual project, not just its infrastructure spending as a whole.

**Vendor and contractor invoices.** If the company brings in a specialized contractor for a piece of the interoperability module, or pays a third-party vendor for a licensed component used in the build, that invoice gets coded to the specific project it supports.

All of these costs accumulate in a holding account on the balance sheet called **Construction in Progress**, the software-industry equivalent of the account a construction company would use to track a building that is not finished yet. As of this dataset's snapshot date, Fake Telemedicine, Inc. has **$2,990,668.44** sitting in this account, spread across twenty-three active development projects at varying stages of completion. None of that has become a finished asset yet. It is money spent, tracked carefully, waiting for the underlying software to be finished.

## When the software is not real work, the accounting falls apart

This is worth stating plainly, because it is the single biggest risk in this whole area of accounting: if a company cannot actually show, with real timesheets, real invoices, and a real cost ledger, how much has been spent on a specific project, it has no defensible basis for claiming any particular percentage of completion. An auditor reviewing this kind of revenue would ask, directly, for the underlying cost detail behind every percent-complete figure on the books. A number that cannot be traced back to real labor hours, real cloud bills, and real vendor invoices is not a number that should be on the financial statements at all. This is exactly why strong, disciplined cost tracking is not a bureaucratic afterthought for a software company. It is the entire legal and financial basis for recognizing a large share of its revenue.

## From Construction in Progress to a real asset

Once a development project reaches 100 percent complete — meaning the accumulated costs incurred equal the total estimated cost of the build — the software is finished and ready to be used commercially. At that point, its full accumulated cost moves out of Construction in Progress and into a new account: **Capitalized Software**.

Six projects in this dataset have reached that point, moving a combined **$1,491,717.09** out of the in-progress account and into a finished, capitalized software asset. This is not a minor bookkeeping shuffle. It represents a real, meaningful shift in what those dollars mean on the balance sheet: they are no longer "money spent building something," they are now "a completed asset the company owns and can generate revenue from going forward," matching the products already generating grant revenue and, in some cases, ready to be offered as a licensable product to future customers.

## Depreciation: how a finished software asset loses value over time

Once software is capitalized, its cost does not sit on the books forever at full value. Like a piece of equipment or a vehicle, it is expected to become less valuable and eventually obsolete as technology moves forward, and GAAP requires that decline to be recognized gradually, not all at once.

Fake Telemedicine, Inc. depreciates (more precisely, amortizes, since this is an intangible asset rather than a physical one) its capitalized software on a **straight-line basis over a five-year useful life**. That means each project's capitalized cost is divided evenly across sixty months, and that same amount is recognized as an expense every single month, starting from the date the software was placed into service.

As of this dataset's snapshot, the six capitalized products have accumulated **$193,947.11** in amortization against their combined $1,491,717.09 in original cost, leaving a **net book value of $1,297,769.98** still on the books. Every month going forward, that net book value declines a little further, and a corresponding amortization expense reduces the company's reported profit, even though no new cash is changing hands. This is one of the clearest examples in all of accounting of a rule that exists specifically to prevent a company's reported profitability from being misleading: the cost of building the software was real and already spent, and GAAP requires that cost to be matched against the revenue it helps generate over its useful life, not dumped entirely into the year it was built.

## Why this requires real collaboration, not just accounting discipline

None of this works if the finance department is operating in isolation. The entire chain — from a signed contract, to logged development hours, to a percent-complete calculation, to recognized revenue, to a fully capitalized asset, to a depreciation schedule — depends on information that lives in at least two other departments entirely.

**Business development** owns the contract information: what was signed, for how much, with what terms, and what the client actually expects to receive. Without accurate, timely contract data flowing from business development into the accounting records, there is no reliable revenue figure to recognize in the first place.

**Software development and engineering** own the ground truth of project progress: how much time has actually been spent, what has genuinely been completed, and — critically — the moment a product is actually finished and ready to be placed into service. If engineering does not clearly communicate when a project has crossed the finish line, the accounting team has no way of knowing when to move a project out of Construction in Progress and start depreciating it, and the company's balance sheet will not reflect economic reality.

This is not a minor administrative detail. A technology company where finance, business development, and engineering do not talk to each other regularly and precisely will, almost inevitably, end up with financial statements that either overstate revenue by recognizing progress that never really happened, or understate it by sitting on completed, valuable assets that never get properly capitalized and put to use in the company's reporting. Strong cross-department collaboration is not a nice-to-have here. It is the mechanism that makes accurate financial statements possible at all.

## What this means for the balance sheet and the bottom line

Pulling all of this together, here is what a reader of Fake Telemedicine, Inc.'s financial statements would actually see, and why each piece matters:

The **balance sheet** shows real assets that represent genuine, tracked investment: money spent on software still being built, sitting separately from money spent on software that is finished and generating value. It also shows real liabilities and near-cash assets, like deferred revenue and accrued income, that keep the timing of cash flow honest and separate from the timing of value actually delivered.

The **income statement** shows revenue that reflects real, earned progress, whether that progress is measured by time elapsed on a license or by actual cost incurred on a development project, alongside a steady, predictable amortization expense that spreads the cost of past software investment across the years that asset will actually be useful.

Together, these choices are what make it possible to look at a single snapshot of the company's finances and trust that the numbers reflect what has actually happened, not just what cash has moved in or out of the bank account. That distinction, more than any other single idea, is the entire purpose of accrual-basis accounting under GAAP, and it is exactly why a technology company building custom software needs disciplined, well-documented cost accounting behind every dollar of revenue it claims to have earned.

**A note on the data:** every contract, dollar figure, and company name in this dataset is fictional, built to demonstrate how these accounting mechanics actually work together in practice.

## Download the full workbook

<div class="text-center mt-3">
    <a href="{{ '/assets/jupyter/contracts_dataset.xlsx' | relative_url }}" class="btn btn-outline-primary" role="button">Download the full workbook (.xlsx)</a>
</div>
