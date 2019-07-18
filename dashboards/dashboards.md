# Tips for Dashboards using D3, DC.js and Crossfilter.js

So, you want to do a data dashboard for your second milestone, huh?

Well, the bad news is that there's probably a lot of "trial and error" in your near future. The good news is I'm here to provide a little bit of guidance, so you'll hopefully be a little less frustrated than I was for my own project.

Let's get started!



## First things first

First of all, go here [Tim's Notes](https://github.com/TravelTimN/ci-ifd-lead/blob/master/week3-d3-dc/d3-dc.md).

Former lead Tim Nelson has already written an excellent introduction to dashboards, so I won't re-invent the wheel here.



## Crossfilter Tips

Crossfilter is what enables the filtering across multiple charts. Unfortunately the official documentation is not highly accessible, so here are some tips for using it.


### Seeing cross-filtered data with print_filter.js

What happens if you try to console.log crossfiltered data?

![consolelog](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/consolelogdim.PNG)

The above picture shows an example from my own Code Institute Milestone project, A Dashboard of Ice and Fire. If you want to check it out, you can find a link to it in the resources below.

This is what this command outputs in the console:

![consolelog-result](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/consolelogresult.PNG)

It's just showing you that it's an object with methods to use on it. Not terribly useful, is it?

So let's try using the *print_filter* function!

![printfilter](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/printfilter.PNG)

Using this yields this in your dev tools' console:

![printfilter-result](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/printfilterresult.PNG)

As you can see, this actually allows you to inspect the data that you have loaded into your crossfilter.

Use print_filter whenever graphs do something you don't expect, to see which data you are working with. 















