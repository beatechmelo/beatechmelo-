<!--# ⏰ Projeto: Relógio Digital

Este é um projeto simples de um relógio digital criado com HTML, CSS e JavaScript.

---

## 🧾 Código HTML completo

```html-->
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Relógio Digital</title>
  <style>
    body {
      background-color: #000;
      color: #ff1493;
      font-family: Arial, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    .clock-container {
      background: rgba(255, 255, 255, 0.1);
      padding: 20px 40px;
      border-radius: 10px;
      box-shadow: 0 0 30px rgba(255, 255, 255, 0.7);
    }

    #clock {
      font-size: 3rem;
      letter-spacing: 2px;
      text-align: center;
      border: 1px solid white; /* Para teste */
    }
  </style>
</head>
<body>
  <div class="clock-container">
    <h1 id="clock">00:00:00</h1>
  </div>

  <script>
    window.addEventListener("DOMContentLoaded", () => {
      function updateClock() {
        const now = new Date();
        const horas = now.getHours().toString().padStart(2, "0");
        const minutos = now.getMinutes().toString().padStart(2, "0");
        const segundos = now.getSeconds().toString().padStart(2, "0");

        document.getElementById("clock").textContent = `${horas}:${minutos}:${segundos}`;
      }

      setInterval(updateClock, 1000);
      updateClock();
    });
  </script>
</body>
</html>
