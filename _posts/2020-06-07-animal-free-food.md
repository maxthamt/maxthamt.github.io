---
layout: post
title: Consumption of animal-free products
subtitle: MakeoverMonday Week 23
tags: [MakeoverMonday]
comments: true
---

<iframe title="How often do British people with different food habits consume animal-free products?" aria-label="Split Bars" id="datawrapper-chart-qHw1A" src="https://datawrapper.dwcdn.net/qHw1A/3/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="491"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


The #MakeoverMonday Challenge week 20 involved visualizing auto insurance rate in the US by State. The original viz was a radial chart created by [howmuch.net](https://howmuch.net/articles/car-insurance-rates-in-2020):

![Viz](/assets/img/car-insurance-rates-in-2020.jpg){: .mx-auto.d-block :}


**What works?**
 
* Title and subtitle are short and descriptive.
* Design is visually attractive, related to the topic (circular chart, that resembles a wheel).
* I liked the color palette.
 
**What can be improved?**
 
* I did not get the distinction between full & minimum rate by looking at the chart, I thought it could be clarifying to add the explanation in the chart or as a hover in an interactive version.
* Even though the circle is attractive, it is not as effective to compare between states, especially between states that are far apart in the wheel.
* The full and minimum rates are distinct measures, but the chart gives the impression that they add up. It can be a little confusing.
* My final solution was a dot-plot with the minimum and full rates encoded as circles joined together by a line. States are ordered by their rank number. And I added a map to reinforce the ranking, especially the 3 most expensive states.
* This is my makeover:
