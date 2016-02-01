---
layout: post
title: A/B Tests in Online Learning
---

<style>
div {
    text-align: justify;
    text-justify: inter-word;
}
</style>

A/B tests are not only beneficial in website optimization, but too have great potential in leveraging online learning. In this very (very) brief post on A/B testing in online learning environments, I share some links to interesting online material that collectively may serve as a primer on the topic.

![Experimental comparisons](/assets/abtesting_kevindooley.jpg)

## A/B tests
[A/B tests](http://www.wired.com/2012/04/ff_abtesting) are large-scale online randomized controlled experiments. Meaning, an online environment such as a webpage or app is randomly varied (hence A and B) across users, and after some time it is evaluated which variant is most effective. The randomization and large scale make sure alternative explanations are controlled for. Naturally, an A/B-test can be extended to any complexity one desires (e.g., an A/B/n or multivariate test).

Although superficially the idea is simple and straightforward, proper A/B testing is [far from trivial](http://www.qubit.com/sites/default/files/pdf/mostwinningabtestresultsareillusory_0.pdf). One great way to learn more about it is through the [online course](https://www.udacity.com/course/ab-testing--ud257) from Udacity. Also, Ronny Kohavi and his team are some of the few that publish many [excellent papers](http://www.exp-platform.com) on A/B testing.

Others that point out difficulties and propose solutions are for instance [Slater Stich](http://sl8r000.github.io/ab_testing_statistics/), [Manojit Nandi](http://blog.dominodatalab.com/ab-testing-with-hierarchical-models-in-python/), and [Will Kurt](https://www.countbayesie.com/blog/2015/4/25/bayesian-ab-testing).

## Online learning
Large-scale online learning environments provide an excellent opportunity for experimentally optimizing learning gains. A few online educators are known to run A/B tests, such as [DuoLingo](http://duolingo.wikia.com/wiki/Experimental_feature) and [Khan Academy](http://bjk5.com/post/10171483254/abingo-split-testing-now-on-app-engine-built-for). However, results are shared only sporadically and informally (e.g., [here](http://www.slate.com/articles/technology/technology/2014/01/duolingo_the_free_language_learning_app_that_s_addictive_and_fun.html), [here](http://cs-blog.khanacademy.org/2014/03/ab-testing-curriculum-to-sneak-peek-or.html), and [here](http://www.technologyreview.com/news/515396/as-data-floods-in-massive-open-online-courses-evolve/)), and most of the environments are not available to external academic researchers.

A notable exception is the intelligent tutoring software ASSISTments. ASSISTments uses a [crowdsource model](https://sites.google.com/site/assistmentstestbed/) that enables external researchers to run experiments on the platform. Moreover, massive open online courses (MOOCs) may as well lend itself to A/B tests (e.g., [EdX content experiments](http://edx-open-learning-xml.readthedocs.org/en/latest/content-experiments/index.html)), as long as the platform allows and preferably facilitates such tests and one can cooperate with a teacher on the platform. Finally, but unverified, DuoLingo says its crowdsourced course building platform [provides A/B testing capabilities](http://www.fastcolabs.com/3029531/how-duolingo-uses-a-b-testing-to-understand-the-way-you-learn).

Others working on A/B testing in online learning are for instance [Joseph Williams](http://www.josephjaywilliams.com/mooclet). I myself am currently setting up A/B tests in [Math Garden](http://www.mathsgarden.com/) and a [Coursera specialization](https://www.coursera.org/specializations/social-science). If you're interested in the topic or wish to cooperate (either in setting up experiments or analyzing its data), feel free to send me a message.

<hr />

<span style="color: #808080;">Photo: <a style="color: #808080;" href="https://www.flickr.com/photos/pagedooley/4289850727/" target="_blank">Kevin Dooley</a> / Flickr</span>