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
.delft-gallery{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:16px;margin-top:24px}
.delft-gallery figure{margin:0}.delft-gallery img{width:100%;height:auto;cursor:zoom-in;border:1px solid #eee}
.delft-gallery figcaption{font-size:12px;color:#666;margin-top:5px}
#delft-lightbox:not([hidden]){position:fixed;inset:0;z-index:9999;background:rgba(0,0,0,.94);display:flex;align-items:center;justify-content:center;overflow:hidden}
#delft-lightbox img{max-width:94vw;max-height:92vh;object-fit:contain;transform-origin:center;cursor:zoom-in}
#delft-lightbox button{position:absolute;z-index:2;background:rgba(0,0,0,.45);border:0;color:white;font-size:26px;cursor:pointer;padding:12px}
.delft-close{top:12px;right:15px}.delft-prev{left:12px;top:50%}.delft-next{right:12px;top:50%}
@media(max-width:650px){.delft-gallery{grid-template-columns:1fr}}
</style>
<script>
document.addEventListener('DOMContentLoaded',function(){
const images=[...document.querySelectorAll('.delft-zoomable')],box=document.getElementById('delft-lightbox'),big=box.querySelector('img');
let index=0,scale=1;
function show(i){index=(i+images.length)%images.length;big.src=images[index].src;big.alt=images[index].alt;scale=1;big.style.transform='scale(1)';box.hidden=false;document.body.style.overflow='hidden'}
function close(){box.hidden=true;document.body.style.overflow='';big.src=''}
images.forEach((img,i)=>img.addEventListener('click',()=>show(i)));
box.querySelector('.delft-close').onclick=close;
box.querySelector('.delft-prev').onclick=()=>show(index-1);
box.querySelector('.delft-next').onclick=()=>show(index+1);
big.onclick=e=>{e.stopPropagation();scale=scale===1?2:1;big.style.transform='scale('+scale+')';big.style.cursor=scale===1?'zoom-in':'zoom-out'};
box.onclick=e=>{if(e.target===box)close()};
document.addEventListener('keydown',e=>{if(box.hidden)return;if(e.key==='Escape')close();if(e.key==='ArrowLeft')show(index-1);if(e.key==='ArrowRight')show(index+1)});
});
</script>