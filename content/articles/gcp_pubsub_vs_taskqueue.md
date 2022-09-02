---
author: "Bryce Fryer"
title: "Google Cloud: Pub/Sub vs Task Queue"
date: "2021-07-14"
description: "Learn the differences between google cloud pub/sub and google cloud task queue (cloud tasks)."
katex: true
tags: 
---

<!-- 
 Goal: Help the reader understand each service individually, and when it is
 good to use either one.

 Audience: relatively junior engineers (less than 2y experience)
 trying to learn about the two similar cloud services
 -->

## Overview

The goal of this post is to help you understand what these services are, when is the right time
to use them, and be aware of other considerations to look at when picking which service to use.

## What are the services?

### Pub/Sub

Service for sending messages to generic receivers. 

### Task Queue

Time based payload that gets sent out to a specific receiver.

## When to use each service?

### Pub/Sub

Event based workloads. No control over how the messages are processed. Best 
for teams that want little coupling.

### Task Queue

When you want to do work at a specific time and to specify who is going to do the work.

## Other considerations

Maybe costs can go here or compatability.

## Alternative services

AWS SQS + SNS