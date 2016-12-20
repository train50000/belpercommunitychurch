---
layout: page
title: Calendar
description: Gatherings and events
permalink: /calendar/
order: 4
---
<table class="dataTable">
    <thead>
    <tr>
        <th>Category</th>
        <th>Title</th>
        <th>Description</th>
        <th>Date</th>
        <th>Time</th>
    </tr>
</thead>
<tbody>
{% for event in site.events %}
    {% for date in event.dates %}
    <tr>
        <td>{{ event.category }}</td>
        <td>{{ event.title }}</td>
        <td>{{ event.description }}</td>
        <td>{{ date.date | date: '%-d %B %Y'}}</td>
        <td>{{ date.start }} - {{ date.finish }}</td>
    </tr>
{% endfor %}
{% endfor %}
</tbody>
</table>