---
date: 2020-01-26T12:30:00+00:00
lastmod: 2020-01-26T12:30:00+00:00
title: Survey Monkey
authors: ["prasanthabr"]
categories: 
  - Salesforce
  - Platform
  - Survey
tags: ["Survey","Salesforce","Platform"]
slug: sf-surveymonkey
draft: true
---

#### _tl;dr_
Setting up a data capture survey with Survey Monkey

List<ApexClass> lapc = [select id,namespaceprefix,name,isvalid,body from apexclass];
pattern myPattern = pattern.compile('(?msi)WebServiceCallout.invoke\\(.+?\\)');
for (ApexClass apx:lapc) {
    String st = apx.body;
    // system.debug(apx.name);
    matcher myMatcher = myPattern.matcher(st);
    if (myMatcher.find()) {
        system.debug('found: class: (' + apx.namespaceprefix + ') [' + apx.name + '] = ' + myMatcher.group().replace('\n',''));    
    }    
}

ref: https://developer.salesforce.com/forums/?id=9062I000000g8KwQAI