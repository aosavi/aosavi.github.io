---
layout: post
title: Evidence-Based Improvements to Coursera Courses Using a Qualtrics Integration 
---

<style>
div {
    text-align: justify;
    text-justify: inter-word;
}
</style>

Most platforms for Massive Open Online Courses (MOOCs) do not allow their lecturers to use randomized controlled experiments to detect evidence-based improvements for their course. Regrettably, because the M in MOOC offers a powerful opportunity to do so. Therefore, in order to make these experiments possible I was elected for the [UvA Grassroots program](http://icto.uva.nl/icto-centraal/uva-grassroots/); a fund for ICT innovations in education. The post below introduces the project (first published in Dutch on the [UvA Grassroots blog](http://ict-innovatie.uva.nl/2016/01/27/coursera-qualtrics-een-lti-integratie-uit-de-frontlinie/)).

![CourseraQualtrics](/assets/courseraqualtrics.png)

## Optimizing learning in MOOCs
The University of Amsterdam partners with Coursera to offer Massive Open Online Courses (MOOCs). MOOCs are free online courses that can be followed by many students at once. Such courses have a few interesting promises. Firstly, the large number of students that follow those courses enable us to reliably investigate the factors that optimize learning. Moreover, the online learning environment allows for extensive customization of the learning experience. Unfortunately, delivering on these promises appears to be far from trivial, and thus in the current Grassroots project [Annemarie Zand Scholten](https://www.coursera.org/instructor/annemarie) and I aim to take an important first step.

## The tool
The first phase of that step has been completed. This phase consisted of formally connecting the MOOC provider Coursera with the Qualtrics survey software. We established the connection with the aid of the LTI protocol (i.e., Learning Tools Interoperability), which enables information to be sent from Coursera to Qualtrics. The possibility to return information from Qualtrics to Coursera might be added in the future. The tool that creates the connection, including a user manual, is freely available at [GitHub](https://github.com/renspoesse/qualtrics_lti_bridge).

## The possibilities
The link between Coursera and Qualtrics is a first step towards both promises. Qualtrics offers rich opportunities to provide additional material, such as text, video, and questions, but above all the possibility to randomly assign students to different learning materials. The experimental situation thus created enables us to determine which learning material leads to the largest learning gain. Additionaly, because information can be sent from Coursera to Qualtrics, it is in principle possible to personalize the material on the basis of person-specific characteristics. Unfortunately, at the moment both Coursera and the LTI protocol solely offer to communicate the user ID to Qualtrics, so proper personalization is not (yet) possible. Should this change in the future, then the tool can be easily modified such that personalization of the learning material is still possible.

## The future
In the second phase of the project the manual will be completed and disseminated such that Coursera lecturers worldwide can use the tool and improve their courses. Furthermore, we consider adapting the tool to enable it to send grades from Qualtrics to Coursera, and we are planning to use the tool within the courses of Annemarie Zand Scholten. Finally, we would like to thank Simon Wiles from Stanford University, who built the [foundation of the tool](https://github.com/cognitivesciencelearning/qualtrics_lti_bridge) and made it publicly available, and Rens Poesse from the University of Amsterdam, who adapted the tool for use with Coursera.