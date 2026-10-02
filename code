!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Un Universo Para Ti ✨</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
    }

    #canvas-universe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
    }

    .container {
      position: relative;
      z-index: 2;
      text-align: center;
      padding: 35px;
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(12px);
      border-radius: 24px;
      border: 1px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 0 35px rgba(138, 43, 226, 0.35);
      max-width: 90%;
      width: 450px;
    }

    h1 {
      font-size: 2.1rem;
      margin-bottom: 12px;
      background: linear-gradient(45deg, #ff758c, #ff7eb3, #a18cd1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 20px rgba(255, 117, 140, 0.5);
    }

    p.subtitle {
      font-size: 0.95rem;
      color: #d1d5db;
      margin-bottom: 30px;
    }

    .btn-group {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .btn {
      padding: 15px 25px;
      font-size: 1rem;
      font-weight: 600;
      color: #fff;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }

    .btn-reasons {
      background: linear-gradient(135deg, #ff758c 0%, #ff7eb3 100%);
    }

    .btn-date {
      background: linear-gradient(135deg, #8a2be2 0%, #4a00e0 100%);
    }

    .btn:hover {
      transform: translateY(-3px) scale(1.02);
      box-shadow: 0 8px 25px rgba(255, 117, 140, 0.4);
    }

    /* Modales */
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      backdrop-filter: blur(10px);
      z-index: 10;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    .modal-content {
      background: #121620;
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 24px;
      width: 100%;
      max-width: 500px;
      padding: 30px;
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;
      box-shadow: 0 0 40px rgba(138, 43, 226, 0.5);
      animation: zoomIn 0.4s ease;
      text-align: center;
    }

    @keyframes zoomIn {
      from { opacity: 0; transform: scale(0.85); }
      to { opacity: 1; transform: scale(1); }
    }

    .close-btn {
      position: absolute;
      top: 15px;
      right: 20px;
      font-size: 1.8rem;
      color: #aaa;
      cursor: pointer;
      transition: color 0.2s;
    }

    .close-btn:hover {
      color: #fff;
    }

    .modal-title {
      font-size: 1.3rem;
      color: #ff7eb3;
      margin-bottom: 20px;
    }

    /* Contenedor Cascada para 100 razones */
    .ticker-viewport {
      width: 100%;
      height: 260px;
      overflow: hidden;
      position: relative;
      border-radius: 16px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.1);
      padding: 10px;
    }

    .ticker-track {
      display: flex;
      flex-direction: column;
      gap: 12px;
      animation: scrollUp 45s linear infinite;
    }

    .ticker-track:hover {
      animation-play-state: paused;
    }

    @keyframes scrollUp {
      0% { transform: translateY(0); }
      100% { transform: translateY(-50%); }
    }

    .reason-chip {
      background: rgba(255, 117, 140, 0.12);
      border: 1px solid rgba(255, 126, 179, 0.3);
      padding: 10px 16px;
      border-radius: 12px;
      font-size: 0.95rem;
      color: #f1f5f9;
      display: flex;
      align-items: center;
      gap: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
    }

    .reason-chip span {
      color: #ff7eb3;
      font-weight: 600;
      font-size: 0.85rem;
    }

    /* Animaciones para Invitación y Respuestas */
    .heart-icon {
      font-size: 3.5rem;
      animation: heartbeat 1.2s infinite ease-in-out;
      margin: 10px 0;
      display: inline-block;
    }

    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.25); }
    }

    .anim-yes-icon {
      font-size: 4rem;
      animation: celebrate 1s ease infinite alternate;
      margin: 15px 0;
    }

    @keyframes celebrate {
      0% { transform: scale(1) rotate(-5deg); }
      100% { transform: scale(1.2) rotate(5deg); }
    }

    .anim-no-icon {
      font-size: 4rem;
      animation: softSad 2s infinite ease-in-out;
      margin: 15px 0;
    }

    @keyframes softSad {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(10px); }
    }

    .quote-box {
      min-height: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 10px 0 20px 0;
    }

    .quote-text {
      font-style: italic;
      color: #d1d5db;
      font-size: 0.9rem;
    }

    .action-btns {
      display: flex;
      gap: 15px;
      width: 100%;
      position: relative;
    }

    .btn-yes {
      flex: 1;
      background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
      color: #fff;
      padding: 12px;
      border: none;
      border-radius: 25px;
      font-weight: 600;
      cursor: pointer;
      transition: transform 0.2s;
    }

    .btn-no {
      flex: 1;
      background: linear-gradient(135deg, #ff416c 0%, #ff4b2b 100%);
      color: #fff;
      padding: 12px;
      border: none;
      border-radius: 25px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .btn-yes:hover { transform: scale(1.05); }

    .response-card-text {
      font-size: 1.05rem;
      line-height: 1.6;
      color: #f1f5f9;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <canvas id="canvas-universe"></canvas>

  <div class="container">
    <h1>Un Universo Para Ti ✨</h1>
    <p class="subtitle">Hay cosas en el universo infinitas, pero hay un par que destacan para mí...</p>
    
    <div class="btn-group">
      <button class="btn btn-reasons" onclick="openModal('modal-reasons')">
        100 cosas que me encantan de ti 💖
      </button>
      <button class="btn btn-date" onclick="openModal('modal-date')">
        Una invitación especial 🌲✨
      </button>
    </div>
  </div>

  <!-- Modal 100 Cosas (Cascada Continua) -->
  <div id="modal-reasons" class="modal">
    <div class="modal-content">
      <span class="close-btn" onclick="closeModal('modal-reasons')">&times;</span>
      <h2 class="modal-title">Cosas que me encantan de ti 💖</h2>
      
      <div class="ticker-viewport">
        <div class="ticker-track" id="ticker-container"></div>
      </div>
    </div>
  </div>

  <!-- Modal Cita con Opción Sí / No -->
  <div id="modal-date" class="modal">
    <div class="modal-content">
      <span class="close-btn" onclick="closeModal('modal-date')">&times;</span>
      <h2 class="modal-title">Cita en Selva Negra 🌲☕</h2>
      
      <div class="heart-icon">💖</div>

      <p style="font-size: 1rem; color: #fff; margin-bottom: 10px; font-weight: 600;">
        ¿Te gustaría acompañarme a disfrutar de Selva Negra?
      </p>

      <div class="quote-box">
        <p class="quote-text">"Entre tantas estrellas en el universo, tu luz es la única que sigo."</p>
      </div>

      <div class="action-btns">
        <button class="btn-yes" onclick="handleChoice('yes')">¡Sí! 🥰</button>
        <button class="btn-no" id="btn-no-option" onclick="handleChoice('no')">No 🙈</button>
      </div>
    </div>
  </div>

  <!-- Modal Animación SI -->
  <div id="modal-response-yes" class="modal">
    <div class="modal-content" style="border-color: rgba(56, 239, 125, 0.4); box-shadow: 0 0 40px rgba(56, 239, 125, 0.3);">
      <span class="close-btn" onclick="closeModal('modal-response-yes')">&times;</span>
      <div class="anim-yes-icon">✨🥰💖</div>
      <h2 class="modal-title" style="color: #38ef7d;">¡Siiii! 🎉</h2>
      <p class="response-card-text">
        Qué bonito que hayas aceptado! ❤️ Espero poder conocerte mucho más y hacerte sonreír. 🫶🏻
      </p>
    </div>
  </div>

  <!-- Modal Animación NO -->
  <div id="modal-response-no" class="modal">
    <div class="modal-content" style="border-color: rgba(255, 75, 43, 0.4); box-shadow: 0 0 40px rgba(255, 75, 43, 0.3);">
      <span class="close-btn" onclick="closeModal('modal-response-no')">&times;</span>
      <div class="anim-no-icon">🌙🥺☁️</div>
      <h2 class="modal-title" style="color: #ff758c;">Está bien... ✨</h2>
      <p class="response-card-text">
        No te preocupes, entiendo y respeto tu decisión. Gracias por ser sincera conmigo, no quiero que te sientas incómoda. 😞🥺
      </p>
    </div>
  </div>

  <script>
    const reasons = [
      "Tu sonrisa", "Tus ojos", "Tu mirada", "Tu risa", "Tu voz",
      "Tu forma de hablar", "Tu forma de caminar", "Tu cabello", "Tu estilo", "Tu personalidad",
      "Tu forma de pensar", "Tu inteligencia", "Tu sentido del humor", "Tus gestos", "Tus expresiones",
      "Tu amabilidad", "Tu forma de bromear", "Tu manera de decir mi nombre", "Tus ocurrencias", "Tus detalles",
      "Tu paciencia", "Tu confianza", "Tu sinceridad", "Tus gustos", "Tus hobbies",
      "Tu creatividad", "Tu forma de explicar cosas", "Tu forma de contar historias", "Tu manera de ver el mundo", "Tu actitud",
      "Tu energía", "Tu memoria para recordar cosas", "Tu forma de entenderme", "Tu forma de ser conmigo", "Tu lado divertido",
      "Tu lado serio", "Tu lado tierno", "Tu forma de pensar diferente", "Tu manera de reaccionar", "Tus metas",
      "Tus sueños", "Tu esfuerzo", "Tu forma de resolver problemas", "Tu forma de confiar", "Tus pequeñas manías",
      "Tu naturalidad", "Tu autenticidad", "Tu forma única de ser", "Tu manera de ver las cosas", "Tu belleza",
      "Tu ternura", "Tu forma de sonreír", "Tu forma de reír", "Tu mirada cuando estás feliz", "Tu tranquilidad",
      "Tu forma de expresarte", "Tu sensibilidad", "Tu manera de entender a los demás", "Tu forma de pensar en el futuro", "Tu forma de aprender cosas",
      "Tu forma de hablar de lo que te gusta", "Tu manera de emocionarte", "Tu forma de ver los pequeños detalles", "Tu manera de cuidar lo que te importa", "Tu forma de esforzarte por lo que quieres",
      "Tu manera de mantenerte fuerte", "Tu forma de ser sincera", "Tu forma de decir lo que piensas", "Tu manera de hacer las cosas a tu forma", "Tu forma de sorprender",
      "Tu manera de reaccionar a las cosas buenas", "Tu manera de reaccionar a las cosas difíciles", "Tu forma de disfrutar momentos simples", "Tu forma de concentrarte", "Tu manera de hablar cuando algo te emociona",
      "Tu forma de mostrar lo que sientes", "Tu manera de valorar las cosas", "Tu forma de cuidar a las personas que quieres", "Tu manera de ser especial sin intentarlo", "Tu forma de destacar",
      "Tu manera de ser diferente", "Tu forma de hacer especiales los momentos", "Tu manera de ver lo bueno en las cosas", "Tu forma de mantenerte fiel a ti misma", "Tu manera de ser fuerte cuando hace falta",
      "Tu forma de levantarte cuando algo sale mal", "Tu manera de seguir adelante", "Tu forma de alegrar un momento", "Tu manera de hacer reír", "Tu forma de llenar un lugar con tu presencia",
      "Tu manera de hacer que todo se sienta más tranquilo", "Tu forma de hacer que los momentos valgan más", "Tu manera de hacer que alguien se sienta importante", "Tu forma de ser tan tú", "Tu manera de hacer que los días sean mejores",
      "Tu forma de brillar sin darte cuenta", "Tu manera de dejar huella", "Tu forma de ser única", "Tu forma de ser diferente a las demás", "Todo lo que te hace ser quien eres.✨"
    ];

    // Cargar tarjetas duplicadas para el efecto infinito en marquesina
    const tickerContainer = document.getElementById('ticker-container');
    const fullList = [...reasons, ...reasons];
    
    fullList.forEach((text, i) => {
      const num = (i % reasons.length) + 1;
      const chip = document.createElement('div');
      chip.className = 'reason-chip';
      chip.innerHTML = `<span>#${num}</span> ${text}`;
      tickerContainer.appendChild(chip);
    });

    // Manejar selección de respuesta y guardar en servidor
    function handleChoice(choice) {
      closeModal('modal-date');
      
      const answerText = choice === 'yes' ? 'Aceptó la cita ❤️' : 'Rechazó la cita 💔';
      sendResponseToServer(answerText);

      if (choice === 'yes') {
        openModal('modal-response-yes');
      } else {
        openModal('modal-response-no');
      }
    }

    // Enviar la respuesta al backend Node.js
    async function sendResponseToServer(answer) {
      try {
        await fetch('/api/responder', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({
            respuesta: answer,
            fecha: new Date().toLocaleString()
          })
        });
      } catch (err) {
        console.log('Error de conexión o servidor local no iniciado:', err);
      }
    }

    // Esquivar botón No
    const btnNo = document.getElementById('btn-no-option');
    btnNo.addEventListener('mouseover', () => {
      const randomX = (Math.random() - 0.5) * 80;
      const randomY = (Math.random() - 0.5) * 40;
      btnNo.style.transform = `translate(${randomX}px, ${randomY}px)`;
    });

    // Modales
    function openModal(id) { document.getElementById(id).style.display = 'flex'; }
    function closeModal(id) { document.getElementById(id).style.display = 'none'; }

    // Fondo Canvas Universo
    const canvas = document.getElementById('canvas-universe');
    const ctx = canvas.getContext('2d');
    let stars = [];

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }

    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    class Star {
      constructor() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * canvas.height;
        this.size = Math.random() * 2;
        this.speedX = (Math.random() - 0.5) * 0.2;
        this.speedY = (Math.random() - 0.5) * 0.2;
        this.brightness = Math.random();
        this.brightnessChange = 0.01;
      }

      update() {
        this.x += this.speedX;
        this.y += this.speedY;
        if (this.x < 0 || this.x > canvas.width) this.speedX *= -1;
        if (this.y < 0 || this.y > canvas.height) this.speedY *= -1;
        this.brightness += this.brightnessChange;
        if (this.brightness >= 1 || this.brightness <= 0.2) this.brightnessChange *= -1;
      }

      draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fillStyle = `rgba(255, 255, 255, ${this.brightness})`;
        ctx.shadowBlur = 8;
        ctx.shadowColor = '#fff';
        ctx.fill();
      }
    }

    for (let i = 0; i < 150; i++) stars.push(new Star());

    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      stars.forEach(s => { s.update(); s.draw(); });
      requestAnimationFrame(animate);
    }
    animate();
  </script>
</body>
</html>
