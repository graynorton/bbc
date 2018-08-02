---
layout: default
title: Baja Bronco Registry
permalink: /registry.html
---
# Baja Bronco Registry

Here's a list of all known Baja Broncos. If you own or know of one that isn't listed here,
please [let me know](mailto:andrew@bajabronco.com).

<table>
    <tr>
        <th>VIN</th>
        <th>Owner</th>
        <th>Location</th>
        <th>Email</th>
    </tr>
    {% for year in site.data.registry %}
        <tr>
            <th colspan="4">
                Model Year {{ year.modelYear }}
            </th>
        </tr>
        {% for dso in year.dso %}
            <tr>
                <th colspan="4">
                    {{ dso.dso }}
                </th>
            </tr>
            {% for vehicle in dso.vehicle %}
                <tr>
                    <td>
                        {{ vehicle.vin }}
                    </td>
                    <td>
                        {{ vehicle.owner }}
                    </td>
                    <td>
                        {{ vehicle.location }}
                    </td>
                    <td>
                        {{ vehicle.email }}
                    </td>
                </tr>
            {% endfor %}
        {% endfor %}
    {% endfor %}
</table>