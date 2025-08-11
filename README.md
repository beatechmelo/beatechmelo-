# Relógio Digital ⏰

Projeto simples de um relógio digital feito com HTML, CSS e JavaScript.

---

### 💻 Código HTML

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Relógio Digital</title>
  <style>
    body {
      background-color: #0f172a;
      color: #fff;
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
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    }

    #clock {
      font-size: 3rem;
      letter-spacing: 2px;
      text-align: center;
      border: 1px solid red; /* Para teste */
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
        const hours = now.getHours().toString().padStart(2, "0");
        const minutes = now.getMinutes().toString().padStart(2, "0");
        const seconds = now.getSeconds().toString().padStart(2, "0");

        document.getElementById("clock").textContent = `${hours}:${minutes}:${seconds}`;
      }

      setInterval(updateClock, 1000);
      updateClock();
    });
  </script>
</body>
</html>
git init
git add .
git commit -m "Primeiro commit do relógio"
git remote add origin https://github.com/beatechmelo/relogio-digital.git
git branch -M main
git push -u origin main
