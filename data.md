---
layout: page
title: Plant List
---

<table id="csp-table">
    <thead>
        <tr>
            <td>Name</td>
            <td>Country</td>
            <td>Status</td>
            <td>Year operational</td>
            <td>Technology</td>
            <td>Capacity [MW]</td>
            <td>Storage capacity [h]</td>
            <td>Remuneration [$/kWh]</td>
            <td>Location</td>
        </tr>
    </thead>
    <tbody>
    {% for plant in site.data.csp-guru %}
        <tr>
            <td>{{ plant.Power_station }}</td>
            <td>{{ plant.Country }}</td>
            <td>{{ plant.Status }}</td>
            <td>{{ plant.Year_operational }}</td>
            <td>{{ plant.Technology }}</td>
            <td>{{ plant.Capacity_MW }}</td>
            <td>{{ plant.Storage_capacity_hours }}</td>
            <td>
            {%- if plant.Remuneration_USD2020_per_kWh_deflated -%}
                {{ plant.Remuneration_USD2020_per_kWh_deflated | round: 2}}
            {%- else -%}
                {{ plant.Remuneration_USD2020_per_kWh_deflated }}
            {%- endif -%}
            </td>
            <td>
            {%- if plant.Location_coordinates -%}
                <a href="https://www.google.com/maps/@?api=1&map_action=map&zoom=15&basemap=satellite&center={{ plant.Location_coordinates }}">
                Show
                </a>
            {%- endif -%}
            </td>
        </tr>
    {% endfor %}
    </tbody>
</table>

<script type="text/javascript">
    $(document).ready( function () {
        $('#csp-table').DataTable({
            "paging": false,
            "order": [[ 3, "desc" ]]
        });
    } );
</script>
