---
layout: event
title: Event Calendar
permalink: /calendar/
---

<meta charset='utf-8' />
<link href="{{ "/assets/css/fullcalendar.min.css" | prepend: site.baseurl }}" rel="stylesheet" />
<link href="{{ "/assets/css/fullcalendar.print.min.css" | prepend: site.baseurl }}" rel="stylesheet" media="print" />
<script src="{{ "/assets/js/moment.min.js" | prepend: site.baseurl }}"></script>
<script src="{{ "/assets/js/jquery.min.js" | prepend: site.baseurl }}"></script>
<script src="{{ "/assets/js/fullcalendar.min.js" | prepend: site.baseurl }}"></script>
<script src="{{ "/assets/js/gcal.min.js" | prepend: site.baseurl }}"></script>
<script>

  $(document).ready(function() {

    $('#calendar').fullCalendar({

      header: {
        left: 'prev,next today',
        center: 'title',
        right: 'month,listYear'
      },

      googleCalendarApiKey: '{{ site.google.api_key }}',

      events: {
          googleCalendarId: '{{ site.google.calendar_id }}'
      },

      eventClick: function(event) {
        // opens events in a popup window
        window.open(event.url, 'gcalevent', 'width=700,height=600');
        return false;
      },

    });

  });

</script>

<div id='calendar'></div>
