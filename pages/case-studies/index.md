---
layout: left-menu
title: Case studies
tagline: technical documentation for JDemetra+ using GitHub Pages
description: Basics
---

This document aims to introduce users to the main features of JDemetra+
enabling them to take advantage of this program and understand the
output from consecutive steps of the analysis. The document includes
step-by-step descriptions of how to perform a typical analysis and
useful tips that facilitate replication of the results with user’s own
data and working instructions. The *Case Studies* does not cover
all available JDemetra+ functionalities. They are included in the
[*Reference Manual*](../reference-manual/) and the user should refer to it for
necessary information.

It is assumed that the reader is familiar with concepts, such as *time
series*, *trend-cycle*, *seasonality*, *descriptive statistics*,
*confidence level*, *mean square error*, *estimate*, *estimator*,
*linear regression, stationarity*, *ARIMA process* and so on. Readers
with insufficient background to follow this document are encouraged to
refer to an appropriate textbook, e.g. Chatfield (2004). Some background
knowledge about seasonality in the time series can be gained from the
e-learning courses on Seasonal Adjustment that are available at [<span
class="underline">http://www.sa-elearning.eu/</span>](http://www.sa-elearning.eu/).

JDemetra+ uses the notation "X12", "X13","Arima", "RegArima" and
"TramoSeats" instead of "X-12-ARIMA", "X-13ARIMA-SEATS", "ARIMA",
"RegARIMA" and "TRAMO/SEATS" respectively. This notation is also used in
the *Case Studies* when the references to the user interface are
made.

### Who should use this document? {#who-should-use-this-document}

With JDemetra+, which is an extremely user-friendly software,
pre-adjustment and decomposition of a time series can be performed
easily by users who have absolutely no knowledge of seasonal adjustment
theory. Although the output is easy to produce, its analysis,
interpretation, readjustment and validation requires certain knowledge
and practice. Therefore the *JDemetra+ User Guide* is designed for two
types of users: beginners, who have only a basic knowledge of
seasonality and its estimation in time series, and advanced users, who
already perform seasonal adjustment and are able to interpret the
outcomes, at least on a basic level.

This *Case Studies* neither describes in detail how the seasonal
adjustment methods work, nor the underlying mathematics. For
readers interested in studying seasonal adjustment methods a brief
sketch of the X-13ARIMA-SEATS and TRAMO/SEATS algorithms and concepts
are included in the [*Reference Manual*](../reference-manual/). 
For a detailed discussion of the seasonal adjustment 
related issues the user should refer to the [bibliography](..references/)

### How the document is organized {#how-the-document-is-organized}

The *Case Studies* includes a set of scenarios.They focuses on varous topics, such as:
 - [Simple](../case-studies/modelling-basic.html) and [advanced](../case-studies/modelling-advanced.html) time series modelling
 - [Automatic seasonal adjustment process)(../case-studies/simplesa.html)
 - [Manual setting of the parameters of teh seasonal adjustemnt process](../case-studies/specification.html)
 - [Generating teh output from teh seasonal adjustment procedure](../case-studies/output.html)
 - Options for the [revision policies](../case-studies/revision.html)
 - Setting the (calendars)[../case-studies/calendars-main.html]
 - Tools for (spectral analysis)[../case-studies/spectralanalysis.html] and (spectral graphs)[../case-studies/spectralgraphs.html]
 

### How to use this document {#how-to-use-this-document}

With JDemetra+ seasonal adjustment can be performed in several ways.
Additional functionalities designed for time series analysis, not
necessarily strictly related to seasonal adjustment are also provided.

The *Case Studies* offers several typical paths that can be
followed to perform analyses in an efficient way. These scenarios are
designed to account for different user aims and common constraints, such
as the time allocated to perform the task, the size of the dataset and
the user’s experience and skill in seasonal adjustment. Each scenario
includes consecutive phases of analysis from preparing the source data
to the investigation of the results, readjusting and regular data
production. Therefore it is recommended to study each scenario from
beginning to the end.

The scenarios on seasonal adjustment consist of two simple scenarios 
for beginners and users with limited
time for performing seasonal adjustment and two scenarios of more
detailed seasonal adjustment for more experienced users. The simple and
detailed scenarios both have one example of analysing a single time
series and one example of analysing multiple time series. These
scenarios can be found in section 3.

There are two time series modelling scenarios, one advanced and one
basic that give examples of analysing time series characteristics. The
scenario for advanced users provides a detailed analysis that includes
identification and estimation of outliers[^1], calendar effects[^2],
interpolation of missing values and forecasting. The basic scenario is a
limited version of the advanced analysis, focused mostly on automatic
detection of outliers and calendar effects.

A scenario on seasonality tests is for all types of users and explains
how to test for the presence of seasonal movements in time series. The
presence of seasonality should be checked for each time series in a
dataset. The tests for seasonality are integral to the seasonal
adjustment procedures available in JDemetra+. However, the tests can be
run independently of seasonal adjustment. The scenario on seasonality
tests serves this purpose. As it is designed for analysis of a single
time series, it is usually run for the detailed analysis of the most
important series. For example, it can be used for checking the presence
of seasonal movements to decide if a series should be seasonally
adjusted or for regular monitoring of seasonality in time series.

The spectral graphs scenario is for advanced users and introduces
in-depth analysis of a time series in the frequency domain.

The calendars scenario explains how to define country-specific holidays
and include them into a national calendar. It also deals with the more
sophisticated types of calendar and explains how to import them.