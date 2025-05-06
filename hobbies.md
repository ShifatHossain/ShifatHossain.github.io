---
layout: page
title: Hobbies
permalink: /hobbies/
---


<!-- # Featured Courses Taken -->

<script data-goatcounter="https://shifathsn.goatcounter.com/count" async src="https://gc.zgo.at/count.js"></script>

# 🌍 Places I Visited

<canvas id="mapChart" width="800" height="450"></canvas>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://cdn.jsdelivr.net/npm/chartjs-chart-geo@4.2.1/build/index.umd.min.js"></script>

<script>
  const visitedPlaces = [
    { latitude: 23.8103, longitude: 90.4125, name: "Dhaka" },
    { latitude: 40.7128, longitude: -74.0060, name: "New York" },
    { latitude: 48.8566, longitude: 2.3522, name: "Paris" }
  ];

  fetch('https://cdn.jsdelivr.net/npm/chartjs-chart-geo@4.2.1/world.geo.json')
    .then(res => res.json())
    .then(world => {
      const ctx = document.getElementById("mapChart").getContext("2d");
      new Chart(ctx, {
        type: "bubbleMap",
        data: {
          labels: visitedPlaces.map(p => p.name),
          datasets: [{
            label: "Visited",
            data: visitedPlaces.map(p => ({
              latitude: p.latitude,
              longitude: p.longitude,
              r: 5
            })),
            backgroundColor: "rgba(200, 0, 0, 0.7)"
          }]
        },
        options: {
          plugins: {
            legend: { display: false },
            tooltip: {
              callbacks: {
                label: ctx => ctx.chart.data.labels[ctx.dataIndex]
              }
            }
          },
          scales: {
            xy: {
              projection: "equalEarth"
            }
          },
          geo: {
            map: world
          }
        }
      });
    })
    .catch(error => {
      console.error("Failed to load map or render chart:", error);
    });
</script>



# 🌍 Travel Gallery

<style>
  .gallery-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
  }

  .gallery-grid img {
    width: 200px;
    height: auto;
    border-radius: 6px;
    transition: transform 0.2s ease-in-out;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  }

  .gallery-grid img:hover {
    transform: scale(1.05);
  }

  @media (max-width: 600px) {
    .gallery-grid img {
      width: 100%;
    }
  }
</style>

<div class="gallery-grid">
  <img src="https://placehold.co/300x200?text=Paris" alt="Paris">
  <img src="https://placehold.co/300x200?text=Tokyo" alt="Tokyo">
  <img src="https://placehold.co/300x200?text=New+York" alt="New York">
  <img src="https://placehold.co/300x200?text=Dhaka" alt="Dhaka">
  <img src="https://placehold.co/300x200?text=Istanbul" alt="Istanbul">
  <img src="https://placehold.co/300x200?text=Seoul" alt="Seoul">
</div>

