---
title: "Ultrasonic WiFi Enabled Volume Detector"
excerpt: "Creating analytics for waste and recycling disposal for sustainable campuses"
sidebar:
  - title: "Role"
    text: "Software and Hardware Developer"
  - title: "Responsibilites"
    text: "Designing and testing circuits to power microcontroller, operate sensors. Software on both device-side and server-side to upload data to Google Sheet."

gallery:
  - url: /images/proj-resources/igen230/test.jpg
    image_path: images/proj-resources/igen230/build.jpg
    alt: "Initial testing"
  - url: /images/proj-resources/igen230/core.jpg
    image_path: images/proj-resources/igen230/core.jpg
    alt: "The two microcontrollers result"

header:
  image: /images/proj-resources/igen230/messy-table.jpg
  teaser: /images/proj-resources/igen230/core.jpg
---


In 2014 I took a 6-credit Integrated Design course at UBC and designed and built a wifi-enabled ultrasonic volume measurement device along with several other students. While they took care of the mechanical design of attaching the device inside a garbage can, I took on the role of developing the electronics and software to power it. 


# The Device

An AT-Mega 328 PU/P chip was loaded with a simple script to pulse an ultrasonic speaker, time the echo then output a distance, accurate to +/- 2cm. This value was relayed to a latch circuit and WiFi enabled controller located above the smaller AT-Mega, which periodically turns on and reads the value of the latch, then transmits it to a browser-friendly Google spreadsheet. Additionally, the AT-Mega operates a set of warning lots on the exterior of the garbage to notify nearby staff whether the can needs to be emptied. 


{% include gallery caption="A few glimpses of the process." %}

# Result

We were awarded 94% on the project, and received enthusiastic feedback from students and staff at the Integrated Engineering Design Showcase. That being said, in hindsight the design could've been simplified greatly by using a single printed PCB board to flatten the profile, in addition I would've liked to experiment with using a single microprocessor to control all functionality, and relay signals via RF to a central base station, which connects to the internet. For my first "hands on" project with microcontrollers and software, I was pretty happy with the result. 