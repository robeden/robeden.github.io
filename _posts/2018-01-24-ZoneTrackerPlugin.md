---
layout: post
title:  "'ZoneTracker' Plugin? 🤔"
excerpt_separator: <!--more-->
categories: software
---

It's well know that interruptions are the plague of the modern developer. Getting 
"in the zone" is hard but being ripped out is –unfortunately– easy. Of course, if you
give a software guy a problem, he's likely to think of a software solution. Here's mine...
<!--more-->

My work situation is bit complex from an interruption standpoint. As is common these days,
we have a fairly open cubical configuration. We've also recently rearranged cubes so my
team is all close. This has been great for communication but challenging for 
interruptions. The main difficulty is that I'm lead engineer and team lead. My team has
a broad range of experience levels and right now we have a number of projects in early
stages. This all adds up to lots of great conversations. I love this stage with it's
planning and collaboration; it's one of my favorite parts of development. But at this stage in
my career I find it very difficult to get enough time to be really productive
coding.

Part of the problem is that just blocking out time isn't sufficient because not all time
is equal. I could simply create "office hours" to control when I'm available, but that
would be (vastly) overly restrictive. Much of my time is also taken up with project
planning (i.e., Jira), code reviews and other important tasks (i.e., web surfing) and when
I'm in this mode I really don't mind interruptions at all. Having a "closed door" (even
if it's virtual) must be done sometimes, but is something I'd like to avoid as much as 
possible.

My solution to this has been [a colored light](https://blink1.thingm.com) above my cube 
indicating my level of willingness to be interrupted: green = open door, yellow =
for "important" stuff", red = go away. This works okay, but it's currently a manual 
setting. I have to plan ahead of time to "go red" and then –crucially– remember to turn
it back green. Forgetting to do so means training people to ignore the light. What I 
really want is a more automatic solution. This was [CommitStrip's solution](http://www.commitstrip.com/en/2018/01/11/the-war-on-interruptions/):

<a href="http://www.commitstrip.com/en/2018/01/11/the-war-on-interruptions/">![CommitStrip comic: War on Interruptions](/images/ext/20180124-commitstrip-war-on-interruptions.jpg "CommitStrip: War on Interruptions")</a>

I mean, I like that concept very much. But I suspect some issues in the implementation 
phase.

What (I think) I really want is an indicator of how "in the zone" I am. Take for example
this study on [unplanned interruptions in software development](https://novicearshad.wordpress.com/2012/01/24/unplanned-interruptions-in-software-development/).
The measurement of the percentage impact of an interruption may be debatable, but I
find the basic concept to be true. Also, I agree it takes time to build into a really
productive state. So, the goal should be to get there and stay there for as long as
possible and practical (without shirking "team lead" duties, etc.).

So without further ado, here's my idea. With very little exception, my "real development work"
with is done in [IntelliJ IDEA](https://www.jetbrains.com/idea). I propose that 
–in general– the longer I've been working there without interruption, the more focused I
should be on the task. I'm thinking a plugin could be developed to predict how "in the 
zone" I am based on my work there. Factors such as continual operation (scrolling, 
file changes, typing) could be monitored as well as possibly the rate of typing could be
factored along with a "build up" time (probably non-linear) to quantify the productivity, similar to the report
cited earlier. "Cooldown" time should also be taken into account when progress stops for a duration (again, probably non-linear).

Once a number can generated for productivity or in-the-zone-ness or whatever you want to
call it, many interesting things can be done. First, obviously, there are statistics and
reports... because who doesn't love statistics and reports? Second, I would like to 
associate a color scale (green or blue to red) with that value. It could easily allow
executing shell scripts with parameters that would allow my Blink(1) light to display 
that color. That way my status light is more closely tied to where I'm really at 
concentration-wise at that moment. Also, scripts could be fired when hitting tiers 
(say, 80%?) to do things like mute instant messaging notifications and other such 
distractions since higher productivity is more valuable.

So, dear internet, I ask: what do you think? First, does something like this already 
exist? Project time is scarce, so I don't really want to re-build where there's already 
a solution. Second, do you think this would be useful? What capabilities would you look 
for? Are there other metrics that should be considered in determining when someone is
"in the zone"?