<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Health Management Hub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            color: #333;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            background-color: #f2f2f2;
        }

        .background-image {
            background-image: url('health-background.jpg'); /* Replace with your image path */
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            position: relative;
        }

        .registration-form {
            background-color: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 400px;
            margin: 20px;
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            color: #4caf50;
        }

        h2 {
            margin: 0 0 20px;
            color: #4caf50;
        }

        label {
            margin-top: 10px;
            display: block;
            color: #555;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #45a049;
        }

        .main-content {
            display: none; /* Initially hidden */
            margin-top: 20px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 800px;
            text-align: center;
            margin: 20px auto;
        }

        nav {
            background-color: #4caf50;
            padding: 10px;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 0;
            margin: 0;
        }

        nav ul li {
            margin: 0 1rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #ddd;
        }

        .section {
            margin: 2rem 0;
            padding: 1rem;
            background: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .section h2 {
            color: #4caf50;
        }

        .advice-box {
            margin-bottom: 1rem;
            padding: 10px;
            border: 1px solid #4caf50;
            border-radius: 5px;
            background-color: #e8f5e9;
        }

        footer {
            text-align: center;
            padding: 1rem 0;
            background: #333;
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <div class="background-image">
        <h1>Welcome to Health Management Hub</h1>
        <p>Your companion for physical and mental wellness.</p>
        <div class="registration-form" id="registration">
            <h2>Get Started</h2>
            <form id="regForm">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>

                <button type="submit">Register</button>
            </form>
        </div>
    </div>

    <div class="main-content" id="mainContent">
        <header>
            <h1>Health Management Hub</h1>
            <p>Your companion for physical and mental wellness</p>
        </header>

        <nav>
            <ul>
                <li><a href="#advice">Personalized Advice</a></li>
                <li><a href="#tools">Wellness Tools</a></li>
                <li><a href="#tracking">Mood Tracking</a></li>
                <li><a href="#reminders">Reminders</a></li>
            </ul>
        </nav>

        <main>
            <!-- Section: Personalized Advice -->
            <section id="advice" class="section">
                <h2>Personalized Advice</h2>
                <div id="advice-container">
                    <div class="advice-box">
                        <h3>Diet</h3>
                        <p id="diet-advice">Include more fruits and vegetables in your meals. Aim for a balanced diet rich in nutrients.</p>
                    </div>
                    <div class="advice-box">
                        <h3>Exercise</h3>
                        <p id="exercise-advice">Engage in at least 30 minutes of moderate exercise most days. Try walking, jogging, or cycling.</p>
                    </div>
                    <div class="advice-box">
                        <h3>Sleep</h3>
                        <p id="sleep-advice">Prioritize sleep by creating a bedtime routine and aiming for 7-9 hours of quality sleep each night.</p>
                    </div>
                    <div class="advice-box">
                        <h3>Stress Management</h3>
                        <p id="stress-advice">Practice mindfulness, yoga, or meditation to help manage stress effectively.</p>
                    </div>
                </div>
            </section>

            <!-- Section: Wellness Tools -->
            <section id="tools" class="section">
                <h2>Wellness Tools</h2>
                <div class="tool">
                    <h3>Mindfulness Activities</h3>
                    <button id="mindfulness-btn">Start a Mindfulness Session</button>
                    <p id="mindfulness-activity">Activity will appear here...</p>
                </div>
                <div class="tool">
                    <h3>Motivational Quotes</h3>
                    <button id="quote-btn">Show a Motivational Quote</button>
                    <p id="motivational-quote">Your quote will appear here...</p>
                </div>
            </section>

            <!-- Section: Mood Tracking -->
            <section id="tracking" class="section">
                <h2>Mood Tracking</h2>
                <label for="mood">How are you feeling today?</label>
                <select id="mood">
                    <option value="happy">Happy</option>
                    <option value="neutral">Neutral</option>
                    <option value="sad">Sad</option>
                    <option value="stressed">Stressed</option>
                </select>
                <button id="track-mood-btn">Track Mood</button>
                <p id="mood-response">Your mood will be recorded here...</p>
            </section>

            <!-- Section: Reminders -->
            <section id="reminders" class="section">
                <h2>Reminders</h2>
                <label for="reminder-time">Set Reminder Time:</label>
                <input type="time" id="reminder-time">
                <button id="set-reminder-btn">Set Reminder</button>
                <p id="reminder-status">Reminder status will be updated here...</p>
            </section>
        </main>

        <footer>
            <p>&copy; 2025 Health Management Hub</p>
        </footer>
    </div>

    <script>
        // Show main content after registration
        document.getElementById("regForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent form submission
            document.getElementById("registration").style.display = "none"; // Hide registration form
            document.getElementById("mainContent").style.display = "block"; // Show main content
        });

        // Wellness Tools Functionality
        document.getElementById("mindfulness-btn").addEventListener("click", function() {
            const activities = [
                "Take a deep breath and focus on the present moment.",
                "Listen to a calming sound for 5 minutes.",
                "Spend a minute being aware of your surroundings."
            ];
            const randomActivity = activities[Math.floor(Math.random() * activities.length)];
            document.getElementById("mindfulness-activity").innerText = randomActivity;
        });

        document.getElementById("quote-btn").addEventListener("click", function() {
            const quotes = [
                "The greatest wealth is health.",
                "Take care of your body. It's the only place you have to live.",
                "Health is not just about what you're eating. It's also about what you're thinking and saying.",
                "Your body is your most priceless possession. Take care of it."
            ];
            const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
            document.getElementById("motivational-quote").innerText = randomQuote;
        });

        // Mood Tracking Functionality
        document.getElementById("track-mood-btn").addEventListener("click", function() {
            const mood = document.getElementById("mood").value;
            document.getElementById("mood-response").innerText = `Your mood today is recorded as: ${mood}`;
        });

        // Reminders Functionality
        document.getElementById("set-reminder-btn").addEventListener("click", function() {
            const time = document.getElementById("reminder-time").value;
            document.getElementById("reminder-status").innerText = `Reminder set for: ${time}`;
        });
    </script>
</body>
</html>
