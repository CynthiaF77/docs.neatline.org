---
layout: default
---

# Neatline Editor: Styles Tab

## At a glance

- Click the **Styles** tab in the editor to edit higher-level settings for your exhibit
- These fields define over-all view settings for your exhibit.
- You can return to these settings at any time to make changes.
- Jump to:
    * [Stylesheet Overview](#stylesheet-overview)
    * [Default Map Focus](#default-map-focus) 
    * [Default Map Zoom](#default-map-focus)
    * [Restricted Map Extent](#restricted-map-extent) 
    * [Minimum Map Zoom](#minimum-map-zoom)
    * [Maximum Map Zoom](#maximum-map-zoom)

## Styles Tab

## Stylesheet Overview

![Screenshot of stylesheet](images/stylesheet.png)

The Neatline Stylesheet is a code editor that uses a simplified, Neatline-inflected dialect of CSS to perform bulk updates on large groups of related records clustered together by tags (see [Editing Record Groups](style-tab-groups.html)). Instead of manually changing individual records, one by one, the stylesheet allows for updates to made automatically to grouped records. Neatline CSS treats [record tags](style-tab-groups.html) as "classes", which allows for the use of a set of style properties to be defined in the stylesheet. 

For example, if you have a set of records tagged with the year `2012`, and want to make changes to their [fill color](style-tab-colors.html), include the following in the stylesheet:

{% highlight css %}
.2012 {
fill-color: #08c;
}
{% endhighlight %}

Instead of regular CSS rules, the Neatline stylesheet uses a specific set of rules that directly relate to the fields in the **Record Style Tab**, listed here:
- `widgets`
- `presenter`
- `fill-color`
- `fill-color-select`
- `stroke-color`
- `stroke-color-select`
- `fill-opacity`
- `fill-opacity-select`
- `stroke-opacity`
- `stroke-opacity-select`
- `stroke-width`
- `point-radius`
- `zindex`
- `weight`
- `start-date`
- `end-date`
- `after-date`
- `before-date`
- `point-image`
- `wms-address`
- `wms-layers`
- `min-zoom`
- `max-zoom`
- `map-focus`
- `map-zoom`

For a more detailed information, see [Using Neatline Stylesheets](neatline-stylesheets.html).

## Default Map Focus and Default Map Zoom {#default-map-focus}

The **Default Map Focus** and the **Default Map Zoom** are the settings that determine the initial view of your exhibit, that is, the view seen when first opening the exhibit (in both the editor and in the [Public View](managing-exhibits.html#public-view)).

A simple way to use this setting is to move the map to the exact location and zoom level, using your mouse to drag and zoom, or by using the navigation icons in the left-top corner of the map. Once you find your view, click "Use Current Viewport as Default" and the data will auto-fill. Click the blue "Save" button at the bottom of the panel to save the settings. 

![Screenschot of default map zoom and focus](images/editor-map-focus.png)

## Restricted Map Extent

This setting controls how far your map or image extends, effectively restricting a viewer's ability to change the exhibit's focus. **Restricted Map Extent** does not control zoom levels (a viewer can still zoom in and out as far as allowed). This setting can be particularly useful if your exhibit has a specifc geographic setting, and you'd like to keep viewers within a region, and keep from getting lost elsewhere on the world map. 

Like the **Default Map Focus** and **Default Map Zoom**, this setting can be auto-filled by clicking "Use Current Map Bounds as Max Extent," creating set boundaries for your exhibit. Click the blue "Save" button at the bottom of the panel to save the setting.

![Screenshot of Restricted Map Extent Field](images/editor-map-extent.png)

## Minimum Map Zoom

This setting controls how far you can "zoom out" in your exhibit. Like the **Restricted Map Extent**, this setting is useful for creating boundaries for your exhibit, and can make the viewer's experience better by limiting where they can move the map, effectively keeping the focus on the setting of your exhibit.

Adjust your map to the furthest zoom level you want a viewer to experience, and click "Set Minimum Zoom to Current" to set. Click the blue "Save" button at the bottom of the panel to save the setting.

![Screenshot of Minimum Map Zoom Field](images/editor-min-zoom.png)

## Maximum Map Zoom

Similar to **Minimum Map Zoom**, this setting controls how far a viewer can "zoom in" on your exhibit. To set, adjust your map to the closest, "zoomed-in" view you want a viewer to experience, and click "Set Maximum Zoom to Current." Click the blue "Save" button at the bottom of the panel to save the setting.

![Screenshot of Max Map Zoom Field](images/editor-max-zoom.png)

**Related:** [Editor Overview](editor-overview.html), [Using Neatline Stylesheets](neatline-stylesheets.html), [Editing Record Groups](style-tab-groups.html), [Editing Record Visibility](style-tab-visibility.html)
