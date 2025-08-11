# ⏰ Projeto: Relógio Digital

Este é um projeto simples de um relógio digital criado com HTML, CSS e JavaScript.

---

## 🧾 Especificações Técnicas

Criar um relógio digital funcional que:

- Exibe a hora atual em tempo real (HH:MM:SS);
- Atualiza automaticamente a cada segundo;
- É exibido de forma centralizada e responsiva na tela;
- Possui estilo visual moderno, com fundo escuro e destaque para os números.

---

## 💻 Tecnologias utilizadas:

- HTML5;
- CSS3 (com flexbox e sombras);
- JavaScript (funções de data e intervalos com `setInterval`).

---

## 📚 O que aprendi:

- **Manipulação do DOM**: usar `getElementById` e atualizar conteúdo HTML dinamicamente.
- **Funções de tempo**: aplicar `Date()` para capturar hora atual e `setInterval()` para atualizações contínuas.
- **Formatação de strings**: usar `.padStart()` para garantir que os números fiquem sempre com dois dígitos.
- **Estilização com CSS moderno**: aplicar sombras, cores contrastantes e centralização com Flexbox.
- **Boas práticas de estruturação**: separar lógica em funções e manter o HTML limpo e sem elementos desnecessários.

---

## 🛠️ Como usar:

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/relogio-digital.git
##

## 🧾 Código HTML completo

```html
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
