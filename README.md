# Schnitzeljagt
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Schnitzeljagd</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .hint {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin: 20px auto;
            max-width: 600px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            background-color: #4CAF50;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <h1>Willkommen zur Schnitzeljagd!</h1>
    <div class="hint" id="hint-container">
        <p id="hint-text">Scanne den QR-Code, um den ersten Hinweis zu erhalten.</p>
    </div>
    <button onclick="nextHint()">Nächster Hinweis</button>

    <script>
        // Liste der Hinweise
        const hints = [
            "Erster Hinweis: Gehe zum großen Baum im Park.",
            "Zweiter Hinweis: Suche unter der Bank am Spielplatz.",
            "Dritter Hinweis: Finde den roten Briefkasten in der Nähe.",
            "Glückwunsch! Du hast den Schatz gefunden!"
        ];
        let currentHint = 0;

        // Funktion zum Anzeigen des nächsten Hinweises
        function nextHint() {
            if (currentHint < hints.length) {
                document.getElementById("hint-text").textContent = hints[currentHint];
                currentHint++;
            } else {
                alert("Die Schnitzeljagd ist vorbei!");
            }
        }
    </script>
</body>
</html>
