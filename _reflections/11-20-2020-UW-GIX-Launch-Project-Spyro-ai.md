---
title: "Spyro.ai"
layout: "single"
classes: "wide"
---
## Background
**Spyro.ai** is a respiratory monitoring system built to increase asthma patient compliance; help doctors make more data-driven decisions and to provide a communication channel between patients and doctors. 

This project has proposed and developed as Launch project for the [MSTI](https://gixnetwork.org/program/msti/) program at the University of Washington. The Launch is a two-quarter project, a mandatory part of MSTI, to help students gain industry experience and leadership skills while pursuing graduate studies.

## Ideation / Defining the Problem

Asthma is one of the most common respiratory illness, apart from one of the major cause of death; it is also a substantial financial burden on the healthcare system. 

Asthma is a very personalized illness in terms of what triggers it, what could be the treatment plan, and how much improvement that treatment shows. Leveraging this personalization problem as an opportunity, I conducted some primary technological and market research and proposed this project to MSTI faculty. 

I worked with other two team members to gather more evidence on the problem's existence and the root cause of it. I reached out to Ubicomp lab at the University of Washington, to seek technical mentorship. Then as a team, we reached out to doctors and patients to find the root cause. We verified that
- Patient's compliance with a treatment plan is significantly low

  ![Asthma Action Plan](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Asthma_Action_Plan.jpg){: .align-center}
  _<center>Fig 1 - Current non-digital treatment plan given to patients</center>_
- Currently, gathering the non-conventional symptoms/features such as Cough Counts, Air Quality, Activity levels are not in practice; but can be helpful.
- Patient's testimonies on their conditions a week before or so is widely unreliable.
- For patients communicating their conditions with doctors are sometimes hard.

With these problems in mind, we Ideated out the solution to be a mobile application with connected devices to log respiratory vitals(SPO2 & Lung Functions). 


## Continuous Development - Phase-1

For the first quarter of the launch process, we polished our idea further in every aspect of technology, business and design. I took the lead on the design-elements and connected hardware solutions. 

![Initial Prototype Elements](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Initial%20Prototype%20Elements.PNG)
_<center>Fig 2 - Elements of Initial Prototype</center>_

In terms of development, my significant duties involved around IoT, making the hardware and connecting it with could to facilitate data collection. The major challenge was to create a communication channel between the mobile application and Arduino(or any prototyping board). AS I didn't have much experience in dealing with communication interfaces, it required some amount of searching/learning before I figure out the optimum solution.

By the end of the quarter, We had a preliminary prototype ready and working. After multiple feedback sessions and further secondary research, 
- We realize that the major project value relies on data collection and communication. 
- Hardware was unnecessarily slowing us down, and in the future, it might cause scaling issues. 
- We also found that some personal health trackers like Garmin, AmazFit and FitBit already records pulse-ox readings, and some are already providing access to that data through APIs.

Adding this all it didn't make much sense going further with the hardware and we shifted our direction to the more software-centric solution, relacing hardware with data processing elements.