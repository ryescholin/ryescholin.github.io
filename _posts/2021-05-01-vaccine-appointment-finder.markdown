---
layout: post
title: Vaccine Appointment Finder for PSPR
date: 2021-05-01 00:00:00 +0300
description: Building an autonomous text line to help users find COVID-19 vaccine appointments quickly and efficiently during the pandemic.
img: zoom.png
tags:
  [
    Software Development,
    Nonprofit,
    JavaScript,
    Machine Learning,
    Community Impact,
  ]
---

In April 2020, I founded the Portland Student Pandemic Response, a nonprofit organization created to connect students with local service opportunities to support their communities during the pandemic. Over time, it expanded to include summer and after-school programs, events, and community engagement initiatives.

<div style="text-align: center;">
  <img src="{{site.baseurl}}/assets/img/vac.png" alt="vac">
</div>

### Vaccine Finder: An Autonomous Solution

One of our most impactful projects was the Vaccine Finder, developed when COVID-19 vaccines first became available and securing appointments was a significant challenge. The appointment slots filled up quickly, often requiring hours of effort over several days to check multiple pharmacies.

Our goal was to simplify this process, especially for those with limited time due to work or childcare responsibilities. We launched the **Portland Student Pandemic Response Vaccine Finder**, an autonomous text line that searched for vaccine appointments by zip code.

### How It Worked

The tool, built using **JavaScript** and **Twilio**, leveraged real-time data from an open-source project that tracked pharmacy availability. Here’s how the process worked:

1. **Eligibility Check**: Users texted a number and answered yes/no questions to confirm their vaccine eligibility (or skipped this step if they already knew).
2. **Zip Code Search**: Users entered their zip code, and the application responded with a list of nearby pharmacies, their available appointments, and links for booking.
3. **Predicted Availability**: In later versions, if no appointments were available, the tool predicted the next wave of availability using **TensorFlow** and historical data on when new appointments were added.

### Collaboration and Impact

This was a team effort—some members handled marketing, others created support documents, and I focused on building the tool itself.

With help from local media coverage, the Vaccine Finder was widely adopted. During its active months, it was used over **409,000 times**, with overwhelmingly positive feedback from the community.

### Media Coverage

- Check out a [TV interview about the text line HERE](https://www.kgw.com/article/news/health/coronavirus/vaccine/portland-students-launch-covid-vaccine-appointment-finder-text-line/283-314c29ad-35b4-473b-b898-72bef196c406).
- Check out a [Radio interview about the text line HERE](https://www.opb.org/article/2021/04/16/portland-area-high-schools-covid-19-vaccine-finder/).

### Technologies Used

- **Languages:** JavaScript
- **Libraries & Frameworks:** TensorFlow
- **Platforms:** Twilio
- **Tools:** Open-source data integration

The Vaccine Finder demonstrated how technology could address critical community needs, providing a scalable solution during a challenging time. It remains one of the most rewarding projects I’ve worked on, showcasing the power of collaboration and innovation.
