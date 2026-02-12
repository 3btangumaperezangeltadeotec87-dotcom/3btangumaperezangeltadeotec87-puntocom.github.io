<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Proyecto de Química</title>

  <style>
    body{
      margin:0;
      font-family: 'Segoe UI', Tahoma, sans-serif;
      background: radial-gradient(circle at top, #020617, #020617, #0f172a);
      color:white;
      overflow-x:hidden;
    }

    /* FONDO QUÍMICO ANIMADO */
    .atoms{
      position:fixed;
      width:100%;
      height:100%;
      top:0;
      left:0;
      z-index:-1;
      background-image:
        radial-gradient(circle at 20% 30%, rgba(56,189,248,0.2) 2px, transparent 3px),
        radial-gradient(circle at 70% 60%, rgba(34,197,94,0.2) 2px, transparent 3px),
        radial-gradient(circle at 40% 80%, rgba(168,85,247,0.2) 2px, transparent 3px);
      animation: moveAtoms 20s linear infinite;
    }

    @keyframes moveAtoms{
      from{background-position:0 0, 0 0, 0 0;}
      to{background-position:300px 400px, 500px 200px, 200px 500px;}
    }

    header{
      background: linear-gradient(90deg,#020617,#0ea5e9,#020617);
      padding:20px;
      text-align:center;
      font-size:28px;
      font-weight:bold;
      letter-spacing:1px;
      box-shadow:0 0 20px rgba(14,165,233,0.6);
    }

    nav{
      display:flex;
      justify-content:center;
      gap:15px;
      background:#020617;
      padding:12px;
      flex-wrap:wrap;
      border-bottom:1px solid rgba(56,189,248,0.3);
    }

    nav button{
      padding:12px 20px;
      border:none;
      border-radius:14px;
      cursor:pointer;
      font-size:15px;
      background:#0f172a;
      color:white;
      box-shadow:0 0 10px rgba(56,189,248,0.4);
      transition:0.3s;
    }

    nav button:hover{
      background:#38bdf8;
      color:black;
      transform:scale(1.05);
    }

    section{
      display:none;
      padding:40px;
      max-width:1100px;
      margin:auto;
      line-height:1.7;
      animation: fade 0.5s ease;
    }

    @keyframes fade{
      from{opacity:0; transform:translateY(10px);} 
      to{opacity:1; transform:translateY(0);} 
    }

    .active{ display:block; }

    h2{
      color:#38bdf8;
      font-size:32px;
    }

    .card{
      background: rgba(15,23,42,0.7);
      padding:25px;
      border-radius:18px;
      box-shadow:0 0 25px rgba(56,189,248,0.3);
      margin-top:20px;
    }

    .audio-box{
      margin:25px 0;
      padding:18px;
      background:#020617;
      border-radius:14px;
      box-shadow:0 0 15px rgba(34,197,94,0.4);
    }

    /* IMAGENES */
    .img-science{
      width:100%;
      border-radius:16px;
      margin-top:20px;
      box-shadow:0 0 20px rgba(168,85,247,0.5);
    }

    footer{
      text-align:center;
      padding:20px;
      margin-top:40px;
      background:#020617;
      border-top:1px solid rgba(56,189,248,0.3);
    }

  </style>
</head>
<body>

<div class="atoms"></div>

<header>
  Plataforma Interactiva: Luz y Química
</header>

<!-- MUSICA DE FONDO -->
<audio id="musicaFondo" autoplay loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<nav>
  <button onclick="mostrar('menu')">Inicio</button>
  <button onclick="mostrar('tema1')">Teoría ondulatoria</button>
  <button onclick="mostrar('tema2')">Cuerpo negro</button>
  <button onclick="mostrar('tema3')">Fotoeléctrico</button>
  <button onclick="mostrar('tema4')">Espectros</button>
</nav>

<!-- MENU -->
<section id="menu" class="active">
  <h2>Bienvenido al laboratorio digital</h2>

  <div class="card">
    <p>Este sitio combina física y química para explicar la naturaleza de la luz y la estructura de la materia.</p>
    <p>Navega por cada pestaña y escucha la explicación científica mientras observas representaciones visuales.</p>

    <img class="img-science" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Bohr_atom_model.svg/800px-Bohr_atom_model.svg.png">
  </div>
</section>

<!-- TEMA 1 -->
<section id="tema1">
  <h2>Teoría ondulatoria de la luz</h2>

  <div class="audio-box">
    <audio controls autoplay>
      <source src="audio-tema1.mp3" type="audio/mpeg">
    </audio>
  </div>

  <div class="card">
    <p>La luz se comporta como una onda electromagnética capaz de propagarse en el vacío.</p>
    <p>Presenta fenómenos como reflexión, refracción, difracción e interferencia.</p>

    <img class="img-science" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Diffraction_pattern_single_slit.svg/800px-Diffraction_pattern_single_slit.svg.png">
  </div>
</section>

<!-- TEMA 2 -->
<section id="tema2">
  <h2>Radiación del cuerpo negro y Planck</h2>

  <div class="audio-box">
    <audio controls autoplay>
      <source src="audio-tema2.mp3" type="audio/mpeg">
    </audio>
  </div>

  <div class="card">
    <p>Un cuerpo negro absorbe toda la radiación que recibe y la emite según su temperatura.</p>
    <p>Planck propuso que la energía se emite en paquetes llamados cuantos.</p>

    <img class="img-science" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5d/Black_body.svg/800px-Black_body.svg.png">
  </div>
</section>

<!-- TEMA 3 -->
<section id="tema3">
  <h2>Efecto fotoeléctrico</h2>

  <div class="audio-box">
    <audio controls autoplay>
      <source src="audio-tema3.mp3" type="audio/mpeg">
    </audio>
  </div>

  <div class="card">
    <p>El efecto fotoeléctrico ocurre cuando la luz incide sobre un metal y libera electrones.</p>
    <p>Einstein explicó este fenómeno mediante los fotones.</p>

    <img class="img-science" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Photoelectric_effect.svg/800px-Photoelectric_effect.svg.png">
  </div>
</section>

<!-- TEMA 4 -->
<section id="tema4">
  <h2>Espectros de emisión</h2>

  <div class="audio-box">
    <audio controls autoplay>
      <source src="audio-tema4.mp3" type="audio/mpeg">
    </audio>
  </div>

  <div class="card">
    <p>Los electrones al cambiar de nivel liberan energía formando espectros característicos.</p>
    <p>Cada elemento químico posee su propia firma espectral.</p>

    <img class="img-science" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Emission_spectrum-H.svg/800px-Emission_spectrum-H.svg.png">
  </div>
</section>

<footer>
  Proyecto educativo de química
</footer>

<script>
  function mostrar(id){
    document.querySelectorAll('section').forEach(sec => sec.classList.remove('active'));
    document.getElementById(id).classList.add('active');
  }
</script>

</body>
</html>
