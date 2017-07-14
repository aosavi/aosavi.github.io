---
layout: post
title: How to Return Qualtrics Quiz Grades to your MOOC
comments: true
---

<style>
div {
    text-align: justify;
    text-justify: inter-word;
}
</style>

You are teaching a MOOC or using a more traditional virtual learning environment (VLE)? You want to enhance your course with external exercises and quizzes? And you want the external tool to return the students' grades to your MOOC/VLE? Here, I'll show you how to do it.

## 1. The Qualtrics LTI bridge

Qualtrics survey software will enable you to create enhanced questionnaires and quizzes. In order to return the grade from a Qualtrics quiz to the MOOC or VLE of your choice, you'll first need to make sure to setup the Qualtrics LTI bridge. The following resources will introduce you to the tool and help you set it up:

* A [demonstration](/blog/qualtrics-lti-demonstration/) of the bridge, without grade returns. Settings for a demonstration with grade returns are provided below.
* Detailed [instructions](https://github.com/renspoesse/qualtrics_lti_bridge) on setting up the bridge.
* The [paper](https://osf.io/q53jx/) about the bridge.

## 2. Grading

Now that you've got the bridge in place, it's time to make sure grades can be sent from Qualtrics to your MOOC.  You have two options. Either you assign a fixed grade, for instance to simply see whether a student finished a quiz or questionnaire, or you assign a variable grade, for instance to reflect the proportion correct answers.

### Fixed grades

You might just want to know whether a student finished the quiz or questionnaire, without the need to assign a variable grade. You can do this by following the instructions on [setting up the tool provider](https://github.com/renspoesse/qualtrics_lti_bridge/#setting-up-the-tool-provider-qualtrics). By setting `custom_grade=1`, Qualtrics will return a `1` (or 100%) whenever a student finishes the questionnaire or quiz. You can set this value to any value in the range of `0.00` to `1.00` (which corresponds to 0% to 100% correct).

### Variable grades

However, in a quiz setting, you're most likely interested in the proportion correct. Such a variable grade is a little more tricky, but Qualtrics does provide the means to return such a grade:

1. Make sure you understand [scoring](https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/response-management-tools/scoring/) in Qualtrics.
1. Set up scoring for your Qualtrics quiz.
1. Make sure you understand [math operations and embedded data fields](https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/response-management-tools/scoring/#MoreInformation) in Qualtrics (follow the link and check the links under More Information).

Now that you've set up scoring and know about math operations and embedded data, it's time to use this knowledge to create variable grades:

1. Go to the Survey Flow of your quiz.
1. If you've set up the Qualtrics bridge correctly, you already have a `Set Embedded Data` element.
1. Create another `Set Embedded Data` element at the end of the Survey Flow.
1. In this element, add a new field and name it `custom_grade`.
1. You can now [create your own formula](https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/piped-text/math-operations/) to calculate the grade for a student. Importantly, make sure the grade cannot exceed the range of `0.00` to `1.00`.

In the simplest case you can have 10 items, where each correct answer is scored with a `0.1`. If you let `custom_grade` be the score, the grade will automatically reflect the proportion correct.

![Scoring](/assets/scoring.png)
![Survey Flow](/assets/survey_flow.png)

Now that you have a variable grade, it's time to make sure you can return it to your MOOC or VLE:

1. Add another new field (this time, the name you give it is irrelevant).
1. Set a value for that field, select Insert Piped Text > Embedded Data Field, and insert `custom_grade`.
1. Copy the piped text that just appeared as the new value, most likely `${e://Field/custom_grade}`.
1. You can remove the field with the irrelevant name if you wish, since it won't be used anymore.

The piped text carries the variable grade and is used by the Qualtrics LTI tool to return it to the MOOC:

1. Go to the Survey Options of your quiz and find the Survey Termination Redirect URL.
1. If you've set up the Qualtrics bridge correctly, this redirect URL has the value of `1` attached to the `custom_grade` parameter (see instructions on [setting up the tool provider](https://github.com/renspoesse/qualtrics_lti_bridge/#setting-up-the-tool-provider-qualtrics)).
1. Replace the `1` with the piped text, which will most likely result in `[URL]&custom_grade=${e://Field/custom_grade}`.

## 3. Returning grades

Of course, you'll want your MOOC to collect this grade. You can do this by following the instructions on [setting up the tool consumer](https://github.com/renspoesse/qualtrics_lti_bridge/#setting-up-the-tool-consumer-coursera). That is, simply make sure you enable grading callbacks when setting up the LTI item in your MOOC, and optionally, set the return URL.

## 4. A demonstration

Use the instructions from the [demonstration post](/blog/qualtrics-lti-demonstration/) and the settings from the image below.

![LTI Configuration](/assets/lti_grading.png)

Happy grading!