---
layout: event
title: Event Calendar
permalink: /calendar/
---

<script src="{{"/assets/js/jquery.min.js" | prepend: site.baseurl}}"  
integrity="sha256-hVVnYaiADRTO2PzUGmuLJr8BLUSjGIZsDYGmIJLv2b8="  crossorigin="anonymous"></script>
<script type="text/javascript" src="{{"/assets/js/gcal.min.js" | prepend: site.baseurl}}" ></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.2.0/fullcalendar.min.js"></script>
<link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.2.0/fullcalendar.min.css">
<link rel="stylesheet" media="print" href="//cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.2.0/fullcalendar.print.css">


<script>
$(document).ready(function() {
    $('#calendar').fullCalendar({
        googleCalendarApiKey: 'AIzaSyDMSiavMkwBvw9Pl-WP_NMYwQ4Rgb7v_rI',
        events: {
            googleCalendarId: '2dg9b3ten4cc6ef752hpfvbbp8@group.calendar.google.com'
        }
    });
});

</script>

<!--
{% for event in site.events %}
{{event.title}} {{event.event_date}}<br/>
{% endfor %}
-->
<div id="calendar"></div>
