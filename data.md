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
            <td>LCOE [USD/kWh]</td>
            <td>Remuneration [USD/kWh]</td>
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
            <td>{{ plant.Storage_capacity_h }}</td>
            <td>{{ plant.LCOE_5_25_USD2018_per_kWh | round: 2 | replace: "0.0", ""}}</td>
            <td>{{ plant.Remuneration_USD2018_per_kWh_deflated | round: 2 | replace: "0.0", ""}}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>

<script type="text/javascript">
    $(document).ready( function () {
        $('#csp-table').DataTable({
            "paging": false,
        });
    } );
</script>
