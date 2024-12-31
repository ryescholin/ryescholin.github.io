---
layout: post
title: Model Management Application at Syntiant
date: 2023-09-01 00:00:00 +0300
description: Building a React-based tool to streamline machine learning model management and enhance collaboration.
img: model.png
tags: [Software Engineering, Frontend Development, Machine Learning, React]
---

During my summer 2023 internship, I developed a user interface to help employees manage and interact with a database of machine learning models. This project involved designing a user-friendly tool, implementing core features, and integrating it with existing APIs to streamline workflow and collaboration.

## Understanding the Requirements

I began by meeting with potential users to understand their needs and expectations. Based on their feedback, I drafted several framework designs and discussed them with my mentors and team. This iterative process helped identify the best components and architecture for the project.

![2]({{site.baseurl}}/assets/img/2.png)

## Building the User Interface

Using React with JavaScript, I created a dynamic interface tailored to users' needs. After evaluating options for key components, I selected Tanstack Table for the primary grid due to its flexibility, usability, and scalability. I integrated additional libraries to handle loading states, formatting, and other essential features.

Key pages and features include:

### Model Table – Main Page

The main page displays a sortable grid of models, allowing users to:

- Search by keywords or filter by publication date ranges.
- Sort columns to find models based on specific attributes.
- Use a sidebar to filter by model types, such as templates, snapshots, or recently released versions.

### Model Information Page

After selecting a model, users can view detailed information, including its name, description, ID number, and other attributes. Key features include:

- Editable JSON attributes to update database entries directly.
- Tabs for additional details like attributes and artifacts.

### Artifacts Management

The artifacts tab allows users to upload, edit, delete, and download files related to the model. The table within this tab is searchable and sortable by file name and description, simplifying artifact management.

![3]({{site.baseurl}}/assets/img/3.png)

## Enhancing API Functionality

To support efficient data loading, I worked with my mentors to add pagination to the existing FAST API. This optimization allowed the UI to load only the necessary model entries, improving performance and reducing overhead.

![4]({{site.baseurl}}/assets/img/four.png)

## Technologies Used

- **Languages:** JavaScript, Python
- **Frameworks & Libraries:** React, Tanstack Table, FAST API
- **Platforms:** Browser-based UI, Syntiant’s model database
- **Tools:** JSON, REST APIs

## Results and Impact

The completed tool provides Syntiant employees with an intuitive way to manage machine learning models, streamlining their workflow and improving access to shared resources. Integrated into a suite of other tools, including a neural network designer, this application enhances the overall efficiency of model management.

This project deepened my skills in frontend development, API integration, and user-focused design. It was a rewarding experience to see the application come together and deliver real value to its users.
