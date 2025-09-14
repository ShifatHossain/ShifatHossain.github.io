---
layout: page
title: Publications
permalink: /publications/
---


<!-- # Publications -->
Follow my Researchgate profile [here](http://www.researchgate.net/profile/Shifat_Hossain).

Follow my Google Scholar profile [here](https://scholar.google.com/citations?user=p-dnT8MAAAAJ&hl=en).

<!-- <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js"></script> -->


<!-- <div id='temp'></div>
<script>
    $.getJSON("http://cse.bth.se/~fer/googlescholar-api/googlescholar.php?user=p-dnT8MAAAAJ",function(data){

    });
</script> -->

<script data-goatcounter="https://shifathsn.goatcounter.com/count" async src="https://gc.zgo.at/count.js"></script>

## Citation Data

<div id="metrics" style="font-size: 1.1em; margin-bottom: 1em;">
  <p><strong>Total Citations:</strong> <span id="totalCitations">Loading...</span></p>
  <p><strong>h-index:</strong> <span id="hIndex">Loading...</span></p>
  <p><strong>Last Updated:</strong> <span id="lastUpdated">Loading...</span></p>
</div>

<div style="width: 100%; max-width: 600px;">
  <canvas id="citationsChart"></canvas>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
  const API_URL = "https://prinetapi.mooo.com/api/citations";

  fetch(API_URL)
    .then(res => res.json())
    .then(data => {
      // Set citation metrics
      const citationCounts = Object.values(data.citations);
      const years = Object.keys(data.citations);

      const total = citationCounts.reduce((a, b) => a + b, 0);
      document.getElementById("totalCitations").textContent = total;
      document.getElementById("hIndex").textContent = data.h_index;
      document.getElementById("lastUpdated").textContent = new Date(data.last_updated).toLocaleString();

      // Render Chart
      const ctx = document.getElementById('citationsChart').getContext('2d');
      new Chart(ctx, {
        type: 'bar',
        data: {
          labels: years,
          datasets: [{
            label: 'Citations per Year',
            data: citationCounts,
            backgroundColor: 'rgba(100, 100, 100, 0.8)',
            borderColor: 'rgba(50, 50, 50, 1)',
            borderWidth: 1
          }]
        },
        options: {
          responsive: true,
          scales: {
            y: {
              beginAtZero: true,
              ticks: {
                precision: 0
              }
            }
          },
          plugins: {
            legend: {
              display: false
            }
          }
        }
      });
    })
    .catch(err => {
      document.getElementById("metrics").innerHTML =
        "<p style='color:red;'>Failed to load citation data. Please check if the API server is running.</p>";
      document.getElementById("citationsChart").outerHTML = "";
      console.error("Error fetching data:", err);
    });
</script>



## Patents
8.	Ki-Doo Kim, Tae-Ho Kwon, and **Shifat Hossain**, “Non-invasive biosignal measurement device and method based on skin effect removal,” KR Patent: KR102595803B1. Issued: October 30, 2023. [Online](https://patents.google.com/patent/KR102595803B1/en)  
7.	Ki-Doo Kim, Tae-Ho Kwon, and **Shifat Hossain**, “Non-invasive biosignal measurement device based on skin effect removal,” KR Patent: KR102591405B1. Issued: October 19, 2023. [Online](file:///s://patents.google.com/patent/KR102591405B1/en)  
6.	Ki-Doo Kim, Tae-Ho Kwon, and **Shifat Hossain**, “Method and Apparatus for Non-Invasive Measurement of Glycated Hemoglobin using Monte Carlo Simulation,” KR Patent: KR102439240B1. Issued: September 2, 2022. [Online](https://patents.google.com/patent/KR102439240B1/en)  
5\.	Ki-Doo Kim and **Shifat Hossain**, “Noninvasive HbA1c Measurement System and Method using Monte-Carlo Simulation,”  
    &emsp;- KR patent: KR102403577B1, Issued: May 31, 2022 [Online](https://patents.google.com/patent/KR102403577B1/en)  
    &emsp;- PCT application: WO2022045822A1, Published: March 03, 2022 [Online](https://patents.google.com/patent/WO2022045822A1/en)  
    &emsp;- US application: US20240233961A1, Published: June 11, 2024 [Online](https://patents.google.com/patent/US20240233961A1/en)  
4\. Ki-Doo Kim and **Shifat Hossain**, “Noninvasive HbA1c Measurement System and Method Thereof,” KR Patent: KR102482459B1, Issued: December 29, 2022. [Online](https://patents.google.com/patent/KR102482459B1/en)  
3\. Ki-Doo Kim and **Shifat Hossain**, “Noninvasive HbA1c Measurement System using Photon-Diffusion Theory and Method Thereof,” KR Patent: KR102402263B1, Issued: May 27, 2022. [Online](https://patents.google.com/patent/KR102402263B1/en)  
2\. Ki-Doo Kim and **Shifat Hossain**, “System and Method for Non-Invasive Measurement of Glycated Hemoglobin,”  
    &emsp;- PCT Application: WO2021210724A1, Published: October 21, 2021. [Online](https://patents.google.com/patent/WO2021210724A1/en)  
    &emsp;- US Application: US20240225495A1, Published: July 11, 2024. [Online](https://patents.google.com/patent/US20240225495A1/en)  
1\. Ki-Doo Kim and **Shifat Hossain**, “Noninvasive HbA1c Measurement System using the Beer-Lambert law and Method Thereof,” KR Patent: KR102356154B1, Issued: January 28, 2022. [Online](https://patents.google.com/patent/KR102356154B1/en)  


## Journals
15\. T.-H. Kwon, **S. Hossain**, Mrinmoy Sarker Turja, and K.-D. Kim, “Design and Validation of a Monte Carlo Method for the Implementation of Noninvasive Wearable Devices for HbA1c Estimation Considering the Skin Effect,” Micromachines, vol. 15, no. 9, pp. 1067–1067, Aug. 2024, doi: 10.3390/mi15091067.  
14\. C. A. Haque, **S. Hossain**, T.-H. Kwon, H. Kim, and K.-D. Kim, Noninvasive In-Vivo Estimation of Blood-Glucose Concentration Using Beer-Lambert-Based Model, The Korean Institutes of Communications and Information Sciences, vol. 48 (7), pp. 852-867, Jul. 2023.  
13\. **S. Hossain** and K.-D. Kim, “Non-Invasive In Vivo Estimation of HbA1c Using Monte Carlo Photon Propagation Simulation: Application of Tissue-Segmented 3D MRI Stacks of the Fingertip and Wrist for Wearable Systems,” Sensors, vol. 23, no. 1, p. 540, Jan. 2023, doi: 10.3390/s23010540.  
12\. **S. Hossain**, S. Satter, T.-H. Kwon, and K.-D. Kim, “Optical Measurement of Molar Absorption Coefficient of HbA1c: Comparison of Theoretical and Experimental Results,” Sensors, vol. 22, no. 21, p. 8179, Oct. 2022, doi: 10.3390/s22218179.  
11\. S. Sen Gupta, **S. Hossain**, and K.-D. Kim, “Recognize the surrounding: Development and evaluation of convolutional deep networks using gammatone spectrograms and raw audio signals,” Expert Systems with Applications, vol. 200, p. 116998, Aug. 2022, doi: 10.1016/j.eswa.2022.116998.  
10\.	**S. Hossain** and K.-D. Kim, “Noninvasive Estimation of Glycated Hemoglobin In-Vivo Based on Photon Diffusion Theory and Genetic Symbolic Regression Models,” IEEE Transactions on Biomedical Engineering, vol. 69, no. 6, pp. 2053–2064, Jun. 2022, doi: 10.1109/TBME.2021.3135305.  
9\.  M. S. H. Sunny, **S. Hossain**, N. Afroze, M. K. Hasan, E. Hossain, and M. H. Rahman, “Understanding the nonlinear behavior of EEG with advanced machine learning in artifact elimination,” Biomed. Phys. Eng. Express, vol. 8, no. 1, p. 015017, Dec. 2021, doi: 10.1088/2057-1976/ac3f17.  
8\.  **S. Hossain** and K.-D. Kim, “Comparison of Different Wavelengths for Estimating HbA1c and SpO₂ Noninvasively Using Beer-Lambert Law and Photon Diffusion Theory Derived Models,” 한국통신학회논문지, vol. 46, no. 8, pp. 1301–1308, Aug. 2021, doi: 10.7840/kics.2021.46.8.1301.  
7\.  **S. Hossain**, C. A. Haque, and K.-D. Kim, “Quantitative Analysis of Different Multi-Wavelength PPG Devices and Methods for Noninvasive In-Vivo Estimation of Glycated Hemoglobin,” *Applied Sciences*, vol. 11, no. 15, Art. no. 15, Jul. 2021, doi: 10.3390/app11156867.  
6\.	C. A. Haque, **S. Hossain**, T.-H. Kwon, and K.-D. Kim, “Noninvasive In Vivo Estimation of Blood-Glucose Concentration by Monte Carlo Simulation,” *Sensors*, vol. 21, no. 14, Art. no. 14, Jul. 2021, doi: 10.3390/s21144918.  
5\.	S. Sen Gupta, T.-H. Kwon, **S. Hossain**, and K.-D. Kim, “Towards non-invasive blood glucose measurement using machine learning: An all-purpose PPG system design,” *Biomedical Signal Processing and Control*, vol. 68, p. 102706, Jul. 2021, doi: 10.1016/j.bspc.2021.102706.  
4\.	**S. Hossain** and K.-D. Kim, “Estimation of Molar Absorption Coefficients of HbA1c in Near UV-Vis-SW NIR Light Spectrum,” *The Korean Institutes of Communications and Information Sciences*, Jun. 2020.  
3\.	**S. Hossain**, S. S. Gupta, T.-H. Kwon, and K.-D. Kim, “Derivation and Validation of Gray-Box Models to Estimate Noninvasive In-vivo Percentage Glycated Hemoglobin Using Digital Volume Pulse Waveform,” *Scientific Reports*, Jun. 2021, doi: 10.1038/s41598-021-91527-2.  
2\.	S. Sen Gupta, **S. Hossain**, and K.-D. Kim, “HDR-Like Image from Pseudo-Exposure Image Fusion: A Genetic Algorithm Approach,” *IEEE Transactions on Consumer Electronics*, vol. 67, no. 2, pp. 119–128, May 2021, doi: 10.1109/TCE.2021.3066431.  
1\.	P. P. Banik, **S. Hossain**, T.-H. Kwon, H. Kim, and K.-D. Kim, “Development of a Wearable Reflection-Type Pulse Oximeter System to Acquire Clean PPG Signals and Measure Pulse Rate and SpO2 with and without Finger Motion,” *Electronics*, vol. 9, no. 11, Art. no. 11, Nov. 2020, doi: 10.3390/electronics9111905.  



## Conferences

15\.  [**ICMLA’25**] **S. Hossain**, S. Jha, H. Zheng, and R. Ewetz, “Multitask Contrastive Learning using Task-Wise Training and Partitioned Embedding Space”, International Conference on Machine Learning and Applications (ICMLA), 2025.  
14\.  [**ICMLA’25**] F. Rahat, **S. Hossain**, A. Ramanathan, S. Jha, H. Zheng, and R. Ewetz, “Attr-RAG: Attribution-Guided Retrieval-Augmented Generation for Scientific Experiment Design”, International Conference on Machine Learning and Applications (ICMLA), 2025.  
13\.  [**ICMLA’25**] M. R. Ahmed, F. Rahat, **S. Hossain**, S. Jha, and R. Ewetz, “Street2Air: A Framework for Synthesizing Aerial Vehicle Views from Ground Images”, International Conference on Machine Learning and Applications (ICMLA), 2025.  
12\.  [**WACV'25**] F. Rahat, **S. Hossain**, R. Ahmed, S. Jha, and R. Ewetz, “Data Augmentation for Image Classification using Generative AI”, Winter Conference on Applications of Computer Vision (WACV), 2025.  
11\.  [**ICMLA'24**] **S. Hossain**, C. Walker, S. Jha, and R. Ewetz, “Out-of-Distribution Detection for Contrastive Models using Angular Distance Measures”, International Conference on Machine Learning and Applications (ICMLA), 2024.  
10\.  [**ICMLA'24**] F. Rahat, **S. Hossain**, R. Ahmed, and R. Ewetz, “CLE: Context-Aware Local Explanations for High Dimensional Tabular Data”, International Conference on Machine Learning and Applications (ICMLA), 2024.  
9\.  [**AAAI Workshop'23**] **S. Hossain**, R. Ahmed, L. Pullum, S. Jha, and R. Ewetz, “Neuro-Symbolic Representations of 3D Scenes using Universal Scene Description Language”, Workshop on Neuro-Symbolic Learning and Reasoning in the Era of Large Language Models at the Thirty-Eighth AAAI Conference on Artificial Intelligence (AAAI), 2024.  
8\.  [**ICTC'21**] C. A. Haque, **S. Hossain**, T.-H. Kwon, and K.-D. Kim, “Comparison of Different Methods to Estimate Blood Oxygen Saturation using PPG,” in 2021 International Conference on Information and Communication Technology Convergence (ICTC), Oct. 2021, pp. 792–794. doi: 10.1109/ICTC52510.2021.9621142.  
7\.	[**ICTC'20**] S. S. Gupta, **S. Hossain**, C. A. Haque, and K.-D. Kim, “In-Vivo Estimation of Glucose Level Using PPG Signal,” in 2020 International Conference on Information and Communication Technology Convergence (ICTC), Oct. 2020, pp. 733–736. doi: 10.1109/ICTC49870.2020.9289629.  
6\.	[**ICTC'19**] **S. Hossain**, T.-H. Kwon, and K.-D. Kim, “Comparison of Different Wavelengths for Estimating SpO2 Using Beer-Lambert Law and Photon Diffusion in PPG,” in 2019 International Conference on Information and Communication Technology Convergence (ICTC), Oct. 2019, pp. 1377–1379. doi: 10.1109/ICTC46691.2019.8939849.  
5\.	[**ICASERT'19**] Md. S. Haque Sunny, D. Roy Dipta, **S. Hossain**, H. M. Resalat Faruque, and E. Hossain, “Design of a Convolutional Neural Network Based Smart Waste Disposal System,” in 2019 1st International Conference on Advances in Science, Engineering and Robotics Technology (ICASERT), May 2019, pp. 1–5. doi: 10.1109/ICASERT.2019.8934633.  
4\.	[**EICT'17**] S. S. Khan, Md. S. H. Sunny, **M. S. Hossain**, E. Hossain, and M. Ahmad, “Nose tracking cursor control for the people with disabilities: An improved HCI,” in 2017 3rd International Conference on Electrical Information and Communication Technology (EICT), Dec. 2017, pp. 1–5. doi: 10.1109/EICT.2017.8275178.  
3\.	[**EICT'17**] **S. Hossain**, S. S. Khan, M. S. H. Sunny, and M. Ahmad, “Frequency component grouping based sound source extraction from mixed audio signals using spectral analysis,” in 2017 3rd International Conference on Electrical Information and Communication Technology (EICT), Dec. 2017, pp. 1–6. doi: 10.1109/EICT.2017.8275145.  
2\.	[**ICAEE'17**] Md. S. H. Sunny, E. Hossain, T. N. Mimma, and **S. Hossain**, “An autonomous robot: Using ANN to navigate in a static path,” in 2017 4th International Conference on Advances in Electrical Engineering (ICAEE), Sep. 2017, pp. 291–296. doi: 10.1109/ICAEE.2017.8255369.  
1\.	[**IC2IT'17**] Md. K. Hasan, Md. S. H. Sunny, **S. Hossain**, and M. Ahmad, “User Independency of SSVEP Based Brain Computer Interface Using ANN Classifier: Statistical Approach,” in Recent Advances in Information and Communication Technology 2017, Cham, 2018, pp. 58–68. doi: 10.1007/978-3-319-60663-7_6.  

