---
categories: projects
title: "Statistical Analysis of LEO Satellites"
excerpt: "Visualizing Line of Sight statistics for low earth orbit satellites"
sidebar:
  - title: "Role"
    text: "Researcher"
  - title: "Responsibilites"
    text: "Running orbital simulations in STK, cleaning and analyzing data in MATLAB, and making cool plots."

gallery:
  - url: /images/proj-resources/rsl/stk.jpg
    image_path: images/proj-resources/rsl/stk.jpg
    alt: "Running LEO Simulations"
  - url: /images/proj-resources/rsl/plot2.JPG
    image_path: images/proj-resources/rsl/plot2.JPG
    alt: "Summarizing Statistics for Line of Sight"

header:
  image: /images/proj-resources/rsl/plot1.JPG
  teaser: /images/proj-resources/rsl/plot1.JPG

---

# Modelling LEO Satellites in STK and Analyzing Summary Orbital Statistics

During the academic semesters in 2015 me and David Pownall, a colleague from the Radio Science Laboratory took on an independent research project as a continuation of our work developing a low-cost but accurate ground station, for the establishing of Ka-Band uplinks to LEO satellites. The purpose of this mission was to characterize the rain-fade phenomenon, where atmospheric absorption of microwave frequency signals greatly reduces signal strength, particularly over 11 GHz. 

Most commonly the solution to this problem is to simply up the transmission power, however, this becomes increasingly difficult as communications uplinks move into higher frequency domains. Additionally, satellites are often power and weight-restricted, required a better solution. The RSL aims to characterize the rain-fade effect such that signals can be reconstructed even after attenuation through thick atmosphere.

## Background

Advances in satellite imaging technology have required increases in available bandwidth for data-dumps to ground-stations, increasingly this RF uplink is a bottle-neck in data-acquisition. Space based imaging platforms like the planet hunting [Kepler](https://en.wikipedia.org/wiki/Kepler_(spacecraft)) and the pending [James Webb Telescope](http://www.jwst.nasa.gov/) all utilize Ka-band communications. For example, because of NASA's limited Deep Space Network radar dish capacity, Kepler spacecraft is only able to dump data once per month, at 555 kb/s. Because of this, it must perform some amount of data analysis on-board to conserve bandwidth.

Next-Generation communication systems like the [Iridium Next Project](https://www.iridium.com/network/iridiumnext), and [Immarsat's Global Xpress network](http://www.inmarsat.com/the-i-5-satellites/) also utilize Ka-band communications to handle massive amounts of information across a large number of users. Immarsat's I-5 satellite use 89 Ka-band beams to download up to 50 Mbps from its position in Geosynchronous orbit. 

## The Problem

The potential for Ka-band communication technologies are hampered by atmospheric absorption - since atmospheric penetration is a function of elevation angle, Ka-band satellites suffer greatly when close to the horizon. This motivated our research into conducting a statistical analysis of line-of-sight access parameters, like azimuthal and elevation angles of bearing, range, and relative velocity 

{% include gallery caption="Simulations in STK with results processed in MATLAB" %}

## The Solution

A simulations campaign was conducted using [Systems ToolKit](https://www.agi.com/products/stk/), modeling LEO satellites and line-of-site access across a one year period at 60 second time intervals. Satellites were chosen at 5 altitudes and 10 inclinations to the equatorial plane, with 10 ground stations spaced evenly with latitude at the longitude of Vancouver, British Columbia. STK generated an AER (Access, Elevation and Range) report in csv format describing our simulation results. 

I wrote a package of software in MATLAB to import the raw csv and perform statistical analysis of key observational parameters: distributions of observing time, doppler shift, angular elevation above the horizon, and angular velocity with respect to a tracking satellite dish. The required handling several GB of raw data and organizing it into a tractable problem, which was accomplished by constructing a 3-dimensional space of our input parameters: altitude, elevation above equatorial plane, and latitude of groundstation. Overall there was about 1000 lines of code to import, clean, analyze, and present the data, and some features of MATLAB made the process a lot smoother. 

