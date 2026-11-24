<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prison Breakout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- TELA 1: PÁGINA INICIAL (Aparece primeiro, sem o jogo) -->
    <div id="tela-inicial" class="pagina-inicial">
        <h1>PRISON BREAKOUT</h1>
        <p class="descricao">
            Você é um prisioneiro tentando escapar de uma prisão de segurança máxima. 
            Atravesse 3 alas cada vez mais difíceis, pegue a chave de cada cela e fuja sem ser pego pelos guardas!
        </p>

        <div class="botoes">
            <button class="btn-jogar" onclick="abrirJogo()">Jogar Agora</button>
            <button class="btn-tutorial" onclick="mostrarTutorial()">Como Jogar</button>
        </div>

        <!-- Tutorial (abre/fecha ao clicar em Como Jogar) -->
        <div id="box-tutorial" class="tutorial" style="display: none;">
            <h2>Como Jogar (Tutorial)</h2>
            <p><strong>1. Movimentar:</strong> Use as teclas <strong>W, A, S, D</strong> ou as <strong>Setas</strong> do teclado.</p>
            <p><strong>2. Abrir a saída:</strong> Pegue a <strong>chave dourada</strong> no chão e vá até a porta no topo.</p>
            <p><strong>3. Fugir dos guardas:</strong> Não encoste nos guardas! Use os móveis para bloquear o caminho deles.</p>
            <p><strong>4. Bônus do Nível 3:</strong> Passe sobre o símbolo do <strong>IFSP</strong> para congelar os guardas por 2 segundos.</p>
            <p><strong>5. Reiniciar:</strong> Se perder ou vencer, aperte a tecla <strong>R</strong>.</p>
        </div>

        <footer class="rodape">
            <p><strong>Equipe:</strong> Pietro (Lógica e Física) • Wendel (Design e Arte) • Luiz Miguel (Interface)</p>
            <p>IFSP Campus Itapetininga — 2026</p>
        </footer>
    </div>

    <!-- TELA 2: ÁREA DO JOGO (Começa escondida e só aparece ao clicar em Jogar Agora) -->
    <div id="tela-jogo" class="area-jogo" style="display: none;">
        <div class="barra-topo-jogo">
            <h2>PRISON BREAKOUT</h2>
            <button class="btn-voltar" onclick="voltarInicio()">← Voltar ao Início</button>
        </div>

        <canvas id="gameCanvas" width="800" height="450"></canvas>
    </div>

    <script src="game.js"></script>
    <script>
        function abrirJogo() {
            document.getElementById("tela-inicial").style.display = "none";
            document.getElementById("tela-jogo").style.display = "block";
            reiniciarJogo(); // Já inicia o jogo direto no Nível 1
        }

        function voltarInicio() {
            document.getElementById("tela-jogo").style.display = "none";
            document.getElementById("tela-inicial").style.display = "block";
            estadoJogo = "MENU"; // Pausa o jogo enquanto estiver na tela inicial
        }

        function mostrarTutorial() {
            const box = document.getElementById("box-tutorial");
            if (box.style.display === "none") {
                box.style.display = "block";
            } else {
                box.style.display = "none";
            }
        }
    </script>
</body>
</html>

body {
    background-color: #151515;
    color: #eeeeee;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
}

/* Tela Inicial */
.pagina-inicial {
    max-width: 680px;
    margin: 70px auto 30px;
    padding: 20px;
}

.pagina-inicial h1 {
    color: #e63946;
    font-size: 42px;
    margin-bottom: 15px;
}

.descricao {
    color: #cccccc;
    font-size: 17px;
    line-height: 1.6;
    margin-bottom: 30px;
}

.botoes {
    margin-bottom: 25px;
}

button {
    cursor: pointer;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    font-weight: bold;
    padding: 12px 26px;
    margin: 6px;
}

.btn-jogar {
    background-color: #e63946;
    color: white;
}

.btn-jogar:hover {
    background-color: #c1121f;
}

.btn-tutorial {
    background-color: #2b2b2b;
    color: white;
    border: 1px solid #555555;
}

.btn-tutorial:hover {
    background-color: #3a3a3a;
}

/* Caixa do Tutorial */
.tutorial {
    background-color: #1f1f1f;
    border: 1px solid #333333;
    border-radius: 6px;
    margin: 20px auto;
    padding: 20px;
    text-align: left;
}

.tutorial h2 {
    color: #e63946;
    font-size: 20px;
    margin-top: 0;
    margin-bottom: 12px;
}

.tutorial p {
    font-size: 15px;
    line-height: 1.5;
    margin: 8px 0;
}

.rodape {
    color: #888888;
    font-size: 13px;
    margin-top: 50px;
}

/* Tela do Jogo */
.area-jogo {
    max-width: 820px;
    margin: 20px auto;
    padding: 10px;
}

.barra-topo-jogo {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 800px;
    margin: 0 auto 10px;
}

.barra-topo-jogo h2 {
    color: #e63946;
    margin: 0;
    font-size: 22px;
}

.btn-voltar {
    background-color: #2b2b2b;
    color: #eeeeee;
    border: 1px solid #555555;
    font-size: 14px;
    padding: 8px 14px;
    margin: 0;
}

.btn-voltar:hover {
    background-color: #3a3a3a;
}

canvas {
    background-color: #303030;
    border: 3px solid white;
    max-width: 100%;
}
