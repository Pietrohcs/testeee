<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prison Breakout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Topo / Apresentação -->
    <header class="topo">
        <h1>PRISON BREAKOUT</h1>
        <p>Você está preso e precisa escapar por 3 alas da prisão sem ser pego pelos guardas.</p>
        <div class="botoes">
            <a href="#jogo" class="btn-jogar" onclick="reiniciarJogo()">Jogar Agora</a>
            <a href="#como-jogar" class="btn-tutorial">Como Jogar</a>
        </div>
    </header>

    <!-- Tela do Jogo -->
    <main id="jogo" class="secao-jogo">
        <canvas id="gameCanvas" width="800" height="450"></canvas>
    </main>

    <!-- Tutorial Simples -->
    <section id="como-jogar" class="tutorial">
        <h2>Como Jogar (Tutorial)</h2>
        <p><strong>1. Movimentar:</strong> Use as teclas <strong>W, A, S, D</strong> ou as <strong>Setas</strong> do teclado.</p>
        <p><strong>2. Abrir a cela:</strong> Pegue a <strong>chave dourada</strong> no chão e corra até a saída no topo.</p>
        <p><strong>3. Despistar os guardas:</strong> Não encoste nos guardas! Use os móveis para bloquear o caminho deles.</p>
        <p><strong>4. Bônus do Nível 3:</strong> Passe por cima do símbolo do <strong>IFSP</strong> para congelar os guardas por 2 segundos.</p>
        <p><strong>Reiniciar:</strong> Se for capturado ou vencer, aperte <strong>R</strong> para jogar de novo.</p>
    </section>

    <!-- Créditos -->
    <footer class="rodape">
        <p><strong>Desenvolvido por:</strong> Pietro (Lógica e Física) • Wendel (Design e Arte) • Luiz Miguel (Interface)</p>
        <p>IFSP Campus Itapetininga — 2026</p>
    </footer>

    <script src="game.js"></script>
</body>
</html>

html {
    scroll-behavior: smooth;
}

body {
    background-color: #151515;
    color: #eeeeee;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
}

/* Topo / Landing Page */
.topo {
    max-width: 700px;
    margin: 30px auto 20px;
    padding: 0 15px;
}

.topo h1 {
    color: #e63946;
    font-size: 36px;
    margin-bottom: 10px;
}

.topo p {
    color: #cccccc;
    font-size: 16px;
    margin-bottom: 20px;
}

.botoes {
    margin-bottom: 10px;
}

.btn-jogar, .btn-tutorial {
    display: inline-block;
    padding: 10px 22px;
    margin: 5px;
    text-decoration: none;
    font-weight: bold;
    border-radius: 5px;
    font-size: 15px;
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

/* Canvas do Jogo */
.secao-jogo {
    margin: 20px auto;
}

canvas {
    background-color: #303030;
    border: 3px solid white;
    max-width: 95%;
}

/* Tutorial */
.tutorial {
    max-width: 760px;
    margin: 30px auto;
    padding: 20px;
    background-color: #1f1f1f;
    border: 1px solid #333333;
    border-radius: 6px;
    text-align: left;
}

.tutorial h2 {
    color: #e63946;
    margin-top: 0;
    margin-bottom: 15px;
    font-size: 22px;
}

.tutorial p {
    margin: 10px 0;
    font-size: 15px;
    line-height: 1.5;
}

/* Rodapé */
.rodape {
    margin: 30px 0 20px;
    color: #999999;
    font-size: 13px;
}
