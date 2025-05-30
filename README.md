<!DOCTYPE html>
<html>
<head>
    <title>Relógio Digital</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #000;
            font-family: 'Arial', sans-serif;
        }
        #relogio {
            font-size: 5rem;
            color: #0f0;
            text-shadow: 0 0 10px #0f0;
        }
    </style>
</head>
<body>
    <div id="relogio"></div>

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
