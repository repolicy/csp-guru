---
layout: page
title: Plant List
---

<table>
    <thead>
        <tr>
            <td>Name</td>
            <td>Year operational</td>
            <td>Status</td>
            <td>Country</td>
        </tr>
    </thead>
    <tbody>
    {% for plant in site.data.csp-guru-2016-08-30 %}
        <tr>
            <td> <a href="./plant/{{ plant.Title | replace: " ", "-" }}.html">{{ plant.Title }}</a></td>
            <td>{{ plant.Year_operational }}</td>
            <td>{{ plant.Status }}</td>
            <td>{{ plant.Country }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>
