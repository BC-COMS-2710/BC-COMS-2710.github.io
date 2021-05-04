---
layout: default
title: Lectures
active_tab: lectures
---

<!-- Create a HTML anchor for the most recent lecture -->
{% assign anchor_created = false %}
{% capture now %}{{'now' | date: '%s'}}{% endcapture %}
<!-- End create a HTML anchor for the most recent lecture -->


<div class="alert alert-info">
You can <a href="https://columbia.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx#folderID=%22b5b51c7f-33cd-4a6b-8dfc-acfd01007b3b%22">watch recordings of the lecture videos online</a>.
Recordings are saved on Panopto and require a UNI login.
</div>

The lecture schedule will be updated as the term progresses. 

### Week 0 - Pre-course

Make sure to fill out the pre-course survey that is available on Slack.

Make sure you are registered for the course [Gradescope](https://www.gradescope.com/), [JupyterHub](https://coms2710.columbiajupyter2.org/)
and [Slack](https://bc-coms-2710-summera.slack.com/).

{% for week in site.data.schedule %}
  <h3>
    {{ week.name }}
  </h3>

  {% if week.readings %}
  <h4>
  	 Weekly Readings - Due {{week.readings_deadline | date: '%a, %b %-d, %Y'}} 
	 {% if week.readings_overleaf %} <a href="{{ week.readings_overleaf }}"> - Overleaf Template</a>
	 {% endif %}
  </h4>
  
  <ul 
  	class="{{ week.name }}-readings">
  	
  {% for reading in week.readings %}
  	<li>
  		<a href="{{ reading.url }}">{{ reading.title }}</a> 
      {{ reading.citation }}
  	</li>

  {% endfor %}
  </ul>
  {% endif %}

  {% if week.homework_title %}
  <h4>
    Weekly Homework - Due {{ week.homework_deadline | date: '%a, %b %-d, %Y'}}
  </h4>

  <ul>
    
    <li> {% if week.homework_url %} 
            <a href="{{ week.homework_url }}">{{ week.homework_title }}</a>
         {% else %} 
           {{ week.homework_title }}
         {% endif %}
    </li>
  </ul>

  {% endif %}
  	
  <table class="table table-striped">
    <thead>
      <tr>
        <th>Date</th> 
        <th>Topic</th>
        <!--<th>Recordings</th>-->
        <th>Reading</th>
        <th>Tutorial</th>
      </tr>
    </thead>
    <tbody>

      {% for lecture in week.lectures %}

        <!-- Create a HTML anchor for the most recent lecture -->
        {% capture lecture_date %}{{lecture.date | date: '%s'}}{% endcapture %}
        {% assign lecture_date = lecture_date | plus: 0 %}
        {% assign now = now | minus: 14400 %}

        <tr
        {% if anchor_created != true and lecture_date >= now %}
          {% assign anchor_created = true %}
          id="now" 
        {% endif %}
        
        {% if lecture.type %}
          {% if lecture.type and lecture.type == 'exam' %}
            class="info" 
          {% else if lecture.type and lecture.type == 'deadline' %}
            class="warning"
          {% else if lecture.type and lecture.type == 'no_lecture' %}
            class="warning"
          {% endif %}
        {% endif %}
        >

        <!-- End create a HTML anchor for the most recent lecture -->
          <td>{{ lecture.date | date: '%a, %b %-d, %Y' }}</td>
          <td>
         
            {{ lecture.title }} 
            {% if lecture.slides %}
              <a href="{{ lecture.slides }}">[slides]</a>
            {% endif %}
            {% if lecture.notebook %}
              <br>
              <a href="{{ lecture.notebook }}">[empty notebook]</a>
            {% endif %}
            {% if lecture.completed_notebook %}
              <br>
              <a href="{{ lecture.completed_notebook }}">[completed notebook]</a>
            {% endif %}
            <br>
       

           




          {% if lecture.recording %}
            <a href="{{ lecture.recording }}">[video] </a>
          {% endif %}

  	    {% if lecture.speaker %}
            {% if lecture.speaker_url %}
              by <a href="{{ lecture.speaker_url }}">{{ lecture.speaker }}</a> 
            {% else %} 
            by {{ lecture.speaker }}
            {% endif %}
  	    {% endif %}

        </td>
        <td>	
          {% if lecture.readings %} 	
            {% for reading in lecture.readings %}	
            {% if reading.url %}	
                {% if reading.optional %}<b>Optional:</b> {% endif %}	
                {% if reading.authors %}	
                {{ reading.authors }}, 	
                {% endif %}	
                <a href="{{ reading.url }}">{{ reading.title }}</a> 	
              <br />	
            {% else %}	
                {% if reading.optional %}<b>Optional</b> {% endif %}	
                {% if reading.authors %}	
                {{ reading.authors }}, 	
                {% endif %}	
               {{ reading.title }} 	
              <br />	
            {% endif %}	
            {% endfor %}	
          {% endif %}	
        </td>
        <td>
          {% if lecture.assignments %} 
            {% for assignment in lecture.assignments %}
                {% if assignment.canceled %}<strike> {% endif %}
                {% if assignment.optional %}<b>Optional:</b> {% endif %}
                {% if assignment.url %}
                  <a href="{{ assignment.url }}">{{ assignment.title }}</a> 
                {% else %}
                  {{ assignment.title }}
                {% endif %}
                (Due {{assignment.deadline | date: '%a, %b %-d, %Y' }})
                {% if assignment.canceled %}</strike> {% endif %}
            <br />
            {% endfor %}
          {% endif %}
        </td>
      </tr>
      {% endfor %}
      
    </tbody>
  </table>

  {% endfor %}
