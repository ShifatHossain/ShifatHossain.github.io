---
layout: page
title: Hobbies
permalink: /hobbies/
---


<!-- # Featured Courses Taken -->

<script data-goatcounter="https://shifathsn.goatcounter.com/count" async src="https://gc.zgo.at/count.js"></script>

# Places I Have Visited

<div style="max-width: 800px;">
  <canvas id="worldMapChart"></canvas>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://cdn.jsdelivr.net/npm/chartjs-chart-geo@4.2.1/build/index.umd.min.js"></script>

<script>
  // Replace these with your own visited places (lat, lon, label)
  const visitedPlaces = [
    { latitude: 28.6139, longitude: 77.2090, name: "New Delhi, India" },
    { latitude: 40.7128, longitude: -74.0060, name: "New York, USA" },
    { latitude: 48.8566, longitude: 2.3522, name: "Paris, France" },
    { latitude: 23.8103, longitude: 90.4125, name: "Dhaka, Bangladesh" }
  ];

  // Load world map topology data
  fetch('https://cdn.jsdelivr.net/npm/chartjs-chart-geo@4.2.1/world.geo.json')
    .then(res => res.json())
    .then(topology => {
      const ctx = document.getElementById("worldMapChart").getContext("2d");

      new Chart(ctx, {
        type: "bubbleMap",
        data: {
          labels: visitedPlaces.map(p => p.name),
          datasets: [{
            label: "Visited Places",
            data: visitedPlaces.map(p => ({
              latitude: p.latitude,
              longitude: p.longitude,
              r: 5
            })),
            backgroundColor: "rgba(200, 0, 0, 0.7)"
          }]
        },
        options: {
          responsive: true,
          showOutline: true,
          showGraticule: true,
          scales: {
            xy: {
              projection: "equalEarth"
            }
          },
          plugins: {
            tooltip: {
              callbacks: {
                label: (ctx) => ctx.chart.data.labels[ctx.dataIndex]
              }
            },
            legend: {
              display: false
            }
          },
          geo: {
            map: topology
          }
        }
      });
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

