<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Cobra Kai – Sekai Taikai</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            min-height: 100vh;
            background: #050505;
            color: white;
            font-family: Arial, sans-serif;

            display: flex;
            justify-content: center;
            align-items: center;

            padding: 20px;
        }

        .box {
            width: 100%;
            max-width: 450px;

            background: #111;
            border: 2px solid #b00000;
            border-radius: 15px;

            padding: 35px 25px;

            text-align: center;

            box-shadow: 0 0 35px rgba(180, 0, 0, 0.4);
        }

        .logo {
            width: 230px;
            max-width: 80%;
            margin-bottom: 25px;
        }

        h1 {
            color: #e00000;
            font-size: 28px;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        .subtitle {
            color: #aaa;
            margin-bottom: 30px;
            font-size: 16px;
        }

        input {
            width: 100%;
            padding: 15px;
            margin-bottom: 12px;

            background: #222;
            border: 1px solid #555;
            border-radius: 8px;

            color: white;
            font-size: 16px;
        }

        input:focus {
            outline: none;
            border-color: #e00000;
        }

        button {
            width: 100%;
            padding: 15px;

            background: #c00000;
            color: white;

            border: none;
            border-radius: 8px;

            font-size: 17px;
            font-weight: bold;

            cursor: pointer;
        }

        button:hover {
            background: #e00000;
        }

        #welcome {
            display: none;
        }

        .welcome {
            font-size: 25px;
            color: #e00000;
            margin-bottom: 15px;
        }

        .name {
            font-size: 20px;
            margin-bottom: 20px;
        }
    </style>
</head>

<body>

    <div class="box">

        <!-- COBRA KAI LOGO -->
        <img 
            src="cobra-kai-logo.png" 
            alt="Cobra Kai Logo" 
            class="logo"
        >

        <!-- ANMELDUNG -->
        <div id="login">

            <h1>Anmeldung für das Sekai Taikai</h1>

            <p class="subtitle">
                Melde dich für das Turnier an.
            </p>

            <input 
                type="text" 
                id="vorname" 
                placeholder="Vorname"
            >

            <input 
                type="text" 
                id="nachname" 
                placeholder="Nachname"
            >

            <button onclick="anmelden()">
                ANMELDEN
            </button>

        </div>

        <!-- WILLKOMMEN -->
        <div id="welcome">

            <div class="welcome">
                Anmeldung erfolgreich!
            </div>

            <div class="name" id="name"></div>

            <p>
                Du bist für das Sekai Taikai angemeldet.
            </p>

        </div>

    </div>

    <script>

        function anmelden() {

            const vorname = document.getElementById("vorname").value.trim();
            const nachname = document.getElementById("nachname").value.trim();

            if (vorname === "" || nachname === "") {
                alert("Bitte gib deinen Vor- und Nachnamen ein.");
                return;
            }

            document.getElementById("name").innerHTML =
                vorname + " " + nachname;

            document.getElementById("login").style.display = "none";
            document.getElementById("welcome").style.display = "block";
        }

    </script>

</body>
</html>
