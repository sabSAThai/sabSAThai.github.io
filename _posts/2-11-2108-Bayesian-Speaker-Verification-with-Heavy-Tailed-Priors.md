---
layout: default
title: "Bayesian Speaker Verification with Heavy-Tailed Priors" 
date: 2016-05-29
desc: 
author: Pranav Sankhe
keywords: "Heavy Tails, Bayesian Inference, Speaker Verification, Student's t distribution"
categories: []
tags: [Anthropic principle]
icon: icon-html
comments: true
---


<div class="wrapper wrapper-content  animated fadeInRight article">
    <div class="row">
        <div class="col-lg-10 col-lg-offset-1">
            <div class="ibox">
                <div class="ibox-content">
                    <div class="pull-right">
                    	{% for category in page.categories %}
                        	<a class="btn btn-white btn-xs" href="{{ category | downcase | prepend: '/' | prepend: site.baseurl }}">{{ category }}</a>
                        {% endfor %}
                    </div>

<div class="text-center article-title">
                    <span class="text-muted"><i class="fa fa-clock-o"></i> {{ page.date | date: "%-d %b %Y" }}</span>
                        <h1>
                            {{ page.title }}
                        </h1>
                    </div>

<p style="font-family:FontAwesome;">

I took this course “Advanced Concentration Inequalities” in my 7th semester where we studied properties of heavy-tailed distributions, their emergence, and statistical tools to estimate their parameters. The course was instructed by Professor Jaikrishnan Nair from EE department. Heavy tails is one of the major research area of Prof Jaikrishnan Nair or ‘JK’ as we fondly call him in the department. 
I am writing this post to document the project which I did in this course and to highlight few key takeaways from this course. \\ 

Instead of an endsemester examination, we had to select a topic based on heavy tails preferably an application of heavy tails and give a 45 minute demonstration to the class about the same. Since my interest lies in audio processing, I was searching for an application of heavy tails in the same and found a rather interesting paper. The author had used heavy tail functions as priors to solve the problem of bayesian speaker verification. I will start with describing the speaker verification problem.  


</p>

<p style="font-family:FontAwesome;">

</p>

<br />


<div class="row">
                        <div class="col-lg-12">
                            <!-- share -->
                            {% include share.html %}
                            <br>
						<div id="disqus_thread"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script src="https://code.jquery.com/jquery-1.10.1.min.js"></script>

<script src="{{site.url}}/js/inlineDisqussions.js"></script>
<script src="{{site.url}}/js/disqus.js"></script>
                            </div>
                        </div>
                        <div class="col-md-4" id="toc-wrapper">
                        </div>
                    </div>
                </div>
            </div>
        </div>

    <!-- jQuery-->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
    <script src="https://code.jquery.com/jquery-1.10.1.min.js"></script>

    <script src="{{site.url}}/bootstrap/js/bootstrap.min.js"></script>

    <script src="{{site.url}}/highlight/highlight.pack.js"></script>
    <script>hljs.initHighlightingOnLoad();</script>

    <script src="{{site.url}}/js/footnotes.js"></script>
    <script src="{{site.url}}/js/bootstrap-carousel.js"></script>
    <script src="{{site.url}}/js/inlineDisqussions.js"></script>
    <script src="{{site.url}}/js/toc.js"></script>


    <script type="text/javascript" src="//cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

    <noscript>Enable JavaScript for footnotes, Disqus comments, and other cool stuff.</noscript>
    <!-- comment -->

</div>
</div>
</div>
</div>
</div>
</div>

</div>
