---
layout: post
title: One-Minute Qualtrics LTI Demonstration for MOOC Teachers
comments: true
---

<style>
div {
    text-align: justify;
    text-justify: inter-word;
}
</style>

An often-heard desire of both MOOC teachers and researchers is the ability to enhance their courses with sophisticated questionnaires. Here, I demonstrate a Qualtrics LTI bridge, that bridges your MOOC environment with the popular survey software Qualtrics, and ensures that the students' learner IDs are recorded with their responses. Also, the bridge can help you adapt the learning material to particular groups of students, and enable randomized experiments to find out what works best for your students.

This demonstration will show you how to create the bridge in your learning environment, what it will be like from the viewpoint of the student, and how the additional functionality of Qualtrics (such as a rich variety of question or quiz types, personalized learning, and randomized assignment to different variants) can enhance your course. The demonstration will only take a minute to set up, and a Qualtrics account is not necessary (although it will be as soon as you start using the bridge in your own course).

In the following three simple steps I will walk you through the demonstration.

## 1. Open your learning environment

Open the learning environment that you use for your course (if you don't have one, scroll to the bottom of this post). The Qualtrics LTI bridge works with all learning environments that support [LTI](https://en.wikipedia.org/wiki/Learning_Tools_Interoperability). These include the two most popular MOOC providers, edX and Coursera, but also learning management systems like Moodle and Blackboard.

## 2. Create an LTI item

In your learning environment, create an 'LTI item' (terms may very across environments). Make sure to copy the launch URL, consumer key, and consumer secret from the image below. The image shows how the configuration is done in Coursera.

![LTI Configuration](/assets/lti_demonstration.png)

For demonstration purposes it is not necessary to share your learner ID. Of course, when using the LTI bridge in your own course you do want to share the learner ID, as it will enable you to identify your students' responses in Qualtrics.

## 3. Run the demonstration

Now, publish the item and try it. If your setup is correct, you'll be directed to a Qualtrics questionnaire that demonstrates some of its most important features. And once your finished with the questionnaire, you'll be directed back to your learning environment.

That's all there is to it!

## Additional: grading

You want to return the student's Qualtrics quiz grade to your MOOC? You can. Find out more in the [next post](/blog/qualtrics-lti-grading/).

## Inspired?

Are you interested in using the bridge in your own course? It is freely available on [GitHub](https://github.com/renspoesse/qualtrics_lti_bridge) and includes detailed instructions on setting it up. The accompanying [paper](https://osf.io/q53jx/) that you can cite is available as a preprint, and provides an easy introduction to the bridge. If there's anything else, contact me.

## No MOOC?

_If you do not have access to a learning environment, but still would like to view the demonstration, you can use [this website](http://ltiapps.net/test/tc.php). Find the 'registration settings' field, copy the information from the image above, hit 'save data' and then 'launch TP in new window'. This should take you to the demonstration._