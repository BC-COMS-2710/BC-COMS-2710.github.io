---
title: Computational Text Analysis - COMS 2XXX - Barnard College
layout: default
img: <!-- turk-engraving-detail -->
img_link: <!-- http://en.wikipedia.org/wiki/The_Turk -->
caption: <!--An engraving of the Mechanical Turk, the 18th century chess-playing automaton -->
active_tab: main_page 
---

Computational Text Analysis is the method of using computational tools to analyse and discover insights from large amounts of text. This research based course will introduce students to the methods and tools used in computational text analysis, aka <i>text as data</i>.
Students will learn how to use quantitative methods to <i>discover</i>, <i>measure</i>, and infer concepts and phenomena from large amounts of text. 
The course will involve hands-on analysis of real-world textual datasets from social media (Twitter and Reddit), newswire (Wall Street Journal or NYTimes), and other corpora. This class is ideal for students who are interested in learning how to aggregate large amount of text and apply statistical methods to <i>discover</i>, <i>measure</i>, and <i>infer</i> phenomena from text.
Some prior programming experience is expected, though all necessary skills, including an overview of Unix and Python, will be covered in the beginning of the course.

<!-- Display an alert about upcoming homework assignments -->
{% capture now %}{{'now' | date: '%s'}}{% endcapture %}
{% for page in site.pages %}
{% if page.release_date and page.due_date %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% capture due_date %}{{page.due_date | date: '%s'}}{% endcapture %}
{% if release_date < now and due_date >= now %}
<div class="alert alert-info">
<a href="{{page.url}}">{{ page.title }}</a> has been released.  
{% if page.deliverables %}
The assignment has multiple deliverables.
{% for deliverable in page.deliverables %}
The {{deliverable.description}} is due before {{ deliverable.due_date | date: "%I:%M%p" }} on {{ deliverable.due_date | date: "%A, %B %-d, %Y" }}.  
{% endfor %}
{% else %}
It is due before {{ page.due_date | date: "%I:%M%p" }} on {{ page.due_date | date: "%A, %B %-d, %Y" }}.
{% endif %}
</div>
{% endif %}
{% endif %}
{% endfor %}
<!-- End alert for upcoming homework assignments -->


<!--
<div class="alert alert-info" markdown="1">
Check out the [excellent final projects](http://crowdsourcing-class.org/final-projects-2016.html) from last year's class.
</div>
-->


Course number
: [BC COMS](http://cs.barnard.edu/) 2xxx - students from all majors are welcome!

Instructor
: [Adam Poliak](http://azpoliak.github.io)

Teaching Assistants
: [Course Staff](staff.html) 

Website 
: [TODO]()

Discussion Forum
: [Piazza]() *Requires signing up via a barnard.edu or columbia.edu email*

Time and place
: Summer A May 3rd - June 18th
: Time and Day TBD:
Location: Check courseworks for Zoom link


Office Hours
: <a href="office-hours.html">Times</a>

Prerequisites
: None - no prior programming or college-math background is required

Modes of Thinking Requirement
: Thinking Quantitatively and Empirically
: Thinking Technologically and Digitally

Course Readings
: Each lecture has an accompanying reading that will be posted to the schedule
: Some lectures will have accompanying optional reading related to the lecture's topic

Grading
: This is a project-based course. 
The majority of your grade will be based on assignments.
* Assignments (Homeworks, mini-projects, Final project) - 70%
* Exams and Quizes (Midterm, Daily Quizes) - 25%
* Participation - 10%
* Final Project - 50%
* Homeworks - 30%
* Daily Quizzes - 10%

<!--- 
* Homeworks (20%)
* Projects (25%)
* Pre-course quizes (7.5%)
* Midterm (15%)
* Final Project (25%)
* Participation (7.5%)
-->


<!-- old grading 
This is a project-based course.  Instead of exams, you will do a series of hands-on assignments and a final project.  

* Weekly assignments (45%)
* Final project (45%)
* Peer grading (5%)
* Participation (5%)
-->

Late day policy
: To account for issues that arise in these uncertain times, each student has 10 late days for the homeworks and projects.
<br>
See the [Policies](http://localhost:4000/policies.html#late-days) for more details.
<!--
Each student has five free "late days". Homeworks can be submitted at most two days late. If you are out of late days, then you will not be able to submit your homework. One "day" is defined as anytime between 1 second and 24 hours after the homework deadline. The intent of the late day policy it to allow you to take extra time due to unforseen circumstances like illnesses or family emergencies, and for forseeable interruptions like on campus interviewing and religious holidays. You do not need to ask permission to use your late days. No additional late days are granted.
-->

<!--
#### Acknowledgments
A Google Cloud Education grant is supporting the computational infrastructure for the course.
<br> 
Eric Van Dusen, his staff, and The Data Science Education Community have been very helpful 
in adopting this course at Barnard. 
-->

#### Related Courses
As social science and humanities research heavily incorporates textual data, numerous classes similar to this exist.
Here I will try to keep a running list of related courses.

- Classes that require prior statistical and programmings knowledge:
  - [Text as Data](https://cbail.github.io/textasdata/Text_as_Data.html) by Chris Bail (Sociology, Public Policy, and Dat
a Science) at Duke
  - [Text as Data](https://github.com/justingrimmer/tad_19/blob/master/mac19.pdf) by Justin Grimmer (Political Science) a
t Stanford
  - [Text as Data](https://www.dropbox.com/s/wmqycp11757cekv/TAD_syllabus.pdf?dl=0) by Tamar Mitts (Political Science) at
 Columbia SIPA  
- Classes that focus on Social Media:  
	- [Social Media & Text Analytics](http://socialmedia-class.org/) by Allan Ritter (Computer Science) at Georgia In
stitute of Technology
- Misc:
	- [Quantitative Research Methods (INST 808), Deep Learning for Information Scientists](http://users.umiacs.umd.edu/~jbg/teaching/INST_808/) taught by [Jordan Boyd-Graber](http://users.umiacs.umd.edu/~jbg) at UMD