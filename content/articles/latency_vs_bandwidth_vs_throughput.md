---
author: "Bryce Fryer"
title: "Latency vs Bandwidth vs Throughput"
date: "2022-12-22"
description: "The differences between latency, bandwidth and throughput."
katex: true
tags: 
- learning
- winter22_challenge
---

# Latency Vs Bandwidth Vs Throughput 

## Before any research

I wrote this section before doing any research. So this is all pre-existing knowledge which may or may not be correct.

* Latency: This is the time it takes from when data is sent to when data is received and acknowledged (if applicable). 
Basically, how long it takes to do a `ping`.
* Bandwidth: This defines how much of something can be going on at once. In computing terms, it could be
the max number of connections supported at once, number of API requests that can be handled simultaneously, etc.
* Throughput: The combination of latency and bandwidth. How many requests can be processed per second.

## After researching

### Latency

Latency measures the time it takes for data to move from point A to point B on a network. Round trip time is the time it
takes for data to go from point A to point B and then back to point A again on a network.

Things that may affect latency:
* Physical distance. The time it takes for data to travel from Seattle to London is going to be longer than the travel 
time between Seattle and Los Angeles.
* Network congestion. If there's an excessive amount of data passing through a network, it can cause delays for 
new data traffic to be delivered. The amount of data that causes a network to be congested is dependent on several
factors.

### Bandwidth

Bandwidth is the data transfer rate of a network. This is commonly seen when looking at what internet speeds to purchase
such as 100 Mbps or 500 Mbps.

### Throughput

Throughput is the amount of data that's been successfully sent per unit of time. In a network, bandwidth can be thought 
of as a theorteical maximum capacity and throughput is the quantity of data that's actually being successfully delivered.

### Real World Comparison

We'll use a water pipe. The water pipe has a diameter which is the bandwidth. This defines the max amount of water that
can flow at any point in ideal conditions. A smaller diameter means there's smaller maximum of water that can be in the
pipe at any given time. The same thing occurs in networks. Less network bandwidth means less data can be "on the network"
at any given time.

The water takes a certain amount of time to go from one end to the other. This is the latency. The longer the pipe, the
longer it takes for the water to travel the length of the pipe. Data does travel extremely quickly through a wire but
it still takes time to go from point A to point B on a wire or network.

The amount of water that has actually been flowing through the pipe over the last hour, day, etc is the throughput. For 
a network, you'd likely measure this as the incoming bits per second or requests per second, depending on the metric you
care about. 

## References

1. https://www.cloudflare.com/learning/performance/glossary/what-is-latency/
2. https://www.ittsystems.com/network-throughput/#wbounce-modal 