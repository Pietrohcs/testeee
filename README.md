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
