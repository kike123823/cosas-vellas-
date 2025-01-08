<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta Animada</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom, #f0f8ff, #e6e6fa);
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        .container {
            position: relative;
            text-align: center;
        }

        .letter-container {
            position: relative;
            width: 300px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            padding: 20px;
            text-align: center;
            display: none;
        }

        .letter-container.active {
            display: block;
        }

        .letter-container h1 {
            font-size: 1.6rem;
            color: #ff69b4;
            margin-bottom: 15px;
        }

        .letter-container p {
            font-size: 1rem;
            color: #555;
            line-height: 1.6;
            margin: 10px 0;
        }

        .signature {
            margin-top: 20px;
            font-style: italic;
            color: #ff69b4;
        }

        .button-container {
            margin-bottom: 20px;
        }

        .button img {
            width: 60px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .button img:hover {
            transform: scale(1.1);
        }

        .penguin {
            margin-top: 20px;
            width: 80px;
            animation: float 2s infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }

    </style>
    <script>
        function showLetter() {
            document.querySelector('.letter-container').classList.add('active');
            document.querySelector('.button-container').style.display = 'none';
        }
    </script>
</head>
<body>
    <div class="container">
        <!-- Botón con imagen del pingüino -->
        <div class="button-container">
            <img src="https://tse3.mm.bing.net/th?id=OIP.utKzM2MX3vWjcmIb0Cs3iwHaHa&pid=Api" 
                 alt="Pingüino con corazón" 
                 onclick="showLetter()" 
                 class="button">
        </div>

        <!-- Contenido de la carta -->
        <div class="letter-container">
            <h1>Hola Ojitos Dormilones </h1>
            <p>
                Espero que este mensaje te saque una sonrisa.
            </p>
            <p>
                Ahora un pequeño piropo para alegrarte aún más: ¿Sabes cuál es el ejercicio más efectivo para acelerar mi corazón? ¡Verte sonreír! Y vaya que funciona.
            </p>
            <div class="signature">
                Con cariño,<br>
                Tu admirador secreto
            </div>
            <!-- Imagen del pingüino animado -->
            <img src="https://tse3.mm.bing.net/th?id=OIP.utKzM2MX3vWjcmIb0Cs3iwHaHa&pid=Api" 
                 alt="Pingüino con corazón" 
                 class="penguin">
        </div>
    </div>
</body>
</html>
