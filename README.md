
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bem-vindo ao Cason</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 10%; /* Ajustei para 10% para afastar mais o conteúdo do topo */
            background-image: url('Imagem_fundo_Cason.png'); /* Caminho da imagem */
            background-size: cover; /* Alterado para cover para que a imagem preencha a tela */
            background-position: center center; /* Centraliza a imagem na tela */
            background-repeat: no-repeat; /* Evita repetição da imagem */
            height: 100vh; /* Faz com que o fundo cubra 100% da altura da tela */
        }
        h1 {
            font-size: 36px;
            color: red; /* Altera a cor para vermelho */
            font-weight: bold; /* Define o texto como negrito */
            text-shadow: 3px 3px 0px #ccc, /* sombra mais clara */
                         6px 6px 0px #999, /* sombra intermediária */
                         9px 9px 0px #666; /* sombra mais escura */
        }
        p {
            font-size: 24px;
            color: red; /* Altera a cor para vermelho */
            font-weight: bold; /* Define o texto como negrito */
            text-shadow: 3px 3px 0px #ccc, /* sombra mais clara */
                         6px 6px 0px #999, /* sombra intermediária */
                         9px 9px 0px #666; /* sombra mais escura */
            margin-bottom: 30px;
        }
        label {
            font-size: 24px;
            color: red; /* Altera a cor para vermelho */
            font-weight: bold; /* Define o texto como negrito */
            text-shadow: 3px 3px 0px #ccc, /* sombra mais clara */
                         6px 6px 0px #999, /* sombra intermediária */
                         9px 9px 0px #666; /* sombra mais escura */
        }
        select {
            font-size: 18px;
            padding: 10px;
            width: 300px;
        }
        option {
            font-size: 18px;
        }
        /* Estilo do pato */
        .duck {
            position: absolute;
            bottom: 50px;
            width: 100px; /* Largura do pato */
            cursor: pointer; /* Define o cursor como pointer ao passar o mouse */
            animation: moveDuck 10s linear infinite;
        }
        /* Animação do pato se movendo */
        @keyframes moveDuck {
            0% { left: 0; transform: scaleX(1); } /* Começa da esquerda */
            50% { left: calc(100% - 100px); transform: scaleX(-1); } /* Vai para a direita e vira */
            100% { left: 0; transform: scaleX(1); } /* Volta para a esquerda */
        }
    </style>
    <script>
        // Função para redirecionar com base na seleção e abrir em nova aba
        function redirecionar() {
            var opcaoSelecionada = document.getElementById("opcoes").value;

            if (opcaoSelecionada === "1") {
                window.open("tutoriais.html", "_blank"); // Redireciona para a página do tutorial em nova aba
            } else if (opcaoSelecionada === "2") {
                window.open("duvidas.html", "_blank"); // Redireciona para a página de dúvidas em nova aba
            }
        }

        // Função que abre uma nova aba ao clicar no pato
        function abrirNovaAba() {
            window.open("https://sgbr.com.br", "_blank"); // Substitua o link com o URL desejado
        }
    </script>
</head>
<body>
    <h1>Olá, tudo bem? Aqui é o Cason!</h1>
    <p>Como posso ajudar?</p>

    <form onsubmit="event.preventDefault(); redirecionar();">
        <label for="opcoes">Escolha uma alternativa:</label><br><br>
        <select id="opcoes" name="opcoes">
            <option value="1">Preciso de um tutorial</option>
            <option value="2">Preciso tirar uma dúvida</option>
        </select>
        <br><br>
        <input type="submit" value="Enviar">
    </form>

    <!-- Adiciona o pato andando -->
    <img src="Pato_imagem_cason.png" alt="Pato fofo" class="duck" onclick="abrirNovaAba()">
</body>
</html>
