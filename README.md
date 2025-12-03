# Projects

Hello! Welcome to my portfolio repository. Here you’ll find an overview of several projects I’ve worked on during my studies as a bachelor architecture student at TU Delft. My interests focus on the urban challenges faced by modern cities and the methods used to address them, including participatory design, GIS, and data-driven analysis. Each link provides a deeper look into different phases of my projects and includes the corresponding documentation and code.

<br>

<div class="project-cards">

  <a href="https://okantaskirmaz.github.io/reimagining_port_cities" class="card-link">
    <div class="card">
      <img src="assets/Port Cities 4.jpg" alt="Sfeerbeeld" />
      <div class="card-text">
        Minor, (Re)Imagining Port Cities: Understanding Space, Society and Culture Q1
      </div>
    </div>
  </a>

    <a href="https://okantaskirmaz.github.io/Studio_de_Nieuwe_Tuinstad" class="card-link">
    <div class="card">
      <img src="assets/Poster_1.jpg" alt="Sfeerbeeld" />
      <div class="card-text">
        Studio de Nieuwe Tuinstad
      </div>
    </div>
  </a>

<hr>


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
  

  
.project-cards {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 1rem;
  justify-content: space-between;
  box-sizing: border-box;
}

.card {
  border: 0.7px solid #ddd;
  padding: 1rem;
  border-radius: 3px;
  background-color: #ffffff;
  transition: transform 0.2s;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  height: 100%;
  box-sizing: border-box;
}

.card:hover {
  transform: scale(1.02);
}

.card img {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 3px;
  display: block;
  margin: 0 auto;
}

.card-link {
  display: block;
  text-decoration: none;
  color: inherit;
  width: calc(50% - 10px); 
  box-sizing: border-box;
}

.card-text {
  margin-top: 0.5rem;
  font-weight: 500;
  font-size: 0.75rem;
}

@media (max-width: 768px) {
  .card-link {
    flex: 1 1 100%;
    max-width: 100%;
  }
}
</style>
