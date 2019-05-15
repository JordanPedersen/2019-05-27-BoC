---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "lc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc").  
                      # Be sure to update the Carpentry type in _config.yml as well.  
venue: "Bank of Canada"        # brief name of host site without address (e.g., "Euphoric State University")
address: "234 Wellington St, Ottawa, ON"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "ca"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latlng: "45.4208,75.7029"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "May 27-28, 2019"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 am - 4:20 pm, 9:00 am - 4:00 pm"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2019-05-27      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2019-05-28        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Jordan Pedersen", "Elaine Wong"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Michele Sura"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["msura@bank-banque-canada.ca","jordan.pedersen@mail.utoronto.ca"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}



{% comment %}
For a workshop please delete the following block
{% endcomment %}
This is a two day Library Carpentry Workshop arranged by the Bank of Canada's Knowledge and Information Service and will be delivered in English. The workshop will run from 9:00 - 4:00 pm approximately both days, and 4:00 - 5:00 pm will be reserved for individual Q&A with the instructors. Participants will be able choose which modules they attend, contact Michele Sura (msura@bank-banque-canada.ca) to RSVP.

The FAIR Data curriculum is being piloted, and will be taught in part by Natasha Simons and Chris Erdmann via video call.

Wifi instructions for Government of Canada information professionals will be given by Michele Sura on the day of the event.

{% if page.carpentry != site.carpentry %}
<div class="alert alert-warning">
You specified <code>carpentry: {{page.carpentry}}</code> in <code>index.md</code> and
<code>carpentry: {{site.carpentry}}</code> in <code>_config.yml</code>. Make sure you edit both files. After editing <code>_config.yml</code>, you need to run <code>make serve</code> again to 
see the changes take effect locally.
</div>
{% endif %}


<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) with Git and OpenRefine (we acknowledge that these are conditional based approved by the Bank of Canada IT department or the respective Government IT department). They should have a few specific software packages installed (listed <a href="#setup">below</a>).
</p>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<p id="code-of-conduct">
<strong>Code of Conduct:</strong>  Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. This document also outlines how to report an incident if needed.
</p>


{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

{% comment %} 
SURVEYS - DO NOT EDIT SURVEY LINKS 
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
{% if site.carpentry == "swc" %} 
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif site.carpentry == "dc" %}
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif site.carpentry == "lc" %}
<p><a href="{{ site.lc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.lc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% endif %}

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

{% if page.carpentry == "swc" %}
{% include sc/schedule.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/schedule.html %}
{% endif %}

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>

{% if page.carpentry == "swc" %}
{% include sc/syllabus.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}

<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  To participate in a
  {% if page.carpentry == "swc" %}
  Software Carpentry
  {% elsif page.carpentry == "dc" %}
  Data Carpentry
  {% elsif page.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  workshop,
  you will need access to the software described below.
  In addition, you will need an up-to-date web browser. 
</p>
<p>
For Bank of Canada and participating Government of Canada information professionals you will have to go through your IT department, and not all software may be available for you. However, we have included the set-up instructions because alternatively, you may choose to bring a personal laptop with Git and OpenRefine already set up if you prefer.
</p>
<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>

<div id="git"> {% comment %} Start of 'Git' section. GitHub browser compatability
  is given at https://help.github.com/articles/supported-browsers/{% endcomment %}
  <h3>Git</h3>
  <p>
    Git is a version control system that lets you track who made changes
    to what when and has options for easily updating a shared or public
    version of your code
    on <a href="https://github.com/">github.com</a>. You will need a
    <a href="https://help.github.com/articles/supported-browsers/">supported
    web browser</a>.
  </p>
  <p>
    You will need an account at <a href="https://github.com/">github.com</a>
    for parts of the Git lesson. Basic GitHub accounts are free. We encourage
    you to create a GitHub account if you don't have one already.
    Please consider what personal information you'd like to reveal. For
    example, you may want to review these
    <a href="https://help.github.com/articles/keeping-your-email-address-private/">instructions
      for keeping your email address private</a> provided at GitHub.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#git-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#git-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#git-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="git-windows">
        <p>
          Git should be installed on your computer as part of your Bash
          install (described above).
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="git-macos">
        <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>
        <p>
          <strong>For OS X 10.9 and higher</strong>, install Git for Mac
          by downloading and running the most recent "mavericks" installer from
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.
          Because this installer is not signed by the developer, you may have to
          right click (control click) on the .pkg file, click Open, and click
          Open on the pop up window. 
          After installing Git, there will not be anything in your <code>/Applications</code> folder,
          as Git is a command line program.
          <strong>For older versions of OS X (10.5-10.8)</strong> use the
          most recent available installer labelled "snow-leopard"
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="git-linux">
        <p>
          If Git is not already available on your machine you can try to
          install it via your distro's package manager. For Debian/Ubuntu run
          <code>sudo apt-get install git</code> and for Fedora run
          <code>sudo dnf install git</code>.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'Git' section. {% endcomment %}

<div id="openrefine"> {% comment %} Start of 'OpenRefine' section. {% endcomment %}
  <h3>OpenRefine</h3>
  <p>
    For this lesson you will need <em>OpenRefine</em> and a
    web browser. <em>Note:</em> this is a Java program that runs on your machine (not in the cloud).
    It runs inside a web browser, but no web connection is needed.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#openrefine-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#openrefine-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#openrefine-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="openrefine-windows">
        <p>
          Check that you have either the Firefox or the Chrome browser installed and set as your default browser.
          <strong>OpenRefine runs in your default browser.</strong>
          It will not run correctly in Internet Explorer.
        </p>
        <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a></p>
        <p>Create a new directory called OpenRefine.</p>
        <p>Unzip the downloaded file into the OpenRefine directory by right-clicking and selecting "Extract ...". </p>
        <p>Go to your newly created OpenRefine directory.</p>
        <p>Launch OpenRefine by clicking <code>openrefine.exe</code> (this will launch a command prompt window, but you can ignore that - just wait for OpenRefine to open in the browser).</p>
        <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="openrefine-macos">
        <p>Check that you have either the Firefox or the Chrome browser installed and set as your default browser. <strong>OpenRefine runs in your default browser.</strong> It may not run correctly in Safari.</p>
        <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a>.</p>
        <p>Create a new directory called OpenRefine.</p>
        <p>Unzip the downloaded file into the OpenRefine directory by double-clicking it.</p>
        <p>Go to your newly created OpenRefine directory.</p>
        <p>Launch OpenRefine by dragging the icon into the Applications folder.</p>
        <p>Use <code>Ctrl-click/Open ... </code> to launch it.</p>
        <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="openrefine-linux">
        <p>Check that you have either the Firefox or the Chrome browser installed and set as your default browser. <strong>OpenRefine runs in your default browser.</strong></p>
        <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a>.</p>
        <p>Make a directory called OpenRefine.</p>
        <p>Unzip the downloaded file into the OpenRefine directory.</p>
        <p>Go to your newly created OpenRefine directory.</p>
        <p>Launch OpenRefine by entering <code>./refine</code> into the terminal within the OpenRefine directory.</p>
        <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'OpenRefine' section. {% endcomment %}
