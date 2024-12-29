---
layout: post
title: Automated Document Workflow and AI-Powered Data Processing Tool
date: 2024-09-01 00:00:00 +0300
description: Improving workflows and user experience through automation, machine learning, and strategic development for document generation and enrollment data processing tools.
img: cheese.jpg
tags: [Software Engineering, Machine Learning, Automation, Internship]
---

During my Software Engineering Internship at Pacific Life, I contributed to the development of two critical tools: DocGen, a document automation platform, and the BenAdmin Intake App, an AI-powered enrollment tool. These projects addressed operational bottlenecks, significantly improved efficiency, and delivered measurable value to PL's Workforce Benefit's Division and its clients.

## DocGen: Transforming Document Automation

The DocGen platform enables businesses to generate personalized, compliant documents used across policies, claims, and proposals. My work here focused on reducing manual effort while improving the reliability and scalability of the system:

Claims Documentation Enhancements:

- Designed and deployed document packages for claims processes, automating letters like Status Updates, Info Requests, and Claim Acknowledgements.
- Reduced customization time per document instance by 2–3 minutes through advanced data-driven elements.
- Worked with business administrators to ensure all claims packages met operational and regulatory requirements, aligning with a major system release.

Publish Button Solution:

- Investigated and implemented recommendations for publishing finalized documents via the Empower API.
- Developed a proof of concept for an iframe-based editor wrapper that allowed publishing documents outside the client-side Empower Editor.
- Helped Pacific Life avoid costly third-party software acquisitions by proposing reusable in-house solutions.

Instruction File Optimization:

- Enhanced instruction files for improved data extraction from EIS, facilitating smoother integration with the document generation workflow.

![flow]({{site.baseurl}}/assets/img/flow.png)

## BenAdmin Intake App: Simplifying Data Processing for Enrollment

The BenAdmin Intake App streamlines the translation of employer-provided data into formats compatible with Pacific Life's administration systems. My work targeted expanding its functionality, enhancing its accuracy, and streamlining its development process:

Feature Expansion:

- Introduced support for life insurance products, enabling the app to identify and process life insurance data fields effectively.
- Designed logic to auto-fill missing employee data based on existing coverage details, reducing manual input errors.

Machine Learning Integration:

- Utilized scikit-learn to build and refine algorithms for identifying and mapping data columns with high accuracy, supporting both automated and manual workflows.

![ba]({{site.baseurl}}/assets/img/ba.png)

UI and User Experience:

- Leveraged PyQt5 to develop an intuitive interface for loading, mapping, and exporting enrollment data.
- Streamlined the user journey by providing clear mappings and outputs in ready-to-upload formats.

Azure DevOps Integration:

- Created a structured ADO board, introduced tickets, and formalized the use of branches and pull requests, improving collaboration across the team.
- Updated CI/CD pipelines to ensure seamless packaging of dependencies and distribution-ready application builds.

### Technologies Used

- **Languages:** Python
- **Frameworks & Libraries:** PyQt5, scikit-learn
- **Platforms:** OpenText Exstream, Empower API
- **Tools:** Azure DevOps, JSON

### Results and Takeaways

Through these projects, I contributed to automation and process enhancements that saved valuable time, reduced errors, and opened the door for future improvements. My efforts also demonstrated the value of integrating modern software development practices, such as machine learning and DevOps principles, into traditional workflows.

![Poster]({{site.baseurl}}/assets/img/xxx.jpg)
