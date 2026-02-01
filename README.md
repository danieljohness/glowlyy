<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glow Up Life System</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Glow Up Life System</h1>
        <nav>
            <ul>
                <li><a href="#program">Program Zilnic</a></li>
                <li><a href="#hidratare">Hidratare</a></li>
                <li><a href="#somn">Somn</a></li>
                <li><a href="#sport">Sport</a></li>
                <li><a href="#nutritie">Nutriție</a></li>
                <li><a href="#questuri">Questuri</a></li>
                <li><a href="#skilltree">Skill Tree</a></li>
                <li><a href="#progres">Progres</a></li>
                <li><a href="#shop">Shop</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="program">
            <h2>Program Zilnic</h2>
            <form id="daily-schedule">
                <label for="wake-up">Trezire:</label>
                <input type="time" id="wake-up" required>
                <label for="sleep">Somn:</label>
                <input type="time" id="sleep" required>
                <label for="gym">Sală:</label>
                <input type="time" id="gym">
                <label for="cardio">Cardio:</label>
                <input type="time" id="cardio">
                <label for="meals">Mese:</label>
                <input type="text" id="meals" placeholder="Ex: Mic dejun, Prânz, Cină">
                <button type="submit">Salvează Programul</button>
            </form>
        </section>

        <section id="hidratare">
            <h2>Hidratare</h2>
            <input type="number" id="weight" placeholder="Greutate (kg)" required>
            <button id="calculate-water">Calcul Apă</button>
            <p id="water-intake"></p>
        </section>

        <section id="somn">
            <h2>Somn</h2>
            <input type="number" id="sleep-hours" placeholder="Ore de somn" required>
            <button id="track-sleep">Urmărește Somnul</button>
            <p id="sleep-score"></p>
        </section>

        <section id="sport">
            <h2>Sport</h2>
            <button id="log-exercise">Loghează Exercițiu</button>
        </section>

        <section id="nutritie">
            <h2>Nutriție</h2>
            <button id="log-nutrition">Loghează Nutriție</button>
        </section>

        <section id="questuri">
            <h2>Questuri Zilnice</h2>
            <ul id="daily-quests"></ul>
        </section>

        <section id="skilltree">
            <h2>Skill Tree</h2>
            <div id="skill-tree"></div>
        </section>

        <section id="progres">
            <h2>Progres</h2>
            <div id="progress-calendar"></div>
        </section>

        <section id="shop">
            <h2>Shop</h2>
            <button id="open-shop">Deschide Shop</button>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 Glow Up Life System. Toate drepturile rezervate.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #121212;
    color: #ffffff;
}

header {
    background-color: #1e1e1e;
    padding: 20px;
    text-align: center;
}

nav ul {
    list-style-type: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: #00ffcc;
    text-decoration: none;
}

section {
    margin: 20px;
    padding: 20px;
    border: 1px solid #00ffcc;
    border-radius: 5px;
}

button {
    background-color: #00ffcc;
    color: #121212;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
}

button:hover {
    background-color: #00cc99;
}
document.getElementById('daily-schedule').addEventListener('submit', function(event) {
    event.preventDefault();
    // Logica pentru salvarea programului zilnic
});

document.getElementById('calculate-water').addEventListener('click', function() {
    const weight = document.getElementById('weight').value;
    const waterIntake = weight * 30; // ml
    document.getElementById('water-intake').innerText = `Trebuie să bei ${waterIntake} ml de apă pe zi.`;
});

document.getElementById('track-sleep').addEventListener('click', function() {
    const sleepHours = document.getElementById('sleep-hours').value;
    const sleepScore = sleepHours * 10; // Exemplu de calcul
    document.getElementById('sleep-score').innerText = `Scorul tău de somn este ${sleepScore}.`;
});
