---
layout: page
permalink: /personal/
title: personal
nav: true
nav_order: 6
---

<h2>A name</h2>

My full Vietnamese name is **Võ Khánh An**. Vietnamese names are written family name first, so Võ is my family name and An is my given name. The name was a spontaneous thought of my father's during a naming discussion with my mother. But An does carry meaning: it means *peaceful* in Vietnamese.

<hr>

<h2>Places I have been</h2>

*Sai Gon* and *Ca Mau* in Vietnam, *Daejeon* in South Korea, and *Abu Dhabi* in the UAE are places I have called home, at least for a while.

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.css" crossorigin=""/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/flag-icons@7.2.3/css/flag-icons.min.css" crossorigin=""/>
<script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.js" crossorigin=""></script>

<div id="travel-map" style="height: 480px; border-radius: 8px; margin: 1.5rem 0; z-index: 0;"></div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var map = L.map("travel-map", {
    center: [25, 75],
    zoom: 2,
    scrollWheelZoom: false
  });

  L.tileLayer("https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png", {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors &copy; <a href="https://carto.com/">CARTO</a>',
    subdomains: "abcd",
    maxZoom: 19
  }).addTo(map);

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
    { name: "Thailand", lat: 12.9236, lng: 100.8825, note: "Jomtien beach at Pattaya, a relaxing time." }
  ];

  places.forEach(function (p) {
    L.circleMarker([p.lat, p.lng], style)
      .addTo(map)
      .bindPopup("<strong>" + p.name + "</strong><br>" + p.note);
  });
});
</script>

