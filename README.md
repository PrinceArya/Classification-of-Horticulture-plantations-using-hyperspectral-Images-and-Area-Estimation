# Classification-of-Horticulture-plantations-using-hyperspectral-Images-and-Area-Estimation.


<h1>Content:</h1>
<a href="#obj" >1. Objective</a><br>
<a href="#over" >2.Preprocessing </a><br>
<a href="#model" >3. Model Architecture</a><br>
<a href="#loss" >4. Loss Function</a><br>
<a href="#res" >5. Result</a><br>
<a href="#app" >6. Appendix</a><br>
<hr>
<h1 id="obj">1. Objective:</h1>

<strong>The main objective of this project is to 
  <ul>
    <li>Classify Horticulture plantations using Hyperspectral Images.</li>
    <li>Generation of crop map for the selected horticulture crops in the study areas and area estimation.</li>
  </ul>
</strong>
<br>


<h1 id="obj">2.Preprocessing:</h1>

Let’s denote HSI by D which has dimension (w, h, d), where ‘w’ is the width, ‘h’ is the
height and ‘d’ is the number of spectral bands in HSI. In order to remove the spectral
redundancy in HSI data we apply PCA on its spectral bands. After application of PCA new
dimension that we obtained is given by (w, h, dnew). Then we pad the boundary of HSI with
zero with margin = (patch_size-1)/2. Padded image is then divided into small overlapping
patches of dimension (patch size, patch size, dnew). The label of the patched image is governed
by label of the cantered pixel

