---
layout: left-menu
title: Statistical methods
tagline: technical documentation for JDemetra+ using GitHub Pages
description: Basics
category: Application menu
order: 2
---

The Statistical methods menu includes functionalities for modelling, analysis and seasonal ad-justment of a time series. They are divided into three groups:
* **Anomaly Detection** – allows for a purely automatic identification of regression effects;
* **Modelling** – enables time series modelling using the TRAMO and RegARIMA models; 
* **Seasonal adjustment** – intended for seasonal adjustment of the time series with the TRAMO/SEATS and X-13ARIMA-SEATS methods. 

{: .text-center}
![Text](/assets/img/reference-manual/manual/Statistical methods menu.jpg)

### Anomaly Detection {#anomaly-detection}

The primary goal of functionalities that are available in the *Anomaly
Detection* section is an identification of atypical values called
outliers. According to the ‘*ESS Guidelines on Seasonal Adjustment*’
(2015), seasonal adjustment methods are likely to be severely affected
by the presence of such values; therefore they should be detected and
replaced simultaneously or before estimating the seasonal and calendar
components in order to avoid a distorted or biased estimation.

The use of the RegARIMA models is recommended by the ‘*ESS Guidelines on
Seasonal Adjustment*’ (2015) to estimate and remove outliers before
estimating the seasonal effect. As the presence of outliers could
strongly affect the quality of the decomposition, the various types of
outlier (i.e. additive outliers, transitory changes, level shifts, etc.)
should be detected and corrected for.

The quality control should be performed each time new or revised data
become available. The manual inspection of the data is problematic,
especially in the case of large databases. Moreover, it usually relies
on some simple measures, which do not consider the full information
contained in the series, but just a few values. Therefore the results
can be strongly affected by seasonality, noise, or special events.

JDemetra+ includes two tools dedicated for automatic identification of
outliers: *Check Last* and *Outliers Detection*. Both are based on the
TERROR program, which is an application of TRAMO, executed in an
automatic manner (with several possible options to set) to the problem
of quality control in time series for automatic detection of errors in
time series. Therefore, both tools use the TRAMO specifications.


{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref13.jpg)

The *Anomaly detection* menu.

#### Check Last {#check-last}

The *Check Last* tool automatically detects the TRAMO model, forecasts
up to three last observations and marks the observations that are too
different from their forecasted values. The *Check Last* *Batch* window
is divided into three panels. The panel on the left presents the list of
analysed series. The results are dispalyed in the panels on the right.

To launch the analysis, drag and drop the series from the *Providers*
window into the left hand side panel of the *Check Last Batch* window
and click the *Start* button (denoted with the green arrow) from the
menu in the top part of the window. The analysis will be performed using
the TRAMO speciation selected from the list. By default, TR4 is used.

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref14.jpg)

The *Check Last* initial window with series to be processed
and the list of available specifications expanded.

JDemetra+ removes the last observations from the series and calculates a
one-period-ahead out-of-sample forecast of the series. The forercasted
values are then compared with the actual values. The user may decide how
many of the last observations will be considered (one, two, or three) in
this procedure (click on the *123* button and specify the number). The
number of columns visible in the panel on the left is adjusted
accordingly to the user choice.

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref15.jpg)

The options for number of observations to be examined.

The default settings can be changed in the *Properties* dialog box (the
number of last observations that will be compared to the forecasted
values, specification used for modelling and the threshold values used
to decide if observation is abnormal). To open it, click on the button
marked with the working tools.

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref16.jpg)

The properties for the *Check Last* functionality.

Once the process is executed, click on the series on the list to display
the results. For each series the program automatically identifies an
ARIMA model, detects several types of outliers, interpolates missing
values and estimates the calendar effects, if appropriate. Study the
detailed results section using the vertical scrollbar.

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref17.jpg)

The results of the outlier’s detection process.

The last observations (one, two or three, depending of the user’s
choice) are compared with the forecasted values. If, for a given
observation, the forecast error divided by a standard deviation of
residuals is greater than the first threshold value and lower than the
second threshold value, then this observation is classified as
containing a "possible error" and marked in orange. If this value is
greater than the second threshold value, then the new observation is
classified as containing a "likely error" and marked in red. Otherwise,
the observation is accepted as without error[^12].

: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref18.jpg)

Investigation of the outliers’ detection results.

JDemetra+ enables the user to save the results of this analysis in the
compact form of the report. To generate it, click on the **Generate
Report** button and specify the sorting options.

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref19.jpg)

Figure 3.19: The *Generate Report* functionality.

To save the report click **OK** and select a destination folder.
{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref20.jpg)


Report from the outliers’ detection process.

#### Outlier detection {#outlier-detection}

The *Outlier Detection* tool allows for an identification of an ARIMA
model, including detection of outliers, interpolation of missing values
and estimation of calendar effects. The assessment of the last
observations’ quality is not performed. Instead, the outliers are
highlighted in green (transitory changes), red (level shifts), blue
(additive outliers) and violet (seasonal outliers). By default the
seasonal outliers are not considered. The user may change this setting
in the *Properties* menu.

A step-by-step demonstration of the *Outlier Detection* tool
capabilities can be found in the ‘*JDemetra+ User Guide*’ (2017), item
3.3.1.

### Modelling {#modelling}

The aim of the *Modelling* section is to provide tools for time series
modelling and forecasting without performing the estimation of the
components and decomposition. The estimation results can be useful for
time series analysis and prediction of a short-term development.

The *Modelling* section includes all capabilities from the TRAMO and
RegARIMA models. It is flexible in specifying model parameters. The
results can be saved and refreshed with updated series. Instructions on
how to use this functionality is given in the ‘*JDemetra+ User Guide*’
(2017), item 3.3.2.

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref21.jpg)

 The *Modelling* menu.

### Seasonal Adjustment {#seasonal-adjustment}

The *Seasonal Adjustment* section provides tools to perform seasonal
adjustment for a single time series as well as for the multiple time
series using the TRAMO/SEATS or X-13ARIMA-SEATS methods. It also offers
several seasonality tests that can be used to scrutinize the presence
and the nature of seasonal movements in time series independently from
seasonal adjustment. Finally, the *Direct-Indirect Seasonal Adjustment*
tool enables for a comparison of the results from direct and indirect
seasonal adjustment performed for the aggregated series.

The guidance for using these functionalities is given in the ‘*JDemetra+
User Guide*’ (2017) (basic scenario that allows for generating seasonal
adjustment in an automatic way is presented in 3.1, different types of
user interventions are discussed in 3.2, the *Seasonality Tests* tool is
explained in 3.4.1 while the capabilities of *Direct-Indirect Seasonal
Adjustment* are shown in 3.2.1.8).

{: .text-center}

![Text](/assets/img/reference-manual/manual/A_Ref22.jpg)

The *Seasonal Adjustment* menu.