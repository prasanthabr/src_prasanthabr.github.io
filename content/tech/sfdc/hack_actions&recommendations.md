---
date: 2020-08-15T06:00:00+06:00
lastmod: 2020-08-15T06:00:00+06:00
title: Extending Actions & Recommendations on Salesforce.com
authors: ["prasanthabr"]
categories: 
  - Salesforce
  - Hack
tags: ["extending","Salesforce","Hacking"]
slug: a_r_salesforce
draft: true
---

## Background  

Recently helped an auto-lease firm implement a framework for their customer experience teams on Salesforce.com.  
There was a need to procvide guided actions for team members based on the nature of the Salesforce.com case. [**Einstien Next Best Action**](https://google.com) with its stategy builder was an excellent fit for this challenge; the only reasons to avoid this was the 5000 recommendations free tier that Salesforce offers you and also since there was not enough complexity in the nature of the cases to warrant system learning and system recommendations.

The actions and recommendations component seemed like a very good fit for the challenge - the following is a high level solution attempted for this business case.