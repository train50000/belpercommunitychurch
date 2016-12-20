---
layout: page
title: Calendar
description: Upcoming events and gatherings
permalink: /calendar/
order: 4
---

<table class="dataTable" id="calendar">
    <thead>
    <tr>
        <th>Date</th>
        <th>Category</th>
        <th>Title</th>
        <th>Description</th>
        <th>Time</th>
    </tr>
</thead>
<tbody>
{% for event in site.events %}
    {% for date in event.dates %}
    <tr>
        <td>{{ date.date | date: '%d %B %Y'}}</td>
        <td>{{ event.category }}</td>
        <td>{{ event.title }}</td>
        <td>{{ event.description }}</td>
        <td>{{ date.start }} - {{ date.finish }}</td>
    </tr>
{% endfor %}
{% endfor %}
</tbody>
</table>
