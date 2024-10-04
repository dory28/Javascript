<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aventura em JavaScript</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; padding: 20px; }
        #game { background: white; padding: 20px; border-radius: 5px; }
    </style>
</head>
<body>
    <div id="game">
        <h1>Aventura na Floresta Encantada</h1>
        <p id="story"></p>
        <button id="choice1"></button>
        <button id="choice2"></button>
    </div>

    <script>
        let storyText = document.getElementById("story");
        let choice1Button = document.getElementById("choice1");
        let choice2Button = document.getElementById("choice2");

        function startGame() {
            storyText.innerText = "Você está em uma floresta encantada. Há dois caminhos à sua frente.";
            choice1Button.innerText = "Seguir pelo caminho da esquerda.";
            choice2Button.innerText = "Seguir pelo caminho da direita.";
            choice1Button.onclick = leftPath;
            choice2Button.onclick = rightPath;
        }

        function leftPath() {
            storyText.innerText = "Você encontrou uma fada que oferece ajuda mágica!";
            choice1Button.innerText = "Aceitar a ajuda.";
            choice2Button.innerText = "Recusar e continuar sozinho.";
            choice1Button.onclick = acceptHelp;
            choice2Button.onclick = continueAlone;
        }

        function rightPath() {
            storyText.innerText = "Você se depara com um dragão feroz!";
            choice1Button.innerText = "Tentar conversar com o dragão.";
            choice2Button.innerText = "Correr e tentar escapar.";
            choice1Button.onclick = talkToDragon;
            choice2Button.onclick = runAway;
        }

        function acceptHelp() {
            storyText.innerText = "A fada lhe deu uma poção mágica e você derrotou um inimigo! Você venceu!";
            choice1Button.style.display = "none";
            choice2Button.style.display = "none";
        }

        function continueAlone() {
            storyText.innerText = "Você se perdeu na floresta e nunca mais foi visto.";
            choice1Button.style.display = "none";
            choice2Button.style.display = "none";
        }

        function talkToDragon() {
            storyText.innerText = "O dragão se torna seu amigo e você voa por toda a floresta!";
            choice1Button.style.display = "none";
            choice2Button.style.display = "none";
        }

        function runAway() {
            storyText.innerText = "Você correu, mas tropeçou e caiu em um rio. O dragão te salvou!";
            choice1Button.style.display = "none";
            choice2Button.style.display = "none";
        }

        startGame();
    </script>
</body>
</html>
