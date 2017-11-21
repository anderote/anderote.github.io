---
categories: projects
---

# Mobile 60 GhZ Indoor Insertion Loss Testing Apparatus and Channel Sounder

During the summer of 2015 I worked as Research Assistant at UBC's [Radio Science Laboratory](http://rsl.ece.ubc.ca/), after winning funding through the [NSERC Research Fellowship](http://www.nserc-crsng.gc.ca/index_eng.asp). The RSL conducts research RF-related research in a broad number of areas related to RF: Satellite Communications, Vehicle-to-Vehicle communications, Channel sounding, and others. As an undergraduate I was able to participate in a number of exciting and challenging projects to help advance the frontiers of RF science. This article describes one such project, using a Vector-Network Analyzer to perform Channel Sounding in the UBC campus. 

## Background Theory

Channel sounding is a technique which measures the transmission characteristics of a radio environment, specifically to analze the [multipath effect](), which describes how a signal is reflected and refracted by objects in urban environments resulting in multiple 'copies' of the same signal arriving from point A to point B at different times. This produces position-dependent variations in signal strength and phase shift. Accurately understanding these effects enables us to better design wireless networks and leverage the multipath effect to drastically increase bandwidth and data transfer speeds in a [MIMO]() system. In a multipath system the wireless channel is frequency dependant, time dependant, and position dependant, therefore the direction of departure, arrival, time delay, and doppler shift are all important parameters to consider when designing MIMO networks. 

<center>
<img src="../../images/proj-resources/rsl/multipath.jpg" alt="Multipath" align="middle">
</center>

*The basic idea behind multipath propagation - differences in path length produce time delays between signals*
{: style="text-align: center;"}

## The Problem

The wave characteristic of light means that reflectance and refraction off objects is a function of the wavelength, smaller waves being less able to penetrate objects than longer wavelengths, but better able to bounce and reflect off objects. Communication modelling tools developed for the design and planning of 3G and 4G/LTE which use 915 MHz and 2GHz respectively can lead to inaccurate predictions when designing high-capacity 5G networks in the 30GHz frequency range. However, higher frequencies have much greater bandwidth for data transfer, and MIMO systems which leverage the multipath to their advantage have become the industry norm in mobile communications devices. 

## The Solution

Accessing higher frequency ranges enables for greater data transmission rates, but to design networks we need to first understand how urban environments behave in this new frequency range. Therefore extensive experimental testing is required to model these environments. Experimentation involves establishing a wireless uplink in an urban setting and taking careful measurements at precisely known intervals.

For the purposes of wireless communication we model light as the finite sum of waves which are assumed to be planar between the receiver and transmitter. Additionally, we assume that the relative bandwidth is small compared to the time delay. With these assumptions the basic signal model is:

<center>
	<img src="../../images/proj-resources/rsl/planar-wave.jpg" alt="Planar wave approximation" align="middle" height="480" width="400">
</center>


*Planar wave model of RF transmission for Channel Modelling, with angles corresponding to the below equation*
{: style="text-align: center;"}

 $$ h( \alpha, \tau, \psi_R, \mu_R, \psi_T, \mu_T) = \sum\limits_{p=1}^{P} \gamma_p \delta(\alpha - \alpha_p) \delta(\tau - \tau_p) \cdot \delta(\psi_R - \psi_{RP}) \delta (\mu_R - \mu_{RP}) \cdot \delta(\psi_T - \psi_{TP})\delta(\mu_T - \mu_{TP})$$ 

Where subscript p is wavefront, R is recevier, T is transmitter; alpha is doppler shift, tau is time-difference of arrival, and psi and mu are azimuthal and elevation angles respectively. At each measurement location the VNA takes a time-slice snapshot of the environment by measuring the s12 tranmission parameters and sampling a generated pulsed signal. The unique features of the signal enable us to precisely reconstruct the relevant time-delays induced by reflection and refraction from the environment. Additionally, we can infer the path waves take through the environment by feeding in information about the location of nearby buildings. We then compare the broadcast to the received signal, and from it deduce what time-delays, shifts in strength, and so forth occured in that specific physical location. 

## The Equipment

Taking spatially resolved snapshots of a radio transmission environment requires a lot of planning and equipment: a known signal must be generated, mixed to a higher frequency, broadcast to a transmitter, received then downconverted into an input port on the same source which generated it. Effectively we make a closed loop of a signal, where one of the steps involves transmitting through an urban environment wirelessly, wherein occurs the multipath effect. In this experiment we used an Agilent equipment to generate and compare the input and output signal, in addition to [Sage Millimeter](http://www.sagemillimeter.com/) hardware to handle, upconvert and downconvert the high-frequency 30 GHz signal. Generating high-power RF signals becomes incredibly difficult as the frequency increases, as conventional electronics start malfunctioning due to the wavelength of electrical signals becoming comparable to the physical dimension of circuit components. As a result, Sage equipment is incredibly expensive, but also high performance and very precise. 

<center>
	<img src="../../images/proj-resources/rsl/bm.png" alt="Block Diagram of VNA Sounder" align="middle">
</center>

*Block Diagram of our experimental setup. All this equipment was mounted on to to sturdy carts, along with custom fixtures for alignment*
{: style="text-align: center;"}

<center>
	<img src="../../images/proj-resources/rsl/vna2.jpg" alt="Appartus in Use" align="middle" height="500" width="300">
</center>

*Transmitter cart in the foreground, receiver in the background*
{: style="text-align: center;"}

In our experiment, we used a long length of fiber-optic cable to transmit a reference signal of 10MHz to synchronize the receiver and transmitter portions of the uplink. This proved to cause us some head-aches: what we initially thought of as a system malfunction was actually an intermodulated  product between this reference signal and our test signal. Luckily we caught the error and added some adjustable attenuators to reduce the strength of the 10 MHz. 

## The Process

Experimental procedure consisted of establishing a measurement track in an urban environment, mapping nearby buildings with a laser rangefinder, then stepping the VNA receiver cart along the measurement track. At each interval the Receiver directional horn would step through 5 degree increments of a full 360 sweep, through a computer controlled azimuthal motor. The transmission parameters at each angle were recorded and then processed in MATLAB to reconstruct the Angle of Arrival dependence of the radio environment. It was necessary to ensure precise alignment of the transmitter antenna and receiver horn in terms of elevation angle and height - misalignments would throw off assumptions behind the model, and reduce the accuracy of our findings. 

<img src="../../images/proj-resources/rsl/channel-sounding2.jpg" alt="Channel Sounder" align="middle">

## The Result and Followup

Over the course of several weeks in the summer, myself and 2 other undergraduates at UBC collected reams of high quality Channel-Sounding data. Additionally, with very little modifications we transformed the VNA Channel-Sounder into an Indoor Insertion Loss experiment, which looks at the RF transmission characteristics of interior building materials. Overall the project was a success, and through the process we learned a lot about how to design, assemble, and operate a measurement campaign in Channel Modelling. 

The very next year, Radio Science Laboratory replaced the Channel Sounding team with a laser-calibrated and GPS guided robot pictured below. Onwards, march of science!

<center>
	<img src="../../images/proj-resources/rsl/robot.jpg" alt="Channel Sounder" align="middle" height="700">
</center>