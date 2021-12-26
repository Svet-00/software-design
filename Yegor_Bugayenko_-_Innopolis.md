---
layout: page
title: Yegor Bugayenko - Innopolis
permalink: /yegor-bugayenko-innopolis/
---

# Intro
Here are notes on [lectures](https://www.youtube.com/playlist?list=PLaIsQH4uc08woJKRAA7mmjs9fU0jeKjjM) from Innopolis by Yegor Bugayenko

# L2 - Requirements

## Use cases
### Example
Use case: Make a QR Code
Primary Actor: User
Basic flow:
1. <mark style="background: #ADCCFFA6;">The User</mark> <mark style="background: #FFB86CA6;">enters the URL</mark> into the HTML box.
2. The System creates a PNG image of a QR code.
3. The User downloads image through HTTP.

Extensions:
	1a. The User enters broken URL.
		1. The System shows an error modal dialog box.
		2. The User confirms.
	3a. The User cancels downloading.
		1. The System stops sending data over HTTP.

## FPA - Function Point Analysis
COSMIC is the moderd version: ISO/IEC 14143

The method breaks down the requirements into cominations of the four data movement types: Entry (E), Exit (X), Read (R), Write (W)

Function points are used to estimate.

## Traceability Matrix
Shows relationship between tests and requirements.
Shows where to look when something changes/breaks. What parts of the system you need to update when you update something.

## Verification and Validation
Verification - do we do it right? Assuring that 2 + 2 = 4
Validation - do we still do what we need to do?
## Non-Functional Requirements
### Quality Attributes
Availability: $A = \frac{E_{up}}{E_{down}+E_{up}}$, $E$ = time
Capacity: Clicks Per Second (CPS), Requests Per Second (RPS)
Recovery: Recovery Time Objective (RTO)
Maintainability: Mean Time To Repair (MTTR)

 Bad NFR:
 The software should be fast.
 Good NFR:
 Being installed on a test server (see Annex A), the software must
 respond in less than 20mss on any request from UC1-UC7.

 