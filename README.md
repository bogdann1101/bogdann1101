<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Întrebare pentru mama</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 100px;
        }
        h2 {
            font-size: 24px;
        }

        /* Butoane */
        .btn {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            transition: 0.3s;
        }

        #yesBtn {
            background-color: green;
            color: white;
        }

        #noBtn {
            background-color: red;
            color: white;
        }
    </style>
</head>
<body>

    <!-- Întrebarea -->
    <h2>Draga mea mamă, îmi iei BMW la 18 ani?</h2>
    
    <!-- Butoane -->
    <button id="yesBtn" class="btn" onclick="accept()">Da</button>
    <button id="noBtn" class="btn" onclick="increaseYes()">Nu</button>

    <script>
        let yesSize = 20; // Dimensiunea inițială a butonului "Da"

        function accept() {
            alert("Mulțumesc, mami! 🥰🚗💨");
        }

        function increaseYes() {
            yesSize += 10; // Creștem dimensiunea butonului "Da"
            document.getElementById("yesBtn").style.fontSize = yesSize + "px";
            document.getElementById("yesBtn").style.padding = (yesSize / 2) + "px " + (yesSize) + "px";
        }
    </script>

</body>
</html>
