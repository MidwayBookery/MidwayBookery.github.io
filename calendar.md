---
title: Calendar
permalink: "/calendar/"
layout: default
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/fullcalendar@5.5.0/main.min.css">
<script src="https://cdn.jsdelivr.net/npm/fullcalendar@5.5.0/main.min.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script>
  document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('calendar');
    var calendar = new FullCalendar.Calendar(calendarEl, {
      contentHeight: '75vh',
      eventColor: '#750384',
      googleCalendarApiKey: 'AIzaSyC4VtQc4DsrecgLxAJQZOWDYezGHflNZy0',
      events: 'qhkd08skbm49q2ole01ountaoo@group.calendar.google.com',
      eventClick: function(info) {
        info.jsEvent.preventDefault();
        window.open(info.event.url, 'gcalevent');
      },
      headerToolbar: {
        start: '',
        center: 'title',
        end: ''
      }
    });
    calendar.render();
  });
</script>
<div class="topnav-spacer"></div>
<div class="content" style="margin:2em;">
  <div id='calendar'></div>
</div>