# Museo-huasteca
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Museo Virtual Mesoamericano</title>

<style>
body {
    margin: 0;
    font-family: 'Arial', sans-serif;
    background-color: #0b0b0b;
    color: white;
    scroll-behavior: smooth;
}

/* MENÚ */
nav {
    position: fixed;
    width: 100%;
    background: rgba(0,0,0,0.8);
    padding: 10px;
    text-align: center;
    z-index: 1000;
}

nav a {
    color: #d4af37;
    margin: 10px;
    text-decoration: none;
    font-weight: bold;
}

nav a:hover {
    color: white;
}

/* PORTADA */
header {
    height: 100vh;
    background: url('https://images.unsplash.com/photo-1589394815804-964ed0be2eb5') center/cover no-repeat;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

header h1 {
    font-size: 3em;
    background: rgba(0,0,0,0.6);
    padding: 20px;
}

/* SECCIONES */
section {
    padding: 80px 40px;
    border-bottom: 1px solid #222;
    opacity: 0;
    transform: translateY(50px);
    transition: 1s;
}

section.visible {
    opacity: 1;
    transform: translateY(0);
}

h2 {
    color: #d4af37;
}

.container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

.text {
    flex: 1;
    min-width: 300px;
}

.image {
    flex: 1;
}

.image img {
    width: 100%;
    border-radius: 10px;
}

/* GALERÍA */
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
}

.gallery img {
    width: 100%;
    border-radius: 10px;
}

/* VIDEO */
.video {
    text-align: center;
}
</style>
</head>

<body>

<!-- MENÚ -->
<nav>
<a href="#s1">Orígenes</a>
<a href="#s2">Cultura</a>
<a href="#s3">Economía</a>
<a href="#s4">Ciencia</a>
<a href="#s5">Historia</a>
<a href="#s6">Legado</a>
</nav>

<!-- MÚSICA -->
<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<!-- PORTADA -->
<header>
<h1>Museo Virtual de las Culturas Mesoamericanas</h1>
</header>

<section id="s1">
<h2>🧭 Orígenes y desarrollo</h2>
<div class="container">
<div class="text">
<p>Las culturas mesoamericanas surgieron hace miles de años. Civilizaciones como olmecas, mayas y mexicas evolucionaron con el tiempo.</p>
</div>
<div class="image">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/36/Mesoamerica_English.png">
</div>
</div>
</section>

<section id="s2">
<h2>🏺 Cultura y sociedad</h2>
<div class="container">
<div class="text">
<p>La sociedad estaba organizada en jerarquías. La religión, arte y tradiciones eran fundamentales.</p>
</div>
<div class="image">
<img src="https://upload.wikimedia.org/wikipedia/commons/1/1e/Chichen_Itza_3.jpg">
</div>
</div>
</section>

<section id="s3">
<h2>💰 Economía</h2>
<div class="container">
<div class="text">
<p>Se basaba en el trueque y la agricultura como el maíz, frijol y calabaza.</p>
</div>
<div class="image">
<img src="https://upload.wikimedia.org/wikipedia/commons/5/5d/Chinampas.jpg">
</div>
</div>
</section>

<section id="s4">
<h2>🔬 Ciencia</h2>
<div class="container">
<div class="text">
<p>Los mayas desarrollaron matemáticas avanzadas y calendarios precisos.</p>
</div>
<div class="image">
<img src="https://upload.wikimedia.org/wikipedia/commons/8/8f/Mayan_Calendar.jpg">
</div>
</div>
</section>

<section id="s5">
<h2>⚔️ Historia y conquista</h2>
<div class="container">
<div class="text">
<p>La llegada de los españoles cambió estas civilizaciones profundamente.</p>
</div>
<div class="image">
<img src="https://upload.wikimedia.org/wikipedia/commons/0/0c/Cortes_Tenochtitlan.jpg">
</div>
</div>
</section>

<section id="s6">
<h2>🌎 Legado</h2>
<div class="container">
<div class="text">
<p>Su legado sigue vivo en la cultura actual y sitios arqueológicos.</p>
</div>
<div class="image">
<img src="https://upload.wikimedia.org/wikipedia/commons/e/e3/Teotihuacan_Pyramid_of_the_Sun.jpg">
</div>
</div>
</section>

<!-- VIDEO -->
<section class="video">
<h2>🎥 Video educativo</h2>
<iframe width="80%" height="400" src="https://www.youtube.com/embed/0G9z7X2Jb8I" frameborder="0" allowfullscreen></iframe>
</section>

<!-- GALERÍA -->
<section>
<h2>🖼️ Galería</h2>
<div class="gallery">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Olmec_Head_No_1.jpg">
<img src="https://upload.wikimedia.org/wikipedia/commons/1/10/Maya_artifact.jpg">
<img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Aztec_calendar_stone.jpg">
<img src="https://upload.wikimedia.org/wikipedia/commons/6/6f/Tulum_ruins.jpg">
</div>
</section>

<script>
const sections = document.querySelectorAll("section");

window.addEventListener("scroll", () => {
sections.forEach(sec => {
const top = sec.getBoundingClientRect().top;
if(top < window.innerHeight - 100){
sec.classList.add("visible");
}
});
});
</script>

</body>
</html>
