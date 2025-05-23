<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Respuesta al Impulso - Grupo UACh</title>
  <script src="https://unpkg.com/wavesurfer.js"></script>
  <style>
    /* Estilos generales */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #212121;
      color: #f0f0f0;
      display: flex;
      min-height: 100vh;
      flex-direction: column;
    }

    /* Barra lateral */
    .sidebar {
      width: 200px;
      height: 100vh;
      background: #171717;
      color: white;
      padding: 20px;
      position: fixed;
      overflow-y: auto;
    }

    .sidebar-header {
      text-align: center;
      margin-bottom: 15px;
    }

    .sidebar-logo {
      max-width: 100px;
      margin-bottom: 10px;
    }

    .sidebar-title {
      font-size: 1.2rem;
      margin-bottom: 5px;
      color: #f0f0f0;
    }

    .sidebar-subtitle {
      font-size: 0.8rem;
      color: #aaa;
      margin-bottom: 15px;
    }

    .sidebar-divider {
      border-bottom: 1px solid rgba(255,255,255,0.2);
      margin-bottom: 15px;
    }

    /* Botones de navegación */
    .nav-btn {
      display: block;
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      background: #282828;
      color: #f0f0f0;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      text-align: left;
      font-size: 15px;
      transition: all 0.3s;
    }

    .nav-btn:hover {
      background: #2a2a2a;
    }

    .nav-btn.active {
      background: #212121;
      font-weight: bold;
    }

    /* Contenido principal */
    .main-content {
      margin-left: 240px;
      padding: 20px 20px 30px 20px;
      width: calc(100% - 240px);
      flex: 1;
    }

    /* Secciones de contenido */
    .content-section {
      display: none;
      padding: 2rem;
      margin: 1rem auto 3rem auto;
      max-width: 900px;
      background: #2a2a2a;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
    }

    .content-section.active {
      display: block;
    }

    h2 {
      border-bottom: 2px solid #444;
      padding-bottom: 0.5rem;
      color: #f0f0f0;
    }

    h3, h4 {
      color: #f0f0f0;
    }

    .audio-block {
      margin: 1rem 0;
    }

    audio {
      width: 100%;
    }

    ul {
      color: #f0f0f0;
    }

    footer {
      text-align: center;
      padding: 0.5rem;
      color: #aaa;
      font-size: 0.8rem;
      width: calc(100% - 240px);
      margin-left: 240px;
      position: fixed;
      bottom: 0;
      background: transparent;
    }

    /* Player container styles */
    .player-container {
      margin: 20px 0;
      padding: 15px;
      background: #333;
      border-radius: 5px;
    }
    
    /* Audio group styles */
    .audio-group {
      margin-bottom: 30px;
      border-bottom: 1px solid #444;
      padding-bottom: 20px;
    }
    
    .audio-group:last-child {
      border-bottom: none;
    }
    
    /* Audio info styles */
    .audio-info {
      display: flex;
      justify-content: space-between;
      margin-bottom: 10px;
    }
    
    .audio-title {
      font-weight: bold;
    }
    
    .audio-duration {
      color: #aaa;
    }
  </style>
</head>
<body>
  <!-- Barra lateral -->
  <div class="sidebar">
    <div class="sidebar-header">
      <img src="imagenes/logo-au.png" alt="Logo" class="sidebar-logo">
      <div class="sidebar-title">Tarea 02</div>
      <div class="sidebar-subtitle">ACUS099</div>
    </div>
    <div class="sidebar-divider"></div>
    <button class="nav-btn active" onclick="showSection('inicio')">🏠 Inicio</button>
    <button class="nav-btn" onclick="showSection('integrantes')">👥 Integrantes</button>
    <button class="nav-btn" onclick="showSection('equipamiento')">🛠️ Equipamiento</button>
    <button class="nav-btn" onclick="showSection('recintos')">📍 Recintos Medidos</button>
    <button class="nav-btn" onclick="showSection('grabaciones')">🎙️ Grabaciones Secas</button>
    <button class="nav-btn" onclick="showSection('impulsos')">🔊 Respuestas al Impulso</button>
    <button class="nav-btn" onclick="showSection('convolucion')">🔁 Audios Convolucionados</button>
    <button class="nav-btn" onclick="showSection('galeria')">📸 Galería</button>
  </div>

  <!-- Contenido principal -->
  <div class="main-content">
    <!-- Sección Inicio -->
    <section id="inicio" class="content-section active">
      <header>
        <h1>Captura y Procesamiento de Respuesta al Impulso</h1>
        <p>Proyecto Acústica UACh - Grupo X</p>
      </header>
      <p>Bienvenido al informe del proyecto de medición acústica.</p>
    </section>

    <!-- Sección Integrantes -->
    <section id="integrantes" class="content-section">
      <h2>👥 Integrantes del Grupo</h2>
      <ul>
        <li>Nombre 1</li>
        <li>Nombre 2</li>
        <li>Nombre 3</li>
      </ul>
    </section>

    <!-- Sección Equipamiento -->
    <section id="equipamiento" class="content-section">
      <h2>🛠️ Equipamiento Utilizado</h2>
      <div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: space-around;">

        <div style="flex: 1 1 200px; text-align: center;">
          <img src="imagenes/Behringer-ECM8000-Microfono-de-Condensador-para-Medicion-Set-Planet-Music-1200x1200-1.png" alt="Micrófono" style="width: 100%; max-width: 200px; border-radius: 8px;">
          <p>Micrófono: Behringer-ECM8000</p>
        </div>

        <div style="flex: 1 1 200px; text-align: center;">
          <img src="imagenes/s-l400.png" alt="Fuente sonora" style="width: 100%; max-width: 200px; border-radius: 8px;">
          <p>Fuente sonora: Wood clapper</p>
        </div>

        <div style="flex: 1 1 200px; text-align: center;">
          <img src="imagenes/23544.png" alt="Grabadora o interfaz" style="width: 100%; max-width: 200px; border-radius: 8px;">
          <p>Grabadora/Interface: KOMPLETE Audio 1</p>
        </div>

        <div style="flex: 1 1 200px; text-align: center;">
          <img src="imagenes/s23_hero_sp23-dlab-ableton.png" alt="Software" style="width: 100%; max-width: 200px; border-radius: 8px;">
          <p>Software: Ableton Live 12 Suite</p>
        </div>

      </div>
    </section>

    <!-- Sección Recintos -->
    <section id="recintos" class="content-section">
      <h2>📍 Recintos Medidos</h2>
      <h3>1. Cámara Reverberante Acústica UACh</h3>
      <h3>2. Edificio 14K</h3>
      <h3>3. Edificio 6K pasillos</h3>
      
      <p>Descripción breve del recinto...</p>
    </section>

    <!-- Sección Grabaciones Secas -->
    <section id="grabaciones" class="content-section">
      <h2>🎙️ Grabaciones Secas</h2>
      <p>Grabaciones de voz e instrumento sin reverberación.</p>
      
      <div class="audio-group">
        <h3>Voz</h3>
        <div id="voz-seca" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>Instrumento</h3>
        <div id="instrumento-seco" class="player-container"></div>
      </div>
    </section>

    <!-- Sección Respuestas al Impulso -->
    <section id="impulsos" class="content-section">
      <h2>🔊 Respuestas al Impulso</h2>
      <p>Respuestas al impulso medidas en los diferentes recintos.</p>
      
      <div class="audio-group">
        <h3>1. Cámara Reverberante</h3>
        <div id="impulso-camara" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>2. Edificio 14K</h3>
        <div id="impulso-14k" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>3. Edificio 6K Pasillos</h3>
        <div id="impulso-6k" class="player-container"></div>
      </div>
    </section>

    <!-- Sección Audios Convolucionados -->
    <section id="convolucion" class="content-section">
      <h2>🔁 Audios Convolucionados</h2>
      <p>Resultados de aplicar convolución con las respuestas al impulso a las grabaciones secas.</p>
      
      <div class="audio-group">
        <h3>Voz en Cámara Reverberante</h3>
        <div id="voz-camara" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>Voz en Edificio 14K</h3>
        <div id="voz-14k" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>Voz en Edificio 6K Pasillos</h3>
        <div id="voz-6k" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>Instrumento en Cámara Reverberante</h3>
        <div id="instrumento-camara" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>Instrumento en Edificio 14K</h3>
        <div id="instrumento-14k" class="player-container"></div>
      </div>
      
      <div class="audio-group">
        <h3>Instrumento en Edificio 6K Pasillos</h3>
        <div id="instrumento-6k" class="player-container"></div>
      </div>
    </section>

    <!-- Sección Galería -->
    <section id="galeria" class="content-section">
      <h2>📸 Galería Fotográfica</h2>
      <p>Aquí irían las fotos del proyecto cuando estén disponibles.</p>
    </section>
  </div>

  <footer>
    <p>UACh - Escuela de Acústica | Proyecto de Medición ISO 3382</p>
  </footer>

  <script>
    function showSection(sectionId) {
      // Oculta todas las secciones
      document.querySelectorAll('.content-section').forEach(section => {
        section.classList.remove('active');
      });
      
      // Muestra la sección seleccionada
      document.getElementById(sectionId).classList.add('active');
      
      // Actualiza el botón activo
      document.querySelectorAll('.nav-btn').forEach(btn => {
        btn.classList.remove('active');
      });
      event.target.classList.add('active');
    }
    
    function createAudioPlayer(containerId, audioSrc, title) {
      const container = document.getElementById(containerId);
      if (!container) return;
      
      // Limpiar el contenedor si ya tiene contenido
      container.innerHTML = '';
      
      // Crear elemento de información del audio
      const audioInfo = document.createElement('div');
      audioInfo.className = 'audio-info';
      
      const audioTitle = document.createElement('div');
      audioTitle.className = 'audio-title';
      audioTitle.textContent = title || 'Audio';
      
      const audioDuration = document.createElement('div');
      audioDuration.className = 'audio-duration';
      audioDuration.textContent = '0:00 / 0:00';
      
      audioInfo.appendChild(audioTitle);
      audioInfo.appendChild(audioDuration);
      container.appendChild(audioInfo);
      
      // Crear el visualizador de onda
      const wavesurfer = WaveSurfer.create({
        container: `#${containerId}`,
        waveColor: '#4a4a4a',
        progressColor: '#2b91af',
        cursorColor: '#ffffff',
        barWidth: 2,
        barRadius: 3,
        cursorWidth: 1,
        height: 100,
        barGap: 2,
        responsive: true
      });
      
      wavesurfer.load(audioSrc);
      
      // Add controls
      const controls = document.createElement('div');
      controls.style.marginTop = '10px';
      controls.style.display = 'flex';
      controls.style.gap = '10px';
      controls.style.alignItems = 'center';
      
      const playBtn = document.createElement('button');
      playBtn.textContent = 'Play/Pause';
      playBtn.onclick = () => wavesurfer.playPause();
      
      const stopBtn = document.createElement('button');
      stopBtn.textContent = 'Stop';
      stopBtn.onclick = () => {
        wavesurfer.stop();
        wavesurfer.seekTo(0);
      };
      
      const volumeControl = document.createElement('input');
      volumeControl.type = 'range';
      volumeControl.min = '0';
      volumeControl.max = '1';
      volumeControl.step = '0.01';
      volumeControl.value = '1';
      volumeControl.oninput = (e) => wavesurfer.setVolume(e.target.value);
      
      controls.appendChild(playBtn);
      controls.appendChild(stopBtn);
      controls.appendChild(document.createTextNode('Vol:'));
      controls.appendChild(volumeControl);
      
      container.appendChild(controls);
      
      // Update time display
      wavesurfer.on('audioprocess', () => {
        const currentTime = wavesurfer.getCurrentTime();
        const duration = wavesurfer.getDuration();
        audioDuration.textContent = `${formatTime(currentTime)} / ${formatTime(duration)}`;
      });
      
      // Format time as MM:SS
      function formatTime(seconds) {
        const minutes = Math.floor(seconds / 60);
        const secs = Math.floor(seconds % 60);
        return `${minutes}:${secs < 10 ? '0' : ''}${secs}`;
      }
    }
    
    // Initialize audio players when the page loads
    document.addEventListener('DOMContentLoaded', () => {
      // Grabaciones secas
      createAudioPlayer("voz-seca", ".C:/Users/skate/Desktop/TAREA_02_ REPOSITORIO/audios/secos/an_03_poem.wav", "Voz seca (sin reverberación)");
      createAudioPlayer("instrumento-seco", "../audios/an_01_bot.wav", "Instrumento seco (sin reverberación)");
      
      // Respuestas al impulso
      createAudioPlayer("impulso-camara", "audios/ri-camara.wav", "Respuesta al impulso - Cámara Reverberante");
      createAudioPlayer("impulso-14k", "audios/ri-14k.wav", "Respuesta al impulso - Edificio 14K");
      createAudioPlayer("impulso-6k", "audios/ri-6k.wav", "Respuesta al impulso - Edificio 6K Pasillos");
      
      // Audios convolucionados
      createAudioPlayer("voz-camara", "audios/voz-conv-camara.wav", "Voz convolucionada - Cámara Reverberante");
      createAudioPlayer("voz-14k", "audios/voz-conv-14k.wav", "Voz convolucionada - Edificio 14K");
      createAudioPlayer("voz-6k", "audios/voz-conv-6k.wav", "Voz convolucionada - Edificio 6K Pasillos");
      createAudioPlayer("instrumento-camara", "audios/instrumento-conv-camara.wav", "Instrumento convolucionado - Cámara Reverberante");
      createAudioPlayer("instrumento-14k", "audios/instrumento-conv-14k.wav", "Instrumento convolucionado - Edificio 14K");
      createAudioPlayer("instrumento-6k", "audios/instrumento-conv-6k.wav", "Instrumento convolucionado - Edificio 6K Pasillos");
    });
  </script>
</body>
</html>
