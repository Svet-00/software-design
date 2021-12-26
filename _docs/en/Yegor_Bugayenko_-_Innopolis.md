---
layout: article
title: Yegor Bugayenko - Innopolis
permalink: /yegor-bugayenko-innopolis/
key: yegor-bugayenko-innopolis
sidebar:
  nav: docs-en
show_edit_on_github: true
full_width: false
aside:
  toc: true
	
# Default for all pages:
show_edit_on_github: true
full_width: false
mathjax: true
mathjax_autoNumber: true
mermaid: true
chart: true
---

# Intro
Here are notes on [lectures](https://www.youtube.com/playlist?list=PLaIsQH4uc08woJKRAA7mmjs9fU0jeKjjM) from Innopolis by Yegor Bugayenko

# L2 - Requirements

## Use cases
#important #musthave

Use case is a structured description of usage scenarios.

Every flow entry should start with an actor followed by it's action.
Use case should not contain ambigous information. This means no
will/must/would-be-great-if/etc. Only who doing what.

### Example
<mark style="background: #ADCCFFA6;">Blue highlight</mark> - Actor
<mark style="background: #FFB86CA6;">Orange hightlight</mark> - Action

Use case: Make a QR Code
Primary Actor: User
Basic flow:
1. <mark style="background: #ADCCFFA6;">The User</mark> <mark style="background: #FFB86CA6;">enters the URL into the HTML box.</mark>
2. <mark style="background: #ADCCFFA6;">The System</mark> <mark style="background: #FFB86CA6;">creates a PNG image of a QR code.</mark> 
3. <mark style="background: #ADCCFFA6;">The User</mark> <mark style="background: #FFB86CA6;">downloads image through HTTP.</mark> 

Extensions:
	1a. The User enters broken URL.
		1. The System shows an error modal dialog box.
		2. The User confirms.
	3a. The User cancels downloading.
		1. The System stops sending data over HTTP.

## FPA - Function Point Analysis
\[Optional]

COSMIC is the moderd version: ISO/IEC 14143

The method breaks down the requirements into cominations of the four
data movement types: Entry (E), Exit (X), Read (R), Write (W)

Function points are used to estimate.

## Traceability Matrix
\[Optional]

Shows relationship between tests and requirements.
Shows where to look when something changes/breaks. What parts of the
system you need to update when you update something.

## Verification and Validation
#important 

Verification - do we do it right? Assuring that 2 + 2 = 4
Validation - do we still do what we need to do?

First should be done always with automated (and maybe manual) tests.
Latter should be done as frequent as possible when working with customer.

## Non-Functional Requirements
#important 

NFRs should be as exact as possible. Can not be measured = can not be achieved.

### Quality Attributes
Availability: $A = \frac{E_{up}}{E_{down}+E_{up}}$, $E$ = time
Capacity: Clicks Per Second (CPS), Requests Per Second (RPS)
Recovery: Recovery Time Objective (RTO)
Maintainability: Mean Time To Repair (MTTR)

### Example
 Bad NFR:
 The software should be fast.
 Good NFR:
 Being installed on a test server (see Annex A), the software must
 respond in less than 20mss on any request from UC1-UC7.

 