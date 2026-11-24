<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Prison Breakout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- TELA INICIAL -->
    <div id="telaInicial">
        <h1>PRISON BREAKOUT</h1>
        <p>Você está preso e precisa escapar por 3 alas da prisão sem ser pego pelos guardas!</p>

        <button class="btn-vermelho" onclick="jogarAgora()">Jogar Agora</button>
        <button class="btn-cinza" onclick="abrirTutorial()">Como Jogar</button>

        <!-- TUTORIAL (começa escondido) -->
        <div id="tutorial" style="display: none;">
            <h2>Como Jogar</h2>
            <p><strong>Movimento:</strong> Use W, A, S, D ou as Setas do teclado.</p>
            <p><strong>Objetivo:</strong> Pegue a chave dourada e saia pela porta no topo.</p>
            <p><strong>Cuidado:</strong> Não encoste nos guardas. Use os móveis para fugir deles.</p>
            <p><strong>Bônus Nível 3:</strong> Encoste no símbolo do IFSP para congelar os guardas por 2 segundos.</p>
            <p><strong>Reiniciar:</strong> Aperte R para jogar de novo.</p>
        </div>

        <p class="creditos">
            Desenvolvido por: Pietro, Wendel e Luiz Miguel — IFSP 2026
        </p>
    </div>

    <!-- TELA DO JOGO (começa escondida) -->
    <div id="telaJogo" style="display: none;">
        <h1>PRISON BREAKOUT</h1>
        <canvas id="gameCanvas" width="800" height="450"></canvas>
        <br>
        <button class="btn-cinza" onclick="voltarMenu()">Voltar ao Início</button>
    </div>

    <script src="game.js"></script>
    <script>
        function jogarAgora() {
            document.getElementById("telaInicial").style.display = "none";
            document.getElementById("telaJogo").style.display = "block";
            reiniciarJogo();
        }

        function voltarMenu() {
            document.getElementById("telaJogo").style.display = "none";
            document.getElementById("telaInicial").style.display = "block";
            estadoJogo = "MENU";
        }

        function abrirTutorial() {
            let caixa = document.getElementById("tutorial");
            if (caixa.style.display === "none") {
                caixa.style.display = "block";
            } else {
                caixa.style.display = "none";
            }
        }
    </script>
</body>
</html>

body {
    background-color: #151515;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 20px;
}

#telaInicial {
    width: 600px;
    margin: 60px auto;
}

h1 {
    color: #e63946;
    font-size: 38px;
}

p {
    font-size: 16px;
    color: #dddddd;
}

button {
    padding: 12px 24px;
    font-size: 16px;
    font-weight: bold;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin: 10px 5px;
}

.btn-vermelho {
    background-color: #e63946;
    color: white;
}

.btn-cinza {
    background-color: #333333;
    color: white;
}

#tutorial {
    background-color: #222222;
    border: 1px solid #444444;
    padding: 15px;
    margin-top: 20px;
    text-align: left;
}

#tutorial h2 {
    color: #e63946;
    margin-top: 0;
}

.creditos {
    margin-top: 40px;
    font-size: 13px;
    color: #888888;
}

canvas {
    background-color: #303030;
    border: 3px solid white;
    margin-bottom: 10px;
}
