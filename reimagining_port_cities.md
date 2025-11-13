# Minor, (Re)Imagining Port Cities: Understanding Space, Society and Culture

The final part of the minor, focuses on how the Maasboulevard near the Rhijnspoorkade in Rotterdam could evolve into a sustainable and maritime public space for the future. Positioned along the Nieuwe Maas, the site offers a unique interface between the city and the river, a place where movement, ecology, and leisure converge.

<div class="rpc-container">
  <div class="rpc-text"></div>
  <div class="rpc-gallery">
    <img class="zoomable" src="assets/Port Cities 1.jpg" alt="Port Cities concept image 1">
    <img class="zoomable" src="assets/Port Cities 2.jpg" alt="Port Cities concept image 2">
    <img class="zoomable" src="assets/Port Cities 3.jpg" alt="Port Cities concept image 3">
    <img class="zoomable" src="assets/Port Cities 4.jpg" alt="Port Cities concept image 4">
    <img class="zoomable" src="assets/Port Cities 5.jpg" alt="Port Cities concept image 5">
  </div>
</div>
<br>
<div id="lightbox">
  <img id="lightbox-img" src="">
</div>

<style>
header img {
  width: 140px !important;
  height: auto !important;
}  

a {
  color: #b20738;
  font-weight: 400;        
  text-decoration: none;
}

a:hover {
  color: #b20738;
  text-decoration: none;
  font-weight: 400;       
}
  
.rpc-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.zoomable {
  max-width: 220px;           /* pas aan als je ze groter/kleiner wilt */
  cursor: zoom-in;
  transition: transform 0.3s ease;
}

.zoomable.zoomed {
  transform: scale(5);        /* hoeveelheid zoom */
  cursor: zoom-out;
  position: relative;
  z-index: 10;
}

#lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.85);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

#lightbox img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 10px;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const images = document.querySelectorAll('.zoomable');
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = document.getElementById('lightbox-img');

  images.forEach(img => {
    img.addEventListener('click', () => {
      lightboxImg.src = img.src;   // zet de juiste foto
      lightbox.style.display = 'flex';
    });
  });

  // klik ergens buiten de foto om te sluiten
  lightbox.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });
});
</script>
</script>

