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
            "Meeting you felt like finding a place I'd never been, and somehow still knowing every street by heart.",
            "There is nothing I enjoy more than watching you talk about the things that you love. That look you get in your eyes. The way you sparkle. It's infectious.",
            "I went to sleep thinking I couldn't possibly love you more. Then I woke up and I did.",
            "Waking up next to you is like winning the lottery every single day. I don't know how I got so lucky, but I'm so grateful I did.",
            "I knew I was falling in love with you when I realized I was thinking about you without even trying.",
            "Sitting next to you doing absolutely nothing means absolutely everything to me.",
            "I've second guessed a lot of things. Loving you was never one of them.",
            "Someone told me to list all the things I was grateful for, and I just wanted you to know that you were the first thing that came to my mind.",
            "I used to get homesick for places. Now I just get homesick for you.",
            "I never used to understand how people could stare at paintings for hours and hours on end. Then I saw your face.",
            "When I'm alone, the only place I want to be is with you. When I'm with you, the only place I want to be is closer.",
            "Did you know sunflowers follow the sun as it moves across the sky? I think that's why I want to be around you all the time- You're my sunshine.",
            "This careless guy cares a lot about you.",
            "I wish you were here, or I was there, or we were together anywere.",
            "Been thinking of eating a snack, but the snack I'm craving is reading this right now.",
            "There isn't a single part of me, That doesn't crave every part of you.",
            "Me? Obsessed with you? Of course. You are mine<3.",
            "You complete me in ways I never knew i needed.",
            "You're so cute, I mean not just your lookds, but your personality too. The things you say are cute, your voice is cute, your laugh is cute, your smile is cute, Your so perfect.",
            
            // Add more quotes here, up to 500
        ];

        function changeBox() {
            const box = document.getElementById("messageBox");
            box.style.backgroundColor = "black";
            const randomMessage = messages[Math.floor(Math.random() * messages.length)];
            box.textContent = randomMessage;
            box.style.color = "white";
        }
