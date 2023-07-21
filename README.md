<!DOCTYPE html>
<html>
<head>
    <title>Você foi hackeado</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: "Courier New", monospace;
            text-align: center;
            padding-top: 100px;
        }

        button {
            padding: 10px 20px;
            background-color: #1a1a1a;
            border: none;
            color: white;
            font-size: 16px;
            cursor: pointer;
            margin: 5px;
        }

        button:hover {
            background-color: #333;
        }

        .mensagem {
            display: none;
            margin-top: 20px;
            color: green;
            font-size: 20px;
        }
    </style>
</head>
<body>
    <h1>Você foi hackeado</h1>
    <button onclick="mostrarMensagem()">Clique aqui</button>
    <div class="botoes" style="display: none;">
        <button onclick="mostrarMensagemFinal('sim')">Sim</button>
        <button onclick="mostrarMensagemFinal('nao')">Não</button>
    </div>

    <div class="mensagem" id="mensagemFinal"></div>

    <script>
        function mostrarMensagem() {
            var botao = document.querySelector('button');
            var botoes = document.querySelector('.botoes');

            botao.style.display = 'none';
            botoes.style.display = 'block';
        }

        function mostrarMensagemFinal(resposta) {
            var mensagemFinal = document.getElementById('mensagemFinal');
            var botoes = document.querySelector('.botoes');

            if (resposta === 'sim') {
                mensagemFinal.textContent = "Eu te amo tanto, minha princesa, minha deusa. Obrigado por aceitar meu pedido de namoro!";
            } else if (resposta === 'nao') {
                mensagemFinal.textContent = "Que pena! Mas obrigado mesmo assim por responder.";
            }

            mensagemFinal.style.display = 'block';
            botoes.style.display = 'none';
        }
    </script>
</body>
</html>
