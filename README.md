<!DOCTYPE html>
<html>
<head>
    <title>RELÓGIO</title>
    <style>
        body { 
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #relogio {
            font-size: 48px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>RELOGIO</h1>
    <h2>TESTE 02</h2>
    <div id="relogio">--:--:--</div>

    <script>
        function atualizar() {
            const data = new Date();
            const horas = data.getHours().toString().padStart(2, '0');
            const minutos = data.getMinutes().toString().padStart(2, '0');
            const segundos = data.getSeconds().toString().padStart(2, '0');
            
            document.getElementById("relogio").textContent = 
                `${horas}:${minutos}:${segundos}`;
        }
        
        atualizar();
        setInterval(atualizar, 1000);
    </script>
</body>
</html>
