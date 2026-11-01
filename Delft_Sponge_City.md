# Delft as an Interconnected Sponge City

*Master of Science Urbanism — TU Delft | 2026*

How can Delft adapt to increasingly extreme rainfall towards 2100? This project explores how streets, public spaces and green infrastructure can work together as a connected urban water system. Through spatial analyses of flood exposure, surface permeability, housing and movement networks, vulnerable areas were identified across the city. The findings formed the basis for a strategy that combines water management with ecological connectivity, recreation and cycling.

The proposal introduces three complementary interventions: **Sponge Clusters**, where vulnerable areas are transformed into places that absorb and temporarily store rainfall; a **Sponge Spine**, a continuous lowered green corridor that collects and guides excess water towards lower-lying landscapes; and a **Porous Urban Fabric**, a network of smaller green spaces and permeable connections that links neighbourhoods to the larger system. An elevated cycling route remains accessible during heavy rainfall, while the lowered landscape provides recreational space during dry conditions.

The strategy adapts to different urban settings. In the compact historic centre, interventions respond to narrow streets and existing buildings. In residential neighbourhoods, wider profiles allow more space for temporary storage and recreation. At the infrastructure edge, the corridor crosses above a lowered highway, reconnecting green landscapes on either side.

<div class="delft-gallery">
  <figure><img class="delft-zoomable" src="assets/Delft1.png" alt="Urban flood vulnerability analysis" loading="lazy"><figcaption>Urban flood vulnerability analysis</figcaption></figure>
  <figure><img class="delft-zoomable" src="assets/Delft2.png" alt="Vulnerability typologies and strategic diagram" loading="lazy"><figcaption>Urban conditions and opportunities</figcaption></figure>
  <figure><img class="delft-zoomable" src="assets/Delft3.png" alt="Sponge clusters, spine and porous urban fabric synthesis" loading="lazy"><figcaption>Sponge City design strategy</figcaption></figure>
  <figure><img class="delft-zoomable" src="assets/Delft4.png" alt="Urban design typologies and regional strategy" loading="lazy"><figcaption>Adapting the Sponge Spine to different urban conditions</figcaption></figure>
  <figure><img class="delft-zoomable" src="assets/Delft5.png" alt="Sponge Spine sections in dry and extreme rainfall conditions" loading="lazy"><figcaption>Living with the Sponge Spine: dry and rainy conditions</figcaption></figure>
  <figure><img class="delft-zoomable" src="assets/Delft6.png" alt="Delft as an Interconnected Sponge City final design poster" loading="lazy"><figcaption>Final design poster</figcaption></figure>
</div>
<div id="delft-lightbox" role="dialog" aria-label="Enlarged project image" aria-modal="true" hidden>
  <button type="button" class="delft-close" aria-label="Close">×</button>
  <button type="button" class="delft-prev" aria-label="Previous image">❮</button>
  <img alt="Enlarged project drawing">
  <button type="button" class="delft-next" aria-label="Next image">❯</button>
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
