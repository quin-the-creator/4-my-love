# 4-my-love
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>You are loved</title>
    <style>
        body {
            background-color: black;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            height: 100vh;
            margin: 0;
            color: white;
        }

        .message-box {
            width: 80%;
            height: 300px;
            background-color: blue;
            border: 10px solid transparent;
            border-image: url('https://example.com/flower-border.png') 30 stretch; /* Replace with an actual floral border image URL */
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            transition: background-color 0.5s;
            text-align: center;
        }

        .heart-button {
            display: inline-block;
            width: 100px;
            height: 100px;
            background-color: #ff4d4d;
            position: relative;
            cursor: pointer;
            border: none;
            border-radius: 50px;
            transform: rotate(-45deg);
            transition: transform 0.3s;
        }

        .heart-button:before,
        .heart-button:after {
            content: '';
            display: block;
            width: 100px;
            height: 100px;
            background-color: #ff4d4d;
            border-radius: 50px;
            position: absolute;
        }

        .heart-button:before {
            top: -50px;
            left: 0;
        }

        .heart-button:after {
            left: 50px;
            top: 0;
        }

        .heart-button:hover {
            transform: scale(1.1) rotate(-45deg);
        }
    </style>
</head>
<body>

    <div class="message-box" id="messageBox">Welcome! Press the heart button for a surprise.</div>

    <button class="heart-button" onclick="changeBox()"> </button>

    <script>
        const messages = [
            "Love is composed of a single soul inhabiting two bodies.",
            "You are my sun, my moon, and all my stars.",
            "In your smile, I see something more beautiful than the stars.",
            "Every love story is beautiful, but ours is my favorite.",
            "You have bewitched me, body and soul.",
            // Add more quotes here, up to 500
        ];

        function changeBox() {
            const box = document.getElementById("messageBox");
            box.style.backgroundColor = "black";
            const randomMessage = messages[Math.floor(Math.random() * messages.length)];
            box.textContent = randomMessage;
            box.style.color = "white";
        }
