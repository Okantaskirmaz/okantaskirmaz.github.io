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
  <button class="lightbox-nav prev" aria-label="Vorige afbeelding">&#10094;</button>
  <img id="lightbox-img" src="">
  <button class="lightbox-nav next" aria-label="Volgende afbeelding">&#10095;</button>
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

.lightbox-nav {
  background: rgba(0, 0, 0, 0.5);
  border: none;
  color: #fff;
  font-size: 2rem;
  padding: 0.6rem 1rem;
  cursor: pointer;
  border-radius: 8px;
  margin: 0 1rem;
  transition: background 0.2s ease;
}

.lightbox-nav:hover {
  background: rgba(0, 0, 0, 0.7);
}

.lightbox-nav:focus-visible {
  outline: 2px solid #fff;
}

.lightbox-nav.prev {
  order: 0;
}

.lightbox-nav.next {
  order: 2;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const images = Array.from(document.querySelectorAll('.zoomable'));
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = document.getElementById('lightbox-img');
  const prevBtn = document.querySelector('.lightbox-nav.prev');
  const nextBtn = document.querySelector('.lightbox-nav.next');
  let currentIndex = 0;

  function showImage(index) {
    currentIndex = (index + images.length) % images.length;
    lightboxImg.src = images[currentIndex].src;
    lightbox.style.display = 'flex';
  }

  images.forEach((img, index) => {
    img.addEventListener('click', () => {
      showImage(index);
    });
  });

  prevBtn.addEventListener('click', (event) => {
    event.stopPropagation();
    showImage(currentIndex - 1);
  });

  nextBtn.addEventListener('click', (event) => {
    event.stopPropagation();
    showImage(currentIndex + 1);
  });

  // sluit door buiten de foto te klikken
  lightbox.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });
});
</script>
