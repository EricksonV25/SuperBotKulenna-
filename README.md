# SuperBotKulenna-
SuperBotKulenna- Painel de bot para negociação
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SuperBotKulenna</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>SuperBotKulenna</h1>
        <p>Seu painel de negociação automatizada</p>
    </header>
    <main>
        <!-- Conteúdo do painel, botões, gráficos, etc -->
        <div id="bot-status">Status do Bot: <span id="bot-status-text">Inativo</span></div>
        <div id="bot-actions">
            <button onclick="startBot()">Iniciar Bot</button>
            <button onclick="stopBot()">Parar Bot</button>
        </div>
        <div id="signals">
            <h2>Sinais de Negociação</h2>
            <div id="signal-info"></div>
        </div>
    </main>
    <footer>
        <p>SuperBotKulenna - Todos os direitos reservados</p>
    </footer>

    <script src="bot.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #fff;
    color: #333;
}

header {
    background-color: #f4f4f4;
    padding: 10px;
    text-align: center;
}

h1 {
    color: red;
}

#bot-status {
    margin: 20px;
}

#bot-actions button {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    margin: 10px;
}

#bot-actions button:hover {
    background-color: #45a049;
}

footer {
    text-align: center;
    margin-top: 30px;
    background-color: #f4f4f4;
    padding: 10px;
}

let botStatus = false;

function startBot() {
    botStatus = true;
    document.getElementById('bot-status-text').innerText = 'Ativo';
    document.getElementById('signal-info').innerText = 'Bot Iniciado. Gerando sinais de negociação...';
    // Lógica do Bot para iniciar negociações
}

function stopBot() {
    botStatus = false;
    document.getElementById('bot-status-text').innerText = 'Inativo';
    document.getElementById('signal-info').innerText = 'Bot Parado.';
    // Lógica para parar o bot
}
