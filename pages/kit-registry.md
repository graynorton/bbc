---
layout: default
title: Baja Bronco Registry
permalink: /kit-registry.html
---
# Kit Baja Bronco Registry

Welcome to the Kit Baja registry. This registry is a list of all known "Kit Baja Broncos". There are a couple of ways Kit Bajas or Stroppe Modified Broncos came to be. The trucks below are verified and recognized by Baja Broncos Unlimited as legitimate Kit Bajas, based on documentation, photos, and in-person examination by Andrew Norton. If you own or know of one that isn't listed here, please email us and we can discuss the steps necessary to add it to the Registry.

<table>
    <tr>
        <th>VIN</th>
        <th>DSO</th>
        <th>Color</th>
        <th>Owner</th>
        <th>Location</th>
        <th>Email</th>
    </tr>
    {% for year in site.data.kit_registry %}
        <tr>
            <th colspan="6">
                Model Year {{ year.modelYear }}
            </th>
        </tr>
        {% for vehicle in year.vehicle %}
            <tr>
                <td>
                    {{ vehicle.vin }}
                </td>
                <td>
                    {{ vehicle.dso }}
                </td>
                <td>
                    {{ vehicle.color }}
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
</table>