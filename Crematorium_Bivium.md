# Crematorium Bivium

For my graduation project, I designed Crematorium Bivium, a peaceful and respectful environment where architecture, nature and ritual come together. The design guides visitors through a gradual transition from public to intimate spaces, while separate routes provide privacy and tranquillity. Natural materials, integrated technical functions and sustainable solutions contribute to a calm and meaningful experience.

Grade: 8.5

<div class="rpc-container">
  <div class="rpc-text"></div>
  <div class="rpc-gallery">
    <img class="zoomable" src="assets/Bivium1.png" alt="IOP2 concept image 1">
    <img class="zoomable" src="assets/Bivium2.png" alt="IOP2 concept image 2">
    <img class="zoomable" src="assets/Bivium3.png" alt="IOP2 concept image 3">
    <img class="zoomable" src="assets/Bivium4.png" alt="IOP2 concept image 4">
    <img class="zoomable" src="assets/Bivium5.png" alt="IOP2 concept image 5">
    <img class="zoomable" src="assets/Bivium6.png" alt="IOP2 concept image 6">
    <img class="zoomable" src="assets/Bivium7.png" alt="IOP2 concept image 7">
    <img class="zoomable" src="assets/Bivium8.png" alt="IOP2 concept image 8">
    <img class="zoomable" src="assets/Bivium9.png" alt="IOP2 concept image 9">
    <img class="zoomable" src="assets/Bivium10.png" alt="IOP2 concept image 10">
    <img class="zoomable" src="assets/Bivium11.png" alt="IOP2 concept image 11">
    <img class="zoomable" src="assets/Bivium12.png" alt="IOP2 concept image 12">
    <img class="zoomable" src="assets/Bivium13.png" alt="IOP2 concept image 13">
    <img class="zoomable" src="assets/Bivium14.png" alt="IOP2 concept image 14">
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
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  transition: background 0.2s ease;
}

.lightbox-nav:hover {
  background: rgba(0, 0, 0, 0.7);
}

.lightbox-nav:focus-visible {
  outline: 2px solid #fff;
}

.lightbox-nav.prev {
  left: 32px;
}

.lightbox-nav.next {
  right: 32px;
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
