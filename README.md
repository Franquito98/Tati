<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para ti ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Comic Sans MS', cursive;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      color: #fff;
      text-align: center;
      overflow: hidden;
    }
    h1 {
      margin-top: 20vh;
      font-size: 3em;
      animation: fadeIn 3s ease-in-out;
    }
    p {
      font-size: 1.5em;
      margin: 20px;
    }
    .corazon {
      position: absolute;
      color: #ff0000;
      animation: flotar 10s linear infinite;
      font-size: 2em;
    }
    @keyframes flotar {
      0% {
        transform: translateY(100vh) scale(1);
        opacity: 0;
      }
      100% {
        transform: translateY(-10vh) scale(1.5);
        opacity: 1;
      }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      border: none;
      background: #fff;
      color: #ff007f;
      font-weight: bold;
      border-radius: 20px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Para ti, Tati hermosa ❤️</h1>
  <p id="mensaje">Cada día contigo es un regalo que atesoro. Te quiero mucho más de lo que puedo decir ❤️</p>
  <button onclick="cambiarMensaje()">Haz clic para una sorpresa</button>

  <script>
    const mensajes = [
      "Eres mi lugar feliz 🏡❤️",
      "Contigo, todo es mejor 💫",
      "Gracias por darme esta hermosa amistad 💓",
      "Eres la princesita más linda ✨"
    ];
    let index = 0;
    function cambiarMensaje() {
      index = (index + 1) % mensajes.length;
      document.getElementById("mensaje").textContent = mensajes[index];
    }

    // Animación de corazones
    setInterval(() => {
      const corazon = document.createElement("div");
      corazon.textContent = "❤️";
      corazon.className = "corazon";
      corazon.style.left = Math.random() * 100 + "vw";
      corazon.style.fontSize = Math.random() * 2 + 1 + "em";
      document.body.appendChild(corazon);
      setTimeout(() => corazon.remove(), 10000);
    }, 500);
  </script>
</body>
</html>
