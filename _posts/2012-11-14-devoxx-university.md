---
layout: post
title: "Devoxx University"
description: "My first two days at Devoxx 2012"
category: 
tags: [java,devoxx,crash,conference]
---
{% include JB/setup %}

# CRaSH session

Alain Defrance and myself arrived in Anterwerpen Sunday evening with a train from Paris with the main goal of finishing the preps for the CRaSH Tools In Action. We've have been working on CRaSH to finish the features for the demo we wanted to show but we did not have time to reharse together since I was in vacation for a week until this day. However we did prepare it carefully for a long time by creating a precise storyboard of the presentation and focusing on the structure, the flow and the interactions between us. Until the last hour we worked on improving those stories and fine tuning them until it became obvious for us and for the audience. I was a bit scared as we did not reharse them before, but it turns out that the impact on the presentation was almost none and everything went fine.

We had 4 demos packed in half and hour, each demo showing a couple of aspects of CRaSH. This choice was good because it gives a natural structure to the talk, minimizes the demo failure risks. One key point is to have a good flow between the demos, so the transitions are easy for the audience.

## Out Of The Box

We show how to download and install CRaSH, the directory layout and the base configuration., After that we run the standalone mode and show basic commands that are immediatly available. At the end of the demo, we show the new [crashub.org](http://www.crashub.org/) site and the [web demo](http://crash.vietj.cloudbees.net), allowing the audience could use CRaSH from their laptop during the talk!!! 

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/ootb.png" class="img-polaroid"></img></div>

## The Swiss Knife

We explain the concept of attaching CRaSH to a running JVM and in this part we connect to JBoss AS. Thanks to the *log* command we print a message on AS7 console to show that the JVM running CRaSH in JBoss AS. Then we showed what CRaSH brings to the EE developer with commands:

* JNDI : a jndi viewer, for instance **jndi find** list the content of the naming tree.
* JDBC : open an existing an JDBC connection from a JNDI datasource and use it out of the box
* JPA : the new companion of the JDBC command that provides access to your entity beans, allowing to perform live JPA QL queries

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/knife.png" class="img-polaroid"></img></div>

## Extend your runtime

This time the goal is to show we can embed CRaSH in a runtime and create commands interactively. CRaSH is started and configured by a context, in this case CRaSH is started as a Spring bean. Then we code a live command: the Twitter commands which retrieves twits from a Twitter service Spring bean. The command is accessed via an SSH connection.

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/twitter.png" class="img-polaroid"></img></div>

## Monitoring

The last part attaches CRaSH to a Tomcat server. The new jmx commands allows to retrive statistics from the Tomcat MBeans, we combine this command with the sort command and make a command pipe to process an object stream that gets data from the Tomcat MBeans, sort them and display tabular data. We conclude the demo by showing the new CRaSH dashboard feature and put the JMX pipe we previously code in the dashboard.

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/dashboard.png" class="img-polaroid"></img></div>

Although most of the talk is about demoing CRaSH, we had a [few slides](http://www.slideshare.net/jviet/crash-the-shell-for-the-jvm) we used to drive the presentation. We had a very good attendance, considering the time the talk was given and the hard competition against other slots, we had a great feedback on Twitter about the demo that people loved. 

Finally, it was a long time since I wasn't on stage, I was a bit anxious until the last minute given how large the stage is and how small we are (<a href="/wp-content/uploads/2012/11/stage.png">you can look here</a>). But once it started I felt very comfortable and was very proud to show our stuff.

# Hackergarten

On day 2 we participated in the Hackergarten the whole day. Many open source developers showed up and the competition was hard to get people involved. It looks like at the end, not many external people contributed to the Hackergarten and the present open source developers end up contributing on their own project. It was a great social experience though I think, as open source guys from different projects could discuss, share ideas and create bridges between projects.

On our side, Stefan stepped up and was interested in creating a synergy between Grails and CRaSH. He spent the whole day to create a Grails plugin that embeds CRaSH in Grails. The code will be contributed to the crashub organization as a new project and that's a great win for CRaSH :-)

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/img_0036.jpg" class="img-polaroid"></img></div>

Alain Defrance started to reuse most of the Swing VisualVM plugin to create an Intellij plugin. You can expect to see this soon.

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/img_0032.jpg" class="img-polaroid"></img></div>

On my side, I fixed a couple of bugs in CRaSH and spend lot of time talking with other people. I had an long and fruitfull discussion with Dan Allen about Arquillian, testing and open source. I also had the opportunity to show Juzu, the web framework I've been working on for a year to a few JBoss folks that seemed to like it.

<div style="text-align:center"><img src="/wp-content/uploads/2012/11/img_0049.jpg" class="img-polaroid"></img></div>

Now we will to enjoy the rest of the conference and spend time in the conference!
