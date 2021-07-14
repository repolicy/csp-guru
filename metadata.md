---
layout: page
title: Metadata
---

{% assign version = site.data.datapackage["version"] %}
{% assign attributes = site.data.datapackage["resources"][0]["schema"]["fields"] %}
{% assign contributors = site.data.datapackage["contributors"] %}

The version {{ version }} of the CSP.guru dataset has been created by the following people:

<ul>
    {% for contributor in contributors %}
    <li>{{ contributor.title }}</li>
    {% endfor %}
</ul>

It contains the following attributes for each CSP plant:

<table>
    <thead>
        <tr>
            <td>Attribute</td>
            <td>Description</td>
        </tr>
    </thead>
    <tbody>
    {% for attribute in attributes %}
        <tr>
            <td>{{ attribute.name | truncate: 60, "..." }}</td>
            <td>{{attribute.description}}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>
