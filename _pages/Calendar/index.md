---
layout: page
title: Calendar
description: Events and meetings
permalink: /calendar/
order: 4
---

<section id="contact">
     <div class="container">
       <div class="row">
         <div class="col-md-12">
           <div class="title-area">
              <h2 class="title">{{ page.title }}</h2>
              <span class="line"></span>
                <iframe src="https://calendar.google.com/calendar/embed?showTitle=0&amp;showTabs=0&amp;showCalendars=0&amp;height=600&amp;wkst=1&amp;bgcolor=%23FFFFFF&amp;src=ig8ap1u67tkqvlh8hejhfdkjek%40group.calendar.google.com&amp;color=%232952A3&amp;ctz=Europe%2FLondon" style="border-width:0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
                </div>
        </div>
        </div>
    </div>
</section>

=======
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
