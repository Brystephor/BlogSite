---
author: "Bryce Fryer"
title: "What are Real Time Payments?"
date: "2021-07-14"
description: "An overview of real time payments and the network they're on."
katex: false
tags: 
- payments
- RTP
- real time payments
---


# What are Real Time Payments?

The TLDR is that A real time payment is a payment that is made to a bank account via the RTP network. These are bank to bank transactions that happen instantly and are available nearly 24/7. This is very different from standard ACH transactions which take 3-5 business days for the money to arrive in your bank account.

## How fast is instant?

Surprise! Instant actually isn't always instant. As stated by the RTP operating rules in the *Receiving Participants Obligations section A* there is a timeframe that the receiving participant must respond within. The actual timeframe though is unclear.

A real time payment can also be "accepted without posting" meaning the receiving participant could not decide whether or not to process or reject the payment in time. A payment that is accepted without posting is expected to make a decision by 11:59pm local time the next **business** day, unless the payment review is related to sanctions compliance. A payment can be accepted without posting in two situations.

1. when there are additional legal and/or compliance checks that need to be done.
2. The payment is made because of a participants request for return AND the designated account is now closed.
    1. Note: a request for return is different than a new payment that is made to return money. Payments made to closed accounts will be rejected.

## Can real time payments really be made 24/7?

The RTP network is available 24/7. The network mandates that banks are available on the RTP network 99% of the time. Which means they can have up to ~7.3 hours of **unscheduled** downtime each month. In addition to this banks are allocated a maintnenace window from 2am - 6am EST every sunday. Downtime during this 4 hour maintenance window is not counted towards the 99% availability requirement. 

So yes you can always initiate a real time payment, but there is no requirement that the bank you're sending money to must be available 24/7/365. Sending a payment to a bank that is signed off the RTP network results in a rejected payment, meaning there was no transfer of funds.

## What are some limitations of a real time payment?

* A single transaction may not exceed $1 million USD. If you need to pay more than $1MM USD, then you can break it up into multiple transactions and create them back to back. 
    * For example: Let's say you owe someone $2.3MM USD. Then you can create 3 payments. Two payments for $1MM USD, and a final payment for $300k USD. 
* You cannot reduce the size of a payment to collect transaction fees. This means that if you provide a service that transfers money via the RTP network and it costs the user X% of the transaction to initiate, then you cannot simply reduce the size of the payment by X% and send it to your own account. This is known as "fee netting". 
    * For example: You provide a peer to peer payment service that uses the RTP network to provide instant money transfers. This costs someone 2% of the transaction to use. Fred initiates a payment to Joe for $100. You cannot simply initiate a payment to Joe for $98 with the remaining $2 going to your own account.
* Foreign payments are prohibited. The actual definition of this is hard to understand entirely. You can read more about it here: [RTP Operating Rules. 08-25-22](https://www.theclearinghouse.org/-/media/new/tch/documents/payment-systems/rtp_operating_rules_effective_08-25-2022.pdf) under General Participant Responsibilites section E. You can find additional details about this in the [TCH RTP Fee Netting rule interpretation](https://www.theclearinghouse.org/-/media/new/tch/documents/payment-systems/rules_interpretation_no_fee_netting_and_returned_funds_f.pdf) document.

# FAQ

## What are some benefits of real time payments?

1. The transfer of money occurs within seconds of initiation
2. Money can be transferred at anytime.
3. Improved cash flow. No more waiting 3-5 business days to see if a payment will or will not succeed. 

## How can I use real time payments directly?

As an individual you cannot directly connect to the real time payment network. I'm not aware of any API's that're offered to independent developers for real time payments (without the companies own layering on top of it).

Otherwise, you can connect to a third party service provider. This would likely be a big bank. The clearing house is owned by a group of banks, all of which are likely to have access to the RTP network and could be willing to provide you access to their own API.

## I have more questions. Where can I go?

The best source for questions related to RTP is the TCH support email which can be found on their website: https://www.theclearinghouse.org/about/contact