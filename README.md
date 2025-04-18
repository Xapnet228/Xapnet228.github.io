<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surpriză Muzicală!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        h1 {
            font-size: 3em;
        }
    </style>
</head>
<body>
    <div>
        <h1>🎵 SURPRIZĂ! 🎵</h1>
        <p>Muzica se redă la volum maxim!</p>
    </div>

    <audio id="myAudio" controls autoplay loop style="display: none;">
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Browser-ul tău nu suportă elementul audio.
    </audio>

    <script>
        window.onload = function() {
            var audio = document.getElementById("myAudio");
            audio.volume = 1.0; // Volum maxim (1.0 = 100%)
            audio.play().catch(e => console.log("Auto-play a fost blocat: " + e));
            
            // Încearcă să forțeze redarea după prima interacțiune
            document.body.addEventListener("click", function() {
                audio.play();
            });
        };
    </script>
</body>
</html>
