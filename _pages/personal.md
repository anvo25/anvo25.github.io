---
layout: page
permalink: /personal/
title: miscellaneous
nav: true
nav_order: 6
---

<h2>a name</h2>

My full Vietnamese name is **Võ Khánh An**. Vietnamese names are written family name first, so Võ is my family name and An is my given name. The name was a spontaneous thought of my father's during a naming discussion with my mother. That said, *An* does carry meaning: it means _peaceful_ in Vietnamese.

<hr>

<h2>places i have been</h2>

_Sai Gon_ &amp; _Ca Mau_ <span class="fi fi-vn" role="img" aria-label="Vietnam" title="Vietnam" style="vertical-align: -0.1em; margin-left: 0.15em;"></span>, _Daejeon_ <span class="fi fi-kr" role="img" aria-label="South Korea" title="South Korea" style="vertical-align: -0.1em; margin-left: 0.15em;"></span>, _Abu Dhabi_ <span class="fi fi-ae" role="img" aria-label="United Arab Emirates" title="United Arab Emirates" style="vertical-align: -0.1em; margin-left: 0.15em;"></span>, and _Ann Arbor_ <span class="fi fi-us" role="img" aria-label="United States" title="United States" style="vertical-align: -0.1em; margin-left: 0.15em;"></span> are places I have called <span style="color: var(--global-theme-color); font-weight: 500; white-space: nowrap;">home <i class="fa-solid fa-house-chimney fa-sm"></i></span>, at least for a while.

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.css" crossorigin=""/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/flag-icons@7.2.3/css/flag-icons.min.css" crossorigin=""/>
<script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.js" crossorigin=""></script>

<div id="travel-map" style="height: 480px; border-radius: 8px; margin: 1.5rem 0; z-index: 0;"></div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var map = L.map("travel-map", {
    center: [25, 90],
    zoom: 3,
    scrollWheelZoom: true,
    // let the map wrap around the globe: pan east/west past the edge and the
    // world (markers included) comes back around instead of running out.
    worldCopyJump: true
  });

  // Keyless basemaps. Esri's light gray canvas splits the map into a base layer
  // and a separate labels layer, so place names need both. If Esri ever stops
  // serving, fall back to standard OpenStreetMap tiles (labels already baked in).
  var esri = "https://server.arcgisonline.com/ArcGIS/rest/services/Canvas/";

  var base = L.tileLayer(esri + "World_Light_Gray_Base/MapServer/tile/{z}/{y}/{x}", {
    attribution: 'Tiles &copy; <a href="https://www.esri.com/">Esri</a>',
    maxZoom: 16
  }).addTo(map);
  base.setZIndex(1);

  var labels = L.tileLayer(esri + "World_Light_Gray_Reference/MapServer/tile/{z}/{y}/{x}", {
    maxZoom: 16
  }).addTo(map);
  labels.setZIndex(2);

  var usedFallback = false;
  base.on("tileerror", function () {
    if (usedFallback) return;
    usedFallback = true;
    map.removeLayer(base);
    map.removeLayer(labels);
    L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
      attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
      maxZoom: 19
    }).addTo(map);
  });

  var style = {
    radius: 9,
    fillColor: "#4a90d9",
    color: "#2c6fad",
    weight: 2,
    opacity: 1,
    fillOpacity: 0.8
  };

  var places = [
    { name: "Vietnam", lat: 10.8231, lng: 106.6297, note: "Born in Sai Gon, raised in Ca Mau." },
    { name: "South Korea", lat: 36.351, lng: 127.384, note: "MS at KAIST in Daejeon." },
    { name: "Japan", lat: 35.6762, lng: 139.6503, note: "Visited Tokyo for a workshop." },
    { name: "UAE", lat: 24.4539, lng: 54.3773, note: "Research Engineer at MBZUAI in Abu Dhabi." },
    { name: "Canada", lat: 49.2827, lng: -123.1207, note: "9 days in Vancouver at ICML." },
    { name: "Oman", lat: 23.5880, lng: 58.3829, note: "Muscat, where desert meets sea and mountainous land." },
    { name: "Thailand", lat: 12.9236, lng: 100.8825, note: "Jomtien beach at Pattaya, a relaxing time." },
    { name: "United States", lat: 42.2808, lng: -83.7430, note: "PhD at the University of Michigan in Ann Arbor." }
  ];

  places.forEach(function (p) {
    L.circleMarker([p.lat, p.lng], style)
      .addTo(map)
      .bindPopup("<strong>" + p.name + "</strong><br>" + p.note);
  });
});
</script>
