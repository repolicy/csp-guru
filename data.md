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
            <td>Technology</td>
            <td>Capacity [MW]</td>
            <td>Country</td>
        </tr>
    </thead>
    <tbody>
    {% for plant in site.data.csp-guru %}
        <tr>
            <td>{{ plant.Title }}</td>
            <td>{{ plant.Year_operational }}</td>
            <td>{{ plant.Status }}</td>
            <td>{{ plant.Technology }}</td>
            <td>{{ plant.Capacity }}</td>
            <td>{{ plant.Country }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>
