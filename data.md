---
layout: page
title: Plant List
---

<table id="csp-table">
    <thead>
        <tr>
            <td>Name</td>
            <td>Country</td>
            <td>Year</td>
            <td>Technology</td>
            <td>Capacity [MW]</td>
            <td>Storage capacity [h]</td>
            <td>LCOE [$/kWh]</td>
            <td>Remuneration [$/kWh]</td>
            <td>Location</td>
        </tr>
    </thead>
    <tbody>
    {% for plant in site.data.csp-guru %}
        <tr>
            <td>{{ plant.Power_station }}</td>
            <td>{{ plant.Country }}</td>
            <td>{{ plant.Year_operational }}</td>
            <td>{{ plant.Technology }}</td>
            <td>{{ plant.Capacity_MW }}</td>
            <td>{{ plant.Storage_capacity_hours }}</td>
            <td>
            {%- if plant.LCOE_5_25_USD2020_per_kWh -%}
                {{ plant.LCOE_5_25_USD2020_per_kWh | round: 2}}
            {%- else -%}
                {{ plant.LCOE_5_25_USD2020_per_kWh }}
            {%- endif -%}
            </td>
            <td>
            {%- if plant.Remuneration_USD2020_per_kWh_deflated -%}
                {{ plant.Remuneration_USD2020_per_kWh_deflated | round: 2}}
            {%- else -%}
                {{ plant.Remuneration_USD2020_per_kWh_deflated }}
            {%- endif -%}
            </td>
            <td>
            {%- if plant.Location_coordinates -%}
                <a href="https://www.google.com/maps/@?api=1&map_action=map&center={{ plant.Location_coordinates }}" &zoom=13&basemap=satellite&target="_blank">
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
            "order": [[ 2, "desc" ]]
        });
    } );
</script>
