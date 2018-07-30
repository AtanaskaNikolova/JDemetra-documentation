---
layout: left-menu
title: User-defined outliers
tagline: technical documentation for JDemetra+ using GitHub Pages
description: Basics
---

Outliers[^2] are abnormal values of a time series. In general, they
cannot be properly explained by the ARIMA model and its underlying
normality assumption. They tend to be associated with the irregular
special events that produce a distortion on the series. The presence of
such values disturbs the modelling of time series with methods like
X-13ARIMA-SEATS and TRAMO/SEATS because of the linear procedures (e.g.
moving averages and regression analysis) implemented in them. The
presence of outliers has an adverse effect on the quality of seasonal
adjustment because outliers can lead to the model misspecification,
biased parameter estimation, poor forecasts and inappropriate
decomposition of the series. Therefore, it is vital to identify and
include them in the modelling step of seasonal adjustment. The aim is to
remove the effect of outliers from a time series before its
decomposition into the components. Both X-13ARIMA-SEATS and TRAMO/SEATS
include automatic procedure for outliers' treatment (detection and
correction). However, a priori information about an event that may have
caused abnormal observations (the date of its occurrence and type of an
effect) can be included in the model by the user. This case study
explains how to do it.

In the automatic outlier detection and correction procedures, three
outlier types are considered by default:

-   additive outlier (AO) -- an abnormal value in an isolated point of
    the series;

-   transitory change (TC) -- a series of outliers with a temporarily
    decreasing effect on the level of the series;

-   level shift (LS) -- the series of innovation outliers with a
    constant long-term effect on the level of the series, where for an
    innovation outlier is meant an anomalous value in the innovation
    series.

Seasonal outliers, which are defined as an abrupt increase or decrease
of the seasonal component for a specific month or quarter and are of
permanent nature can be automatically detected once the user chose the
appropriate option. The relevant instructions are given in this case
study.

The user may introduce to the model also a ramp effect, which is
described as a smooth, linear transition between two time points unlike
the abrupt change associated with level shifts. This case study explains
how to add the ramp effects into a specification.

The formulas that describe outliers are given in the *JDemetra+
Reference Manual* (2017), item 7.1.

1.  The picture below presents the outflow from the number of registered
    unemployed persons in Poland. It is clear that in the beginning of
    1999 the sudden, permanent shift in the trend level took place as a
    result of a poor condition of the economy. In the end of 2008 a
    single peak can be observed, which can be interpreted as a reaction
    of the entrepreneurs on the beginning of the economic crisis.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image13.jpg)

	{: .text-center.small}
	
	**Time series graph**

2.  To include these events in the model, first create and open a new
    specification as shown in 3.2.1.1.

3.  In the *Regression* section choose a *Pre-defined outliers* item.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image14.jpg)

	{: .text-center.small}

	**Activating a *Pre-specified outliers* option**

4.  In a newly opened window choose the localization (here: 01.1999) and
    an outlier's type. Note that more than one outlier can be assigned
    to the specific period.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image15.jpg)

	{: .text-center.small}

	**An input window for entering a pre-specified outlier**

5.  Enter the relevant information for the next abnormal observation.
    Once all pre-defined outliers are entered, click *Done*.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image16.jpg)

	{: .text-center.small}

	**Confirming the settings for the pre-specified outliers**

6.  Pre-specified outliers are visible in the *Specification* window.
    The localization and type of user-defined outliers are not to be
    verified in the seasonal adjustment process. Click *OK* to confirm
    your choice.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image17.jpg)

	{: .text-center.small}

	**Specification that includes the pre-specified outliers**

7.  Use the newly created specification to perform a seasonal adjustment
    using a *Multi Processing* option (see 3.1.2).

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image18.jpg)

	{: .text-center.small}

	**Choosing a specification**

8.  Go to the pre-processing node and analyse the output. The outliers
    are divided into two parts: pre-specified outliers introduced by the
    user and outliers identified by the software.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image19.jpg)

	{: .text-center.small}

	**Estimation results for the pre-specified outliers**

9.  If some changes are needed (e.g. in the analysed example the
    pre-specified outlier AO (12-2008) is statistically insignificant)
    click on the *Specification* button and modify the settings in the
    *Pre-specified outliers* section.
	
	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image20.jpg)

	{: .text-center.small}

	**Modifying a specification**

10. Automatic identification of the seasonal outliers is performed once
    the user marks the seasonal outlier item in the *Specification*
    window and confirms this choice with the *Apply* button. Detected
    seasonal outliers (if any) are displayed in the pre-processing
    panel.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image21.jpg)

	{: .text-center.small}

	**Launching an automatic identification of seasonal outliers**

11. Alternatively, the user may include identification and estimation of
    the seasonal outliers in the user-defined specification (see
    3.2.1.1) by marking the *Seasonal* option in the *Outliers* section.

12. To include a Ramp effect go to the *Regression* part of the
    specification and click a *Ramp effects* item.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image22.jpg)

	{: .text-center.small}

	**Activating a *ramp* option**

13. In a newly opened window use "+" button to add a ramp effect. Modify
    the default start and end date of the effect. Add more ramps if
    necessary and click *Done*.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image23.jpg)

	{: .text-center.small}

	**Introducing the parameters for a ramp regression variable**

14. Ramps are visible in the *Regression* section. Click *Apply* to
    confirm your input and analyse the output.

	{: .text-center.image-wrapper}

	![Text](/assets/img/user-guide/UG_SA_image24.jpg)

	{: .text-center.small}
	

	**Estimation results for a ramp regression variable**

##### Footnotes

[^2]: Definition of outliers is based on Kaiser, R. and Maravall, A.
    (2003).
