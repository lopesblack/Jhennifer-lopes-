
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Estamos Juntos</title>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Arial', sans-serif;
      text-align: center;
      color: #ffffff;
      background: url('https://a.imagem.app/BzIhAt.jpeg') no-repeat center center fixed;
      background-size: cover;
      overflow-x: hidden;
    }

    h1 {
      font-size: 36px;
      margin-top: 50px;
      text-shadow: 2px 2px 4px #000000;
    }

    #contador {
      font-size: 48px;
      margin: 20px 0;
      text-shadow: 2px 2px 6px #000000;
    }

    .galeria {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 30px;
      padding: 20px;
      z-index: 1;
      position: relative;
    }

    .imagem-amor {
      max-width: 280px;
      border-radius: 12px;
      animation: pulse 2s infinite;
      box-shadow: 0 6px 15px rgba(0,0,0,0.6);
    }

    .frase {
      font-size: 22px;
      font-style: italic;
      text-shadow: 1px 1px 4px #000000;
      max-width: 600px;
      margin: 10px auto;
      padding: 0 15px;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.03); }
      100% { transform: scale(1); }
    }

    .heart {
      position: fixed;
      top: -60px;
      color: #add8e6;
      font-size: 48px;
      text-shadow: 0 0 15px rgba(173, 216, 230, 0.9), 0 0 25px rgba(173, 216, 230, 0.7);
      animation: fall linear infinite;
      z-index: 0;
      pointer-events: none;
    }

    @keyframes fall {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body> <audio id="somClique">
  <source src="https://www.soundjay.com/buttons/sounds/button-16.mp3" type="audio/mpeg">
</audio>

  <h1>Estamos juntos há...</h1>
  <div id="contador"></div>

  <div class="galeria">
    <div class="frase">"Mesmo longe, meu coração nunca deixou de te abraçar."</div>
    <img class="imagem-amor" src="https://a.imagem.app/BzIGT1.jpeg" alt="Foto 1">
<img class="imagem-amor" src="..." onclick="tocarSom()">
    <div class="frase">"A saudade aperta, mas é ela que me mostra o quanto você é essencial."</div>
    <img class="imagem-amor" src="https://a.imagem.app/BzIHZW.jpeg" alt="Foto 2">
<img class="imagem-amor" src="..." onclick="tocarSom()">
    <div class="frase">"Cada dia longe de você é mais um passo pra te encontrar de novo."</div>
    <img class="imagem-amor" src="https://a.imagem.app/BzIBHQ.jpeg" alt="Foto 3">

    <div class="frase">"Distância nenhuma é capaz de diminuir o que sinto por você."</div>
  </div>

  <script>
  const dataInicio = new Date("2025-03-07T00:00:00");

  function atualizarContador() {
    const agora = new Date();
    const diff = agora - dataInicio;

    const dias = Math.floor(diff / (1000 * 60 * 60 * 24));
    const horas = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutos = Math.floor((diff / (1000 * 60)) % 60);
    const segundos = Math.floor((diff / 1000) % 60);

    document.getElementById("contador").textContent =
      `${dias} dias, ${horas}h ${minutos}m ${segundos}s`;
  }

  setInterval(atualizarContador, 1000);
  atualizarContador(1000);
</script>
   
  </script>
<script>
  function tocarSom() {
    const som = document.getElementById("somClique");
    som.currentTime = 0;
    som.play();
  }
</script>
</body>
</html>
