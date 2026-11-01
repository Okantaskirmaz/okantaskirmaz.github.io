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
  <img id="lightbox-img" src="" alt="Vergrote projectafbeelding" draggable="false" title="Scroll om in te zoomen; sleep om de afbeelding te verplaatsen">
  <button type="button" class="lightbox-close" aria-label="Sluiten">×</button>
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

/* Mousewheel zoom and dragging inside the enlarged photo */
#lightbox { overflow: hidden; }
#lightbox img {
  transform-origin: center center;
  cursor: zoom-in;
  user-select: none;
  -webkit-user-drag: none;
  touch-action: none;
  border-radius: 0;
}
#lightbox img.is-zoomed { cursor: grab; }
#lightbox img.is-dragging { cursor: grabbing; }
.lightbox-close {
  position: absolute;
  top: 16px;
  right: 20px;
  z-index: 2;
  background: rgba(0, 0, 0, 0.55);
  color: #fff;
  border: 1px solid rgba(255,255,255,0.3);
  border-radius: 6px;
  font-size: 28px;
  line-height: 1;
  padding: 6px 12px;
  cursor: pointer;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const images = Array.from(document.querySelectorAll('.rpc-gallery .zoomable'));
  const lightbox = document.getElementById('lightbox');
  if (!images.length || !lightbox) return;

  const photo = document.getElementById('lightbox-img');
  const prev = lightbox.querySelector('.lightbox-nav.prev');
  const next = lightbox.querySelector('.lightbox-nav.next');
  const closeButton = lightbox.querySelector('.lightbox-close');

  let index = 0;
  let scale = 1;
  let offsetX = 0;
  let offsetY = 0;
  let dragging = false;
  let lastX = 0;
  let lastY = 0;

  function limitOffsets() {
    const maxX = Math.max(0, (photo.clientWidth * scale - photo.clientWidth) / 2);
    const maxY = Math.max(0, (photo.clientHeight * scale - photo.clientHeight) / 2);
    offsetX = Math.max(-maxX, Math.min(maxX, offsetX));
    offsetY = Math.max(-maxY, Math.min(maxY, offsetY));
  }

  function render() {
    limitOffsets();
    photo.style.transform = 'translate(' + offsetX + 'px, ' + offsetY + 'px) scale(' + scale + ')';
    photo.classList.toggle('is-zoomed', scale > 1);
  }

  function resetZoom() {
    scale = 1;
    offsetX = 0;
    offsetY = 0;
    dragging = false;
    photo.classList.remove('is-dragging');
    render();
  }

  function showImage(nextIndex) {
    index = (nextIndex + images.length) % images.length;
    photo.src = images[index].src;
    photo.alt = images[index].alt;
    lightbox.style.display = 'flex';
    document.body.style.overflow = 'hidden';
    resetZoom();
  }

  function closeLightbox() {
    lightbox.style.display = 'none';
    document.body.style.overflow = '';
    resetZoom();
  }

  images.forEach(function (image, i) {
    image.addEventListener('click', function () { showImage(i); });
  });

  prev.addEventListener('click', function (event) {
    event.stopPropagation();
    showImage(index - 1);
  });

  next.addEventListener('click', function (event) {
    event.stopPropagation();
    showImage(index + 1);
  });

  closeButton.addEventListener('click', function (event) {
    event.stopPropagation();
    closeLightbox();
  });

  // Zoom towards the mouse position; keep the page from scrolling.
  lightbox.addEventListener('wheel', function (event) {
    if (lightbox.style.display !== 'flex') return;
    event.preventDefault();
    const oldScale = scale;
    const direction = event.deltaY < 0 ? 1.18 : 1 / 1.18;
    scale = Math.min(8, Math.max(1, scale * direction));
    if (scale === oldScale) return;

    // Keep the detail underneath the cursor in the same place.
    const relativeX = event.clientX - (window.innerWidth / 2 + offsetX);
    const relativeY = event.clientY - (window.innerHeight / 2 + offsetY);
    const ratio = scale / oldScale;
    offsetX += relativeX * (1 - ratio);
    offsetY += relativeY * (1 - ratio);
    if (scale === 1) {
      offsetX = 0;
      offsetY = 0;
    }
    render();
  }, { passive: false });

  // Drag to explore details once zoomed in.
  photo.addEventListener('pointerdown', function (event) {
    if (scale <= 1 || event.button !== 0) return;
    event.preventDefault();
    dragging = true;
    lastX = event.clientX;
    lastY = event.clientY;
    photo.setPointerCapture(event.pointerId);
    photo.classList.add('is-dragging');
  });

  photo.addEventListener('pointermove', function (event) {
    if (!dragging) return;
    offsetX += event.clientX - lastX;
    offsetY += event.clientY - lastY;
    lastX = event.clientX;
    lastY = event.clientY;
    render();
  });

  function stopDragging() {
    dragging = false;
    photo.classList.remove('is-dragging');
  }
  photo.addEventListener('pointerup', stopDragging);
  photo.addEventListener('pointercancel', stopDragging);
  photo.addEventListener('lostpointercapture', stopDragging);

  lightbox.addEventListener('click', function (event) {
    if (event.target === lightbox) closeLightbox();
  });

  document.addEventListener('keydown', function (event) {
    if (lightbox.style.display !== 'flex') return;
    if (event.key === 'Escape') closeLightbox();
    if (event.key === 'ArrowLeft') showImage(index - 1);
    if (event.key === 'ArrowRight') showImage(index + 1);
  });
  window.addEventListener('resize', function () {
    if (lightbox.style.display === 'flex') render();
  });
});
</script>
