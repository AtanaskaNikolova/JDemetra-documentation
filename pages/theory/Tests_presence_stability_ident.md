---
layout: left-menu
title: Test for presence of identifiable seasonality
tagline: technical documentation for JDemetra+ using GitHub Pages
description: Basics
---

This test combines the values of the $F$-statistic of the parametric
test for stable seasonality and the values of the moving seasonality
test, which was described above.

The test statistic is:

  -------------------------------------------------------------------------------------- -----------
  $T = \left( \frac{\frac{7}{F_{S}} + \frac{3F_{M}}{F_{S}}}{2} \right)^{\frac{1}{2}}$,   \[7.152\]
  -------------------------------------------------------------------------------------- -----------

where $F_{S}$ is a stable seasonality test statistic and $F_{M}$ is
moving seasonality test statistic. The test checks if the stable
seasonality is not dominated by moving seasonality. In such a case the
seasonality is regarded as identifiable. This test statistics is used in
the combined seasonality tests (see 7.6.2.6). The detailed description
of the test is available in LOTHIAN, J., and MORRY, M. (1978).