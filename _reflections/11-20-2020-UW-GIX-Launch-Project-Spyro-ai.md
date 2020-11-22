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

**Asthma is a very personalized illness** in terms of what triggers it, what could be the treatment plan, and how much improvement that treatment shows. Leveraging this personalization problem as an opportunity, I conducted some primary technological and market research and proposed this project to MSTI faculty. 

I worked with other two team members to gather more evidence on the problem's existence and the root cause of it. I reached out to [Ubicomp lab](https://ubicomplab.cs.washington.edu/) at the University of Washington, to seek technical mentorship. Then as a team, we reached out to doctors and patients to find the root cause. We verified that
- Patient's compliance with a treatment plan is significantly low

  ![Asthma Action Plan](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Asthma_Action_Plan.jpg){: .align-center}
  _<center>Fig 1 - Current non-digital treatment plan given to patients</center>_
- Currently, gathering the non-conventional symptoms/features such as **Cough Counts**, **Air Quality**, **Activity levels** are not in practice; but can be helpful.
- Patient's testimonies on their conditions a week before or so is widely unreliable.
- For patients communicating their conditions with doctors are sometimes hard.

> **With these problems in mind, we Ideated out the solution to be a mobile application with connected devices to log respiratory vitals(SPO2 & Lung Functions).** 

<br>
## Continuous Development - Phase-1

For the first quarter of the launch process, we polished our idea further in every aspect of technology, business and design. I took the lead on the design-elements and connected hardware solutions. 

![System Diagram](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/System%20diagram.PNG){: .align-center}
_<center>Fig 2 - High level system diagram</center>_

![Initial Prototype Elements](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Initial%20Prototype%20Elements.PNG)
_<center>Fig 3 - SW & HW Elements of Initial Prototype</center>_

In terms of development, **my significant duties involved around IoT for the first quarter**, making the hardware and connecting it with could to facilitate data collection. The major challenge was to create a communication channel between the mobile application and Arduino(or any prototyping board). 

As I didn't have much experience in dealing with communication interfaces, it required some amount of searching/learning before I figure out the optimum solution.

_By the end of the quarter, We had a preliminary prototype ready and working._ 

![Spirometer Design Rendering](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Spyrometer%203D%20rendering.PNG){: .align-center}
_<center>Fig 4 - 3D rendering of Peak-flow meter prototype</center>_
<br>

![Printed Peak Flow](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Spyrometer-3d-printed.PNG)
_<center>Fig 5 - Initial prototype od Peak-flow meter printed using 3D printer</center>_
<br>

![Working prototype of Pulse-Ox](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Pulse-ox%20prototype.PNG)
_<center>Fig 6 - Working prototype of Pulse-ox to measure blood oxygen saturation levels</center>_
<br>


Prototype was working as expected, with a room of lot of improvements, but after multiple feedback sessions with end-users and experts...
- We realize that most of the **_project value relies on data collection and communication_**.
- **_Hardware was unnecessarily slowing us down_**, and in the future, it might cause scaling issues. 
- We also found that some personal health trackers like Garmin, AmazFit and **_FitBit already records pulse-ox readings_**, and some are already providing access to that data through APIs.

> **Adding this all it didn't make much sense going further with the hardware and we shifted our direction to the more software-centric solution, replacing hardware with data processing elements.**


## Continuous Development - Phase-2

After deprioritizing hardware components from our solution, **I had more time to focus on data processing and data presentation** for the doctor side of the solution.

I started by gathering data presentation requirements for doctors using secondary research. After a technical study, I found that data presentation framework, which also supports data processing is a good fit for this side of the solution. I selected Plotly-Dash as data presentation front end and Python-Flask as data processing backend, which satisfied the requirement.

The tricky part was to make primary data manipulation as easy as possible if **it can't be done in one click; likely, it won't be suited for the solution**. It required a lot of experimentation and design changes to make a primary prototype of web-dashboard, and it's still not perfect but in the workable and usable stage.

[Deployed web-dashboard](https://damp-escarpment-19256.herokuapp.com/)

![web-Dashboard](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/deployed-web-dashboard.PNG)
_<center>Fig 7 - Screenshot of Spyro.ai Web Dashboard</center>_
<br>

On the other side, the team also completed the working prototype of the patient-facing Mobile application.

![Mobile application screenshots](/assets/images/reflections/11-20-2020-UW-GIX-Launch-Project-Spyro-ai/Mobile-app-prototype.PNG)
_<center>Fig 8 - Screen-captures of Spyro.ai Mobile Application </center>_
<br>

I also spent significant time learning video editing and making a team-progress video
<iframe width="640" height="360" src="https://www.youtube.com/embed/Vf48RbAG2kQ" frameborder="0" allowfullscreen></iframe>
_<center>Video 1 - Progress video presented in Milestone-3 </center>_
<br>

In a user-centric approach, without verifying the solution with end-users, it is never complete. Thus we moved forward with comprehensive testing which developing parallelly.

## Final Testing

In the middle of the pandemic, everything was remote, as well as getting appointments with pulmonologists was painstaking. But we moved forward with testing over audio-visual zoom call, and it worked well.

I set up the [calendly](https://calendly.com/) to book appointments and to provide participants with the freedom to choose their preferred time slots. The auto transcription feature of zoom also made things a lot easier for note-taking.

I gathered some development requirements from the user's feedback and implemented them in the web-dashboard.

## Conclusion

Starting with the problem definition, the journey was full of proud moments and some setbacks. Iterative design thinking process allowed me to make changes to our prototype and direction while keep moving forward in this elusive area of technology. 

As a student-led project, time-to-time we had to take a step back and decide whether we are moving in the right direction; This developed sense of ownership and entrepreneurial mindset.

Getting patients feedback and professional's reviews on our prototype kept us user-centric throughout the process. At each iteration of the design thinking process, we focussed on a different aspect of the project like Direction, Business, Design and Usability. This allowed us not just improve on the functionality of the application, but the overall idea which can turn into a business opportunity.