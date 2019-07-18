# Tips for Dashboards using D3, DC.js and Crossfilter.js

So, you want to do a data dashboard for your second milestone, huh?

Well, the bad news is that there's probably a lot of "trial and error" in your near future. The good news is I'm here to provide a little bit of guidance, so you'll hopefully be a little less frustrated than I was for my own project.

Let's get started!

&nbsp;
&nbsp;

## First things first

First of all, go here [Tim's Notes](https://github.com/TravelTimN/ci-ifd-lead/blob/master/week3-d3-dc/d3-dc.md).

Former lead Tim Nelson has already written an excellent introduction to dashboards, so I won't re-invent the wheel here.

&nbsp;
&nbsp;

## Crossfilter Tips

Crossfilter is what enables the filtering across multiple charts. Unfortunately the official documentation is not highly accessible, so here are some tips for using it.

&nbsp;

### Seeing cross-filtered data with print_filter.js

What happens if you try to try to console.log your average crossfiltered data?

&nbsp;
![consolelog](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/consolelogdim.PNG)

The above picture shows an example from my own Code Institute Milestone project, A Dashboard of Ice and Fire. If you want to check it out, you can find a link to it in the resources below.

&nbsp;

This is what this command outputs in the console:

![consolelog-result](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/consolelogresult.PNG)

It's just showing you that it's an object with methods to use on it. Not terribly useful, is it?

&nbsp;

So let's try using the *print_filter* function!

![printfilter](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/printfilter.PNG)

&nbsp;

Using this yields this in your dev tools' console:

![printfilter-result](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/printfilterresult.PNG)

As you can see, this actually allows you to inspect the data that you have loaded into your crossfilter.

&nbsp;

Use print_filter whenever graphs do something you don't expect, to see which data you are working with. You can download the print_filter [HERE](https://gist.github.com/xhinking/9341806).

&nbsp;

### The hidden anatomy of crossfilter commands

&nbsp;

Unfortunately, the course material doesn't really tell us what crossfilter commands are available, and the official documentation does not offer easy visual guidance. So look at the following image for an overview:

![cfcommands](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/commands.PNG)

The picture above shows all the possible crossfilter commands. Note that a *red dot* means the data can be inspected with console.log, and a *blue dot* means it can be looked at with print_filter. Most of these commands have child commands, indicated by a grey dot. You must reach the end point of a command line in order to execute a command correctly.

&nbsp;

For the course, you are most likely going to work mostly with *dimensions*. So here are the crossfilter commands that work specifically on dimensions:

![cfdimcommands](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/cfdimension.PNG)

Note that the groupAll() command returns a single value, while the group() command returns several. These are the subcommands following group():

![cfgroupcommands](https://github.com/synnea/ci-ifd-lead/blob/master/dashboards/images/cfgroup.PNG)

For the meaning and purpose of each commmand, refer to the [crossfilter documentation](https://github.com/square/crossfilter/wiki/API-Reference).

&nbsp;

## Other Resources

&nbsp;

* [reductio.js](https://github.com/crossfilter/reductio) is a crossfilter grouping library that offers help with custom reducers. 

* [Intellipharm dc.js addons](https://github.com/Intellipharm/dc-addons) is a library for dc.js addons. Add tooltips to your charts, or support them in google maps of leaflet.js, along with many more addons. 

* My own Milestone 2 project, with [github code](https://github.com/synnea/GoT-Dashboard) and a link to the deployed website: [A Dashboard of Ice and Fire](https://synnea.github.io/GoT-Dashboard/).




















