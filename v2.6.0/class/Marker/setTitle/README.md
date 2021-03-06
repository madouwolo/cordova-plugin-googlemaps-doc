:green_heart: This is the latest document.

# marker.setTitle()

Change the marker title

```
marker.setTitle(title);
```

## Parameters

name           | type     | description
---------------|----------|---------------------------------------
title          | string   | new title
------------------------------------------------------------------

## Demo code

```html
<div id="map_canvas"></div>
```

```js
var div = document.getElementById("map_canvas");
var map = plugin.google.maps.Map.getMap(div);

// Add a marker
var marker = map.addMarker({
  'position': {
    lat: 0,
    lng: 0
  },
  'title': "Click me!"
});

// Show the infoWindow
marker.showInfoWindow();

// Catch the MARKER_CLICK event
marker.on(plugin.google.maps.event.INFO_CLICK, function() {

  // Change the marker title
  marker.setTitle("Clicked!");

  // Redraw (reopen) the infoWindow.
  marker.showInfoWindow();

});
```

![](image.gif)
