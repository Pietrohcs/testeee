<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PRISON BREAKOUT — Jogo 2D</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="cabecalho">
        <h1>PRISON BREAKOUT</h1>
        <p class="subtitulo">Atravesse as 3 alas de segurança máxima e encontre uma maneira de escapar!</p>
    </header>

    <main class="container">
        <div class="area-jogo">
            <canvas id="gameCanvas" width="800" height="450"></canvas>
        </div>

        <section class="painel-info">
            <div class="card">
                <h2>Como Jogar</h2>
                <p>
                    Use <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> ou as <strong>Setas do Teclado</strong> para movimentar o prisioneiro pela cela.
                </p>
                <ul class="lista-regras">
                    <li><strong>Objetivo:</strong> Pegue a chave dourada para destrancar as grades e saia pelo topo.</li>
                    <li><strong>Cuidado:</strong> Os guardas perseguem você e aceleram quando o alarme toca! Use os móveis como cobertura.</li>
                    <li><strong>Segredo Nível 3:</strong> Encoste no símbolo do <strong>IFSP</strong> para congelar os guardas por 2 segundos.</li>
                    <li><strong>Atalhos:</strong> <kbd>ESPAÇO</kbd> inicia e <kbd>R</kbd> reinicia a partida.</li>
                </ul>
            </div>

            <div class="card">
                <h2>Equipe de Desenvolvimento</h2>
                <p class="descricao-turma">Projeto Integrador — IFSP Campus Itapetininga</p>
                <ul class="lista-equipe">
                    <li>
                        <span class="nome">Pietro</span>
                        <span class="papel">Programação de Lógica e Física</span>
                    </li>
                    <li>
                        <span class="nome">Wendel</span>
                        <span class="papel">Game Design e Arte Digital</span>
                    </li>
                    <li>
                        <span class="nome">Luiz Miguel</span>
                        <span class="papel">Programação de Estado e Interface</span>
                    </li>
                </ul>
            </div>
        </section>
    </main>

    <footer class="rodape">
        <p>Desenvolvido com HTML5, CSS3 e JavaScript (Canvas API) • 2026</p>
    </footer>

    <script src="game.js"></script>
</body>
</html>


* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    background-color: #121316;
    color: #f1f3f5;
    font-family: 'Segoe UI', Arial, sans-serif;
    line-height: 1.6;
}

.cabecalho {
    padding: 25px 15px 15px;
    text-align: center;
}

.cabecalho h1 {
    color: #e63946;
    font-size: 2.4rem;
    letter-spacing: 3px;
    text-transform: uppercase;
    text-shadow: 0 2px 10px rgba(230, 57, 70, 0.4);
}

.subtitulo {
    color: #adb5bd;
    font-size: 1rem;
    margin-top: 6px;
}

.container {
    max-width: 820px;
    margin: 0 auto;
    padding: 10px;
}

.area-jogo {
    display: flex;
    justify-content: center;
    margin-bottom: 24px;
}

canvas {
    background-color: #26282b;
    border: 3px solid #dee2e6;
    border-radius: 6px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.7);
    max-width: 100%;
    height: auto;
}

.painel-info {
    display: grid;
    grid-template-columns: 1.3fr 1fr;
    gap: 20px;
    margin-bottom: 30px;
}

.card {
    background-color: #1b1d22;
    border: 1px solid #2e323b;
    border-radius: 8px;
    padding: 20px;
    text-align: left;
}

.card h2 {
    color: #ff4d4d;
    font-size: 1.25rem;
    margin-bottom: 12px;
    border-bottom: 1px solid #2e323b;
    padding-bottom: 8px;
}

.lista-regras {
    margin-top: 12px;
    padding-left: 18px;
    color: #ced4da;
    font-size: 0.92rem;
}

.lista-regras li {
    margin-bottom: 8px;
}

kbd {
    background-color: #2b2f38;
    border: 1px solid #495057;
    border-bottom-width: 3px;
    border-radius: 4px;
    color: #ffd60a;
    font-family: monospace;
    font-size: 0.9rem;
    font-weight: bold;
    padding: 2px 6px;
}

.descricao-turma {
    color: #868e96;
    font-size: 0.88rem;
    margin-bottom: 12px;
}

.lista-equipe {
    list-style: none;
}

.lista-equipe li {
    background-color: #14161a;
    border-left: 3px solid #e63946;
    border-radius: 4px;
    margin-bottom: 10px;
    padding: 8px 12px;
}

.lista-equipe .nome {
    display: block;
    font-weight: bold;
    color: #ffffff;
}

.lista-equipe .papel {
    display: block;
    font-size: 0.85rem;
    color: #adb5bd;
}

.rodape {
    text-align: center;
    color: #6c757d;
    font-size: 0.85rem;
    padding: 15px;
    border-top: 1px solid #1f2228;
}

@media (max-width: 720px) {
    .painel-info {
        grid-template-columns: 1fr;
    }
}
