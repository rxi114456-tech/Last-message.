<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Do You Miss Me?</title>

<style>
* {
    box-sizing: border-box;
}

html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    min-height: 100%;
}

body {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow-x: hidden;

    font-family: Arial, Helvetica, sans-serif;

    background:
        radial-gradient(circle at 20% 20%, #ffd6e5 0%, transparent 30%),
        radial-gradient(circle at 80% 80%, #ffdce9 0%, transparent 30%),
        linear-gradient(135deg, #fff1f6, #ffe3ed);
}

/* floating hearts */

.heart {
    position: fixed;
    bottom: -30px;
    font-size: 20px;
    pointer-events: none;
    animation: floatUp 5s linear forwards;
    z-index: 1;
}

@keyframes floatUp {
    0% {
        transform: translateY(0) rotate(0deg);
        opacity: 0;
    }

    15% {
        opacity: 1;
    }

    100% {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
    }
}

/* main */

.container {
    width: 94%;
    max-width: 500px;
    padding: 20px 0;
    position: relative;
    z-index: 5;
}

.card {
    width: 100%;
    padding: 25px 20px 30px;

    background: rgba(255,255,255,0.78);
    backdrop-filter: blur(18px);
    -webkit-backdrop-filter: blur(18px);

    border: 2px solid rgba(255,255,255,0.9);
    border-radius: 32px;

    box-shadow:
        0 20px 60px rgba(150,70,100,0.18),
        inset 0 1px 0 rgba(255,255,255,0.9);

    text-align: center;
}

/* image */

.photo {
    width: 250px;
    height: 250px;

    margin: 0 auto 25px;

    border-radius: 28px;
    overflow: hidden;

    background: #f5dce6;

    box-shadow:
        0 12px 35px rgba(80,40,60,0.22);

    transition:
        transform 0.5s ease,
        opacity 0.4s ease;
}

.photo.change {
    transform: scale(0.85) rotate(-3deg);
    opacity: 0;
}

.photo img {
    width: 100%;
    height: 100%;

    object-fit: cover;
    display: block;
}

/* title */

h1 {
    margin: 5px 0 8px;

    color: #4a2b38;

    font-size: 30px;
    font-weight: 700;
}

.subtitle {
    margin-bottom: 22px;

    color: #87616f;
    font-size: 15px;
}

/* long message */

.message {
    width: 100%;

    max-height: 280px;
    overflow-y: auto;

    padding: 18px;

    border-radius: 20px;

    background: rgba(255,245,249,0.75);

    color: #634452;

    font-size: 14px;
    line-height: 1.8;

    text-align: left;

    scrollbar-width: thin;
}

.message::-webkit-scrollbar {
    width: 5px;
}

.message::-webkit-scrollbar-thumb {
    background: #e8a9be;
    border-radius: 20px;
}

/* question */

.question {
    margin-top: 24px;
    margin-bottom: 18px;

    color: #4a2b38;

    font-size: 24px;
    font-weight: bold;
}

/* buttons */

.buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;

    min-height: 65px;
}

button {
    border: none;
    outline: none;

    padding: 13px 30px;

    border-radius: 999px;

    font-size: 17px;
    font-weight: bold;

    cursor: pointer;

    transition:
        transform 0.35s ease,
        box-shadow 0.35s ease,
        opacity 0.35s ease;
}

.yes {
    background: linear-gradient(135deg, #ff6f9f, #ff91b5);
    color: white;

    box-shadow: 0 8px 22px rgba(255,105,150,0.35);
}

.no {
    background: #eeeeee;
    color: #555;

    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
}

button:hover {
    transform: translateY(-3px) scale(1.04);
}

button:active {
    transform: scale(0.9);
}

/* final */

.final {
    animation: finalPop 0.8s ease;
}

@keyframes finalPop {
    0% {
        transform: scale(0.7);
        opacity: 0;
    }

    70% {
        transform: scale(1.08);
    }

    100% {
        transform: scale(1);
        opacity: 1;
    }
}

/* mobile */

@media (max-width: 430px) {

    .card {
        padding: 20px 15px 25px;
        border-radius: 28px;
    }

    .photo {
        width: 220px;
        height: 220px;
    }

    h1 {
        font-size: 27px;
    }

    .message {
        font-size: 13px;
        line-height: 1.75;
        max-height: 250px;
    }

    .question {
        font-size: 21px;
    }

    button {
        padding: 12px 25px;
    }
}
</style>
</head>


<body>

<div class="container">

    <div class="card" id="card">

        <!-- IMAGE -->
        <div class="photo" id="photo">
            <img id="catImage" src="cat1.jpg" alt="cat">
        </div>


        <!-- TITLE -->
        <h1>Do You Miss Me?</h1>

        <div class="subtitle">
            🐾 just one little question...
        </div>


        <!-- YOUR MESSAGE -->
        <div class="message">

            ɪ ᴅᴏɴ'ᴛ ʀᴇᴀʟʟʏ ᴋɴᴏᴡ ʜᴏᴡ ᴛᴏ ꜱᴀʏ ᴛʜɪꜱ, ʙᴜᴛ ᴛʜᴇʀᴇ ᴀʀᴇ ꜱᴛɪʟʟ ꜱᴏ ᴍᴀɴʏ ᴛʜɪɴɢꜱ ɪ ᴡᴀɴᴛ ᴛᴏ ᴛᴇʟʟ ʏᴏᴜ. ꜱᴏᴍᴇᴛɪᴍᴇꜱ ɪ ᴡᴏɴᴅᴇʀ ɪꜰ ʏᴏᴜ ᴇᴠᴇʀ ᴍɪꜱꜱ ᴍᴇ ᴛᴏᴏ, ᴇᴠᴇɴ ᴊᴜꜱᴛ ᴀ ʟɪᴛᴛʟᴇ. ɪ ᴋɴᴏᴡ ᴛʜɪɴɢꜱ ʜᴀᴠᴇ ᴄʜᴀɴɢᴇᴅ ʙᴇᴛᴡᴇᴇɴ ᴜꜱ, ᴀɴᴅ ᴍᴀʏʙᴇ ᴡᴇ ᴀʀᴇɴ'ᴛ ᴛʜᴇ ꜱᴀᴍᴇ ᴘᴇᴏᴘʟᴇ ᴡᴇ ᴜꜱᴇᴅ ᴛᴏ ʙᴇ, ʙᴜᴛ ᴀ ᴘᴀʀᴛ ᴏꜰ ᴍᴇ ꜱᴛɪʟʟ ʀᴇᴍᴇᴍʙᴇʀꜱ ᴀʟʟ ᴛʜᴇ ʟɪᴛᴛʟᴇ ᴍᴏᴍᴇɴᴛꜱ ᴡᴇ ʜᴀᴅ ᴛᴏɢᴇᴛʜᴇʀ.

            ɪ ꜱᴛɪʟʟ ʀᴇᴍᴇᴍʙᴇʀ ᴛʜᴇ ᴡᴀʏ ᴡᴇ ᴜꜱᴇᴅ ᴛᴏ ᴛᴀʟᴋ, ʟᴀᴜɢʜ, ᴀɴᴅ ꜱᴘᴇɴᴅ ᴛɪᴍᴇ ᴛᴏɢᴇᴛʜᴇʀ. ᴛʜᴏꜱᴇ ᴍᴏᴍᴇɴᴛꜱ ᴍɪɢʜᴛ ꜱᴇᴇᴍ ꜱᴍᴀʟʟ ɴᴏᴡ, ʙᴜᴛ ᴛʜᴇʏ ᴍᴇᴀɴᴛ ᴀ ʟᴏᴛ ᴛᴏ ᴍᴇ. ᴇᴠᴇɴ ᴡʜᴇɴ ɪ ᴛʀʏ ɴᴏᴛ ᴛᴏ ᴛʜɪɴᴋ ᴀʙᴏᴜᴛ ᴛʜᴇᴍ, ꜱᴏᴍᴇʜᴏᴡ ᴛʜᴇʏ ᴀʟᴡᴀʏꜱ ꜰɪɴᴅ ᴛʜᴇɪʀ ᴡᴀʏ ʙᴀᴄᴋ ɪɴᴛᴏ ᴍʏ ᴍɪɴᴅ.

            ᴍᴀʏʙᴇ ɪ'ᴍ ʙᴇɪɴɢ ᴀ ʟɪᴛᴛʟᴇ ꜱɪʟʟʏ ꜰᴏʀ ᴍᴀᴋɪɴɢ ᴛʜɪꜱ, ʙᴜᴛ ɪ ᴊᴜꜱᴛ ᴡᴀɴᴛᴇᴅ ʏᴏᴜ ᴛᴏ ᴋɴᴏᴡ ᴛʜᴀᴛ ʏᴏᴜ ᴡᴇʀᴇ ꜱᴏᴍᴇᴏɴᴇ ʀᴇᴀʟʟʏ ɪᴍᴘᴏʀᴛᴀɴᴛ ᴛᴏ ᴍᴇ. ɪ ᴅᴏɴ'ᴛ ᴇxᴘᴇᴄᴛ ᴀɴʏᴛʜɪɴɢ ꜰʀᴏᴍ ʏᴏᴜ. ɪ ᴊᴜꜱᴛ ᴡᴀɴᴛᴇᴅ ᴛᴏ ᴀꜱᴋ ᴏɴᴇ ꜱɪᴍᴘʟᴇ ǫᴜᴇꜱᴛɪᴏɴ: ᴅᴏ ʏᴏᴜ ᴍɪꜱꜱ ᴍᴇ ᴛᴏᴏ?

            ᴀɴᴅ ɪꜰ ʏᴏᴜʀ ᴀɴꜱᴡᴇʀ ɪꜱ ʏᴇꜱ... ᴛʜᴇɴ ᴍᴀʏʙᴇ, ꜱᴏᴍᴇᴡʜᴇʀᴇ ɪɴꜱɪᴅᴇ ʏᴏᴜ, ʏᴏᴜ ꜱᴛɪʟʟ ʀᴇᴍᴇᴍʙᴇʀ ᴍᴇ ᴛᴏᴏ. 🤍

            ᴛʜᴀɴᴋ ʏᴏᴜ ꜰᴏʀ ʙᴇɪɴɢ ᴀ ᴘᴀʀᴛ ᴏꜰ ᴍʏ ʟɪꜰᴇ, ᴇᴠᴇɴ ɪꜰ ᴛʜɪɴɢꜱ ᴅɪᴅɴ'ᴛ ꜱᴛᴀʏ ᴛʜᴇ ᴡᴀʏ ɪ ᴏɴᴄᴇ ʜᴏᴘᴇᴅ ᴛʜᴇʏ ᴡᴏᴜʟᴅ. ᴡʜᴀᴛᴇᴠᴇʀ ʜᴀᴘᴘᴇɴꜱ ꜰʀᴏᴍ ʜᴇʀᴇ, ɪ'ʟʟ ᴀʟᴡᴀʏꜱ ʙᴇ ɢʀᴀᴛᴇꜰᴜʟ ꜰᴏʀ ᴛʜᴇ ᴍᴇᴍᴏʀɪᴇꜱ ᴡᴇ ᴍᴀᴅᴇ.

            ɪ ʜᴏᴘᴇ ʏᴏᴜ ᴋɴᴏᴡ ᴛʜᴀᴛ ʏᴏᴜ ᴡᴇʀᴇ ɴᴇᴠᴇʀ ᴍᴇᴀɴɪɴɢʟᴇꜱꜱ ᴛᴏ ᴍᴇ.

        </div>


        <!-- QUESTION -->
        <div class="question" id="question">
            Do you miss me? 🥺
        </div>


        <!-- BUTTONS -->
        <div class="buttons">

            <button class="yes" id="yesButton" onclick="answer('yes')">
                Yes 💗
            </button>

            <button class="no" id="noButton" onclick="answer('no')">
                No
            </button>

        </div>

    </div>

</div>


<script>

/* =========================
   SETTINGS
========================= */

const images = [
    "cat1.jpg",
    "cat2.jpg",
    "cat3.jpg",
    "cat4.jpg",
    "cat5.jpg"
];

let round = 0;


/* =========================
   ELEMENTS
========================= */

const image = document.getElementById("catImage");
const photo = document.getElementById("photo");
const question = document.getElementById("question");

const yesButton = document.getElementById("yesButton");
const noButton = document.getElementById("noButton");


/* =========================
   BUTTON FUNCTION
========================= */

function answer(choice) {

    /* increase round */
    round++;


    /* change image */

    if (round <= images.length) {

        photo.classList.add("change");

        setTimeout(() => {

            image.src = images[round - 1];

            photo.classList.remove("change");

        }, 250);
    }


    /* =========================
       FIRST 4 ROUNDS
    ========================= */

    if (round < 5) {

        if (choice === "yes") {

            question.innerHTML = "Press No 😭";

        } else {

            question.innerHTML = "Press Yes 🥺";

        }

    }


    /* =========================
       FINAL ROUND
    ========================= */

    else {

        question.innerHTML = "YES 💗";

        question.classList.add("final");

        yesButton.innerHTML = "Yes 💗";

        noButton.style.display = "none";

        yesButton.style.transform = "scale(1.25)";

        yesButton.style.boxShadow =
            "0 12px 35px rgba(255,105,150,0.5)";

        yesButton.onclick = function() {

            question.innerHTML = "I knew it... 🤍";

            createHearts();

        };

        createHearts();
    }

}


/* =========================
   FLOATING HEARTS
========================= */

function createHeart() {

    const heart = document.createElement("div");

    heart.className = "heart";

    const hearts = ["💗", "💖", "💕", "🤍", "♡"];

    heart.innerHTML =
        hearts[Math.floor(Math.random() * hearts.length)];

    heart.style.left =
        Math.random() * 100 + "vw";

    heart.style.fontSize =
        (15 + Math.random() * 20) + "px";

    heart.style.animationDuration =
        (3 + Math.random() * 3) + "s";

    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 6000);
}


function createHearts() {

    for (let i = 0; i < 18; i++) {

        setTimeout(() => {
            createHeart();
        }, i * 120);

    }
}


/* =========================
   BACKGROUND HEARTS
========================= */

setInterval(() => {

    if (Math.random() > 0.5) {
        createHeart();
    }

}, 1000);

</script>

</body>
</html>
