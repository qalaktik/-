# Creating the HTML file with sections based on the user's requirements.
html_content = """
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Личный сайт о космосе</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            color: white;
            margin: 0;
            padding: 0;
            background: url('stars_background.jpg') no-repeat center center fixed;
            background-size: cover;
        }
        h1 {
            text-align: center;
            margin-top: 50px;
        }
        .content {
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .chat-section {
            margin-top: 50px;
        }
        #chatbox {
            width: 100%;
            height: 400px;
            background-color: #222;
            border: 2px solid #444;
            padding: 10px;
            overflow-y: scroll;
        }
        #user-input {
            width: 100%;
            padding: 10px;
            margin-top: 10px;
        }
        .footer {
            text-align: center;
            padding: 20px;
            background-color: #111;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        /* Dynamic background change every hour */
        @keyframes changeBackground {
            0% { background-image: url('stars_background.jpg'); }
            33% { background-image: url('jupiter_background.jpg'); }
            66% { background-image: url('mars_background.jpg'); }
            100% { background-image: url('spiral_galaxy.jpg'); }
        }
        body {
            animation: changeBackground 3600s infinite;
        }
    </style>
</head>
<body>
    <h1>Добро пожаловать на сайт о космосе!</h1>
    <div class="content">
        <section>
            <h2>О космосе</h2>
            <p>Космос — это невероятное пространство, которое исследуется людьми с помощью ракет и других технологий. Всего в космосе побывало около 600 человек, и каждый запуск ракеты становится важной вехой в исследовании Вселенной.</p>
            <p>Ракеты работают благодаря реактивным двигателям, которые создают силу тяги за счет сгорания топлива. Это позволяет им преодолевать силу земного притяжения и выходить на орбиту.</p>
        </section>
        
        <div class="chat-section">
            <h2>Задай вопрос ChatGPT</h2>
            <div id="chatbox">
                <!-- Chatbox will be updated dynamically -->
            </div>
            <input type="text" id="user-input" placeholder="Введите ваш вопрос...">
        </div>
    </div>

    <div class="footer">
        <p>Этот сайт посвящен космосу, ракетам и исследованию Вселенной.</p>
    </div>

    <script>
        // Placeholder script for future integration with ChatGPT API
        document.getElementById('user-input').addEventListener('keydown', function(e) {
            if (e.key === 'Enter') {
                var input = document.getElementById('user-input').value;
                var chatbox = document.getElementById('chatbox');
                chatbox.innerHTML += '<p><strong>Вы:</strong> ' + input + '</p>';
                // Simulate ChatGPT response
                chatbox.innerHTML += '<p><strong>ChatGPT:</strong> Ответ будет здесь...</p>';
                document.getElementById('user-input').value = ''; // Clear input field
                chatbox.scrollTop = chatbox.scrollHeight; // Auto-scroll to bottom
            }
        });
    </script>
</body>
</html>
"""

# Save the HTML content into a file
file_path = "/mnt/data/personal_space_website.html"
with open(file_path, "w", encoding="utf-8") as file:
    file.write(html_content)

file_path
