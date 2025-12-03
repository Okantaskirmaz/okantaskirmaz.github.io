# Studio de Nieuwe Tuinstad

For ON4, I am designing a residential building in Het Kamrad, a green 1950s neighbourhood by Dudok in Hilversum. The assignment is to densify the area carefully without losing its existing spatial and landscape qualities. I explore how my design can connect to the characteristic structure of the neighbourhood and its direct relationship with the heath. Green living and nature-inclusive design are central themes in my approach. My building needs to achieve roughly 100 dwellings per hectare, with a mix of housing types and shared facilities. In the end, I translate these ideas into a clear design that shows how a contemporary new garden city can take shape within Het Kamrad.

Grade: 7.5

<div class="rpc-container">
  <div class="rpc-text"></div>
  <div class="rpc-gallery">
    <img class="zoomable" src="assets/Poster_1.jpg" alt="ON4 concept image 1">
    <img class="zoomable" src="assets/Poster_2.jpg" alt="ON4 concept image 2">
    <img class="zoomable" src="assets/Poster_3.jpg" alt="ON4 concept image 3">
    <img class="zoomable" src="assets/Poster met maquette.jpg" alt="ON4 concept image 4">
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
