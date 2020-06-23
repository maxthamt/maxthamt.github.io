---
layout: post
title: The best LGBT-themed movies 
subtitle: Viz por Pride Month
tags: 
comments: true
---

# The topic

Before June ended I wanted to create some kind of visualization that would commemorate this LGBT Pride Month.

Several topics came to mind. Some of them were serious subjects -like hate crimes occurring around the world- and others were lighter in tone (I thought about doing a viz of one of my favorite tv shows, RuPaul’s Drag Race).

After thinking it through, I decided to come back to the topic of films that I explored in [my visualization of female directors](https://public.tableau.com/profile/maximiliano4575#!/vizhome/FemaleDirectors/FemaleDirectors). 

In that viz, I showed how really few popular films were directed by women, and I showed how that trend has not changed significantly in the last years. 

With that data-story, I wanted to argue that it is not trivial who directs films because that role has the power to tell the story, the power to portray (or not portray) diverse life experiences. Having a landscape of directors that is so unbalanced according to gender implies that there are experiences and points of view that are not being represented. Groups of people that are not seeing themselves on the screen, who probably don’t relate or identify with the stories that are being showcased in the mainstream film industry. 

Something similar happens when we talk about how LGBT people are represented in cinema and in cultural products in general. A documentary that shows this dimension very well is [“The celluloid closet”](https://www.imdb.com/title/tt0112651/) by Rob Epstein and Jeffrey Friedman, which shows how throughout the 20th century LGBT characters and stories entered the film industry only interstitially, indirectly, and mainly through subtleties.

Today the reality is different. Every year many films that portray LGBT experiences are produced and released around the world. So the goal of my visualization was to highlight those films -those cultural objects- that help the LGBT community (especially teenagers and youth) to find narratives and characters with whom to identify and that help them develop their own biographies.

# The data

For the female directors' project, I analyzed data made available by [IMDB](https://www.imdb.com/). So I tried to start from there. However, the keyword system of the website that classified the films as LGBT-themed did not seem precise or exhaustive (films that did not have LGBT lives at their center had the tag, and other movies that for me were part of the canon did not have the tag).

My next exploration was Wikipedia. There I found [lists of LGBT movies](https://en.wikipedia.org/wiki/List_of_LGBT-related_films_by_year) by decade, which I was able to extract and consolidate using R. With that data I could see how the number of movies that portray LGBT characters or stories has significantly increased in the last 30 years.

<iframe title="Number of LGBT movies 1970-2020" aria-label="Interactive line chart" id="datawrapper-chart-tKFEP" src="https://datawrapper.dwcdn.net/tKFEP/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; max-width: 600 !important; border: none;" height="400"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


This data was promising: I had 2,258 titles, the year of release, the film’s director, country, and genre. However, I had no detail regarding what the movie was about, and collecting that information was going to take a long time. So I left that data for some future exploration.

In the end, I came across a very [comprehensive article on the website Rotten Tomatoes](https://editorial.rottentomatoes.com/guide/best-lgbt-movies-of-all-time/), that featured the 200 best LGBT movies. The list had the hyperlinks to the entry for each film, which allowed me to get their synopsis. With that information I classified each movie into one of five categories, depending on which was the focus or main character of the story (lesbian, gay, bisexual, trans or LGBTQ+ in general).

# The Viz 

I got a first idea on how to visualize the data when I was watching a [Tidy Tuesday live Screencast made by David Robinson](https://www.youtube.com/watch?v=-W-OopvhNPo). There, David made a timeline using ggplot that I liked and thought I could use:

![Viz](/assets/img/reference.png){: .mx-auto.d-block :}

With that idea in mind, I made a very basic sketch. I started with something similar to that timeline, but due to the structure of my data (there can be more than one movie per year) I realized that what I needed was a “bee swarm plot”.

![Viz](/assets/img/sketch.jpg){: .mx-auto.d-block :}

I imagine there must be more elegant ways to do a bee swarm plot, but I followed Ken Flerlage's principle that [everything can be visualized in Tableau if you have an X & Y coordinate](https://www.flerlagetwins.com/2017/11/beyond-show-me-part-1-its-all-about-x-y_46.html).

So with a combination of tools/formats ([RawGraphs](https://rawgraphs.io/) & SVGs) I extracted the X & Y coordinates of the bee swarm plot and added them to my LGBT movie data frame. With that data, I was able to make a first version of the chart in Tableau, and I started to refine the design from that.

![Viz](/assets/img/first-iteration.png){: .mx-auto.d-block :}

For the interactive layer, I wanted to allow the user to get more in-depth information about each point/movie. So I added a tooltip that included the title, year, rank, and score of the movie. 

Along with that basic information, I added an excerpt from the synopsis and the poster of the movie (which I incorporated into the tooltip following [Ryan Sleeper’s tutorial](https://playfairdata.com/how-to-add-an-image-to-a-tableau-tooltip/)).

To convey a visual feeling of Pride Month I looked for inspiration on the web and [found a free font that I loved and that was inspired by the rainbow flag creator, Gilbert Frank](https://www.typewithpride.com/). I used the font for the title and the labels.

After that, I was almost ready. But I wanted to add some text that would not compete so much with the chart. So I added a black column in the left that would give me space to add some written context of the data, explain how to read the chart, and add a quote that I feel sums up nicely why LGBT movies are important to many people's lives.

After several tweaks of aligning elements, adjusting the size, etc. I got to this final product

Any feedback is welcome at [@maxthamt](https://twitter.com/maxthamt)!

<div class="mcb-wrap-inner"><div class="column mcb-column mcb-item-ny8ost4q1 one column_column"><div class="column_attr clearfix" style=""><center><iframe src="https://public.tableau.com/views/pride/lgbt-movies?:showVizHome=no&amp;:embed=true" width="1093" height="819" frameborder="0"></iframe></center></div></div></div>
