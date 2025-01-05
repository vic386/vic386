!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>eye.hacking</title>
    <style>
        body {
            background-color: #0d0d0d; /* Fundo bem mais escuro */
            color: #FF0000; /* Cor vermelha */
            font-family: 'Courier New', Courier, monospace;
            text-align: center;
            padding: 50px;
            overflow: hidden;
        }
        h1 {
            font-size: 100px;
            color: #FF0000;
            margin-bottom: 30px;
            text-shadow: 0 0 10px #FF0000, 0 0 20px #FF0000;
        }
        .eye {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background-color: #FF0000;
            margin: 20px auto;
            position: relative;
        }
        .eye::after {
            content: '';
            position: absolute;
            top: 30%;
            left: 30%;
            width: 40px;
            height: 40px;
            background-color: #000;
            border-radius: 50%;
            box-shadow: 0 0 10px #FF0000;
        }
        .hidden-text {
            visibility: hidden; /* Começa invisível */
            opacity: 0; /* Começa invisível */
            transition: opacity 2s ease-in-out; /* Efeito suave */
            font-size: 14px;
            color: #FF0000; /* Texto em vermelho */
            margin-top: 20px;
            text-shadow: 0 0 5px #FF0000, 0 0 10px #FF0000;
        }
        .emoji {
            font-size: 60px;
            cursor: pointer;
            margin-top: 30px;
        }
    </style>
</head>
<body>

    <!-- Olho Vermelho -->
    <div class="eye"></div>

    <!-- Emoji do boneco no computador -->
    <div class="emoji" id="emoji">&#128187;</div>

    <!-- Texto invisível que aparece após clicar no emoji -->
    <p class="hidden-text" id="hiddenText">
        Desisto de ser natural. Vô é tomar bomba.
    </p>

    <script>
        const hiddenText = document.getElementById('hiddenText');
        const emoji = document.getElementById('emoji');

        // Função que revela o texto após clicar no emoji
        function revealText() {
            hiddenText.style.visibility = 'visible'; // Torna o texto visível
            hiddenText.style.opacity = '1'; // Aparece suavemente
        }

        // Adicionando evento de clique no emoji
        emoji.addEventListener('click', revealText);
    </script>

</body>
</html>
