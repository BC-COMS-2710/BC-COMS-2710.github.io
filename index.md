---
title: Computational Text Analysis - COMS 2710 - Barnard College
layout: default
img: <!-- turk-engraving-detail -->
img_link: <!-- http://en.wikipedia.org/wiki/The_Turk -->
caption: <!--An engraving of the Mechanical Turk, the 18th century chess-playing automaton -->
active_tab: main_page 
---

Computational Text Analysis is the method of using computational tools to analyse and discover insights from large amounts of text. This research based course will introduce students to  methods and tools used in computational text analysis, aka <i>text as data</i>.
The course will focus on a [*subset of computational methods that derive from statistical modeling and computational linguistics that are most commonly applied to analyze texts at scale*](https://arcade.stanford.edu/blogs/distant-reading-after-moretti).

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
: [BC COMS](http://cs.barnard.edu/) 2710 - students from all majors are welcome!
: ***This course likely does not count for the CS Major***

Instructor
: [Adam Poliak](http://azpoliak.github.io)

Teaching Assistants
: [Course Staff](staff.html) 

Website 
: [https://coms2710.barnard.edu/](https://coms2710.barnard.edu/)

Discussion Forum
: [Piazza]() *Requires signing up via a barnard.edu or columbia.edu email*

Time and place
: Summer A May 3rd - June 18th
: Time and Day: TBD
: Location: Check courseworks for Zoom link


Office Hours
: <a href="office-hours.html">Times</a>

Prerequisites
: Prior programming experience. Some prior programming course that are suitable include [BC1016](http://coms1016.barnard.edu/), [BC3050](https://edblogs.columbia.edu/eescx3050-001-2015-3/), W1004, E1006, W1002, [STAT UN2102](https://leewtai.github.io/courses/stat_computing/syllabus.html)

Modes of Thinking Requirement
: Thinking Quantitatively and Empirically
: Thinking Technologically and Digitally

Textbook & Course Readings
: Each lecture has an accompanying reading that will be posted to the schedule. Some lectures will have accompanying optional reading related to the lecture's topic.
: We will be using primarily three textbooks for this course:
1. [Text Analysis in Python for Social Scientists](https://www.cambridge.org/core/elements/text-analysis-in-python-for-social-scientists/BFAB0A3604C7E29F6198EA2F7941DFF3). A copy has been put on course reserves at the Barnard Library. 
1. Jurafsky and Martin, Speech and Language Processing (3rd ed. draft) [(online copy)](https://web.stanford.edu/~jurafsky/slp3/)
2. [Computational Text Analysis Textbook](https://bc-coms-2710.github.io/textbook/welcome.html) is an online textbook. It is a modified version of the textbook Melanie Walsh at Cornell developed for her [Intro to Culturual Analytics course](https://melaniewalsh.github.io/Intro-Cultural-Analytics/welcome.html).

Grading
: This is a project-based course. 
The majority of your grade will be based on assignments.
* Final Project - 25%
* Homeworks - 65%
* Participation - 10%

Assignments
: During the first 4 weeks of the course, students will complete a mix of daily assignments and week long assignments. These assignments will help students master the material while preparing them for their final projects

- The daily assignments will be based on the day's lecture and then due at midnight.
- The week long assignments will cover the previous week's material and will be due at midnight on Sunday night. 

Final Project
: During the last two weeks of the course, students will primarily work on final projects. In the final projects, students will be required to collect and analyze a text corpus to answer a research question of their choosing. For the final project, students will be encouraged to develop and test their own research question but will have the option of
reproducing results from a list of approved recent research papers instead.

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
: To account for issues that arise in these uncertain times, each student has ?? late days for the homeworks and projects.
<br>
See the [Policies](https://coms2710.barnard.edu/policies.html#late-days) for more details.
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
  - [Text as Data](https://cbail.github.io/textasdata/Text_as_Data.html) by Chris Bail (Sociology, Public Policy and Data Science) at Duke
  - [Text as Data](https://github.com/justingrimmer/tad_19/blob/master/mac19.pdf) by Justin Grimmer (Political Science) at Stanford
  - [Text as Data](https://www.dropbox.com/s/wmqycp11757cekv/TAD_syllabus.pdf?dl=0) by Tamar Mitts (Political Science) at
 Columbia SIPA
- Classes that do not require statistical and programming knowledge:
  - [TEXT MINING FOR HISTORY & LITERATURE](https://mimno.infosci.cornell.edu/info3350/) by [David Mimno](https://mimno.infosci.cornell.edu/) (Information Science) at Cornell.
  - [WORKING WITH TEXT IN PYTHON](https://applied-language-technology.readthedocs.io/en/latest/index.html) by [Tuomo Hiippala](https://www.mv.helsinki.fi/home/thiippal/) (Department of Languages) at University of Helsinki.
  - [Introduction to Cultural Analytics & Python](https://melaniewalsh.github.io/Intro-Cultural-Analytics/welcome.html) by [Melanie Walsh](https://melaniewalsh.org/) (Information Science) at Cornell.
- Classes that focus on Social Media:  
	- [Social Media & Text Analytics](http://socialmedia-class.org/) by Alan Ritter (Computer Science) at Georgia In
stitute of Technology
- Misc:
	- [Quantitative Research Methods (INST 808), Deep Learning for Information Scientists](http://users.umiacs.umd.edu/~jbg/teaching/INST_808/) taught by [Jordan Boyd-Graber](http://users.umiacs.umd.edu/~jbg) at UMD
