---
layout: post
title: Monitoring is pain!
categories: [Monitoring, Technical]
published: false
---

I am tasked with creating a monitoring platform for an existing SaaS application that is deployed on Azure. I can't help but say that monitoring is a pain somewhere. The amount of available options for monitoring out there is humbling! Here, I try to document my journey, maybe is will be helpful to someone.

## Problem statement:

- We use Azure components for our application
- We use MongoDB Atlas as our database
- Given our compliance policies, we would prefer not to rely on external software. <- I know this might be impossible!!
- Our environments are different from each other, and we only want to monitor our production environment at this point, but you can't get direct access to our production for compliance purposes.
- It will be great if you can use our existing Azure cloud to create this monitoring infrastructure. You're dreaming bro!

## R and hopefully no D 😅:

- One of the tools that has been making a lot of buzz recently is Open Telemetry. I am also familiar with ELK, Prometheus, and Grafana.
- I know that all of the above is not Azure, haha.
- The other direction would be to use [Azure Monitor](https://learn.microsoft.com/en-us/azure/azure-monitor/) which is Microsoft's collection of monitoring solutions. This includes, but not limited to, the infamous App Insights and Log Analytics workspace.

## Game Plan:

- This kinda feels like a matrix of sorts, with monitoring aspects as rows, and resources to be monitored as columns.

- | Monitoring Aspect \ Resource          | MongoDb Atlas | Azure Resources |
  | :------------------------------------ | :-----------: | :-------------: |
  | what are even the monitoring aspects? |        x      |        x        |

- As agreed with the customer, The most important task is to get the MongoDB atlas analytics into Azure. This will be my top priority.
- Next, I will explore how to get monitoring for the rest of the applications that are already stored in Azure into a centralised location.

## Azure Monitor Exploration:
