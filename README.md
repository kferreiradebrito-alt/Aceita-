<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aceira meu pedido?</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #ff7a7a, #ff4757);
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.2);
            max-width: 400px;
            width: 90%;
        }

        h1 {
            color: #ff4757;
            font-size: 26px;
            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            position: relative;
            height: 50px;
        }

        button {
            padding: 12px 30px;
            font-size: 18px;
            font-weight: bold;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: 0.2s;
        }

        #sim {
            background-color: #2ed573;
            color: white;
            box-shadow: 0 4px 15px rgba(46, 213, 115, 0.4);
        }

        #sim:hover {
            background-color: #26af5f;
            transform: scale(1.05);
        }

        #nao {
            background-color: #ff4757;
            color: white;
            position: absolute;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Aceita me dar o cuzinho esse final de semana? ❤️</h1>
        <div class="buttons">
            <button id="sim" onclick="aceitou()">SIM</button>
            <button id="nao" onmouseover="moverBotao()" onclick="moverBotao()">NÃO</button>
        </div>
    </div>

    <script>
        function moverBotao() {
            const botaoNao = document.getElementById('nao');
            const larguraJanela = window.innerWidth - botaoNao.offsetWidth;
            const alturaJanela = window.innerHeight - botaoNao.offsetHeight;
            
            const aleatorioX = Math.floor(Math.random() * larguraJanela);
            const aleatorioY = Math.floor(Math.random() * alturaJanela);
            
            botaoNao.style.position = 'fixed';
            botaoNao.style.left = `${aleatorioX}px`;
            botaoNao.style.top = `${aleatorioY}px`;
        }

        function aceitou() {
            alert('Eba! Você aceitou, obrigado por liberar o peidante te amo! ❤️💍');
            // Você pode redirecionar para uma música ou página especial aqui, se quiser
        }
    </script>

</body>
</html>

