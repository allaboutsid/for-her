<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Be My Valentine?</title>

<style>
       body {
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
    
    background-image: url("c:\Users\ASUS\OneDrive\Nostalgia\Desktop\html\blurry red heart wallpaper.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

    .box {
        background: white;
        padding: 40px;
        border-radius: 20px;
        text-align: center;
        box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        width: 350px;
    }

    h1 {
        color: #ff3366;
    }

    button {
        padding: 10px 20px;
        border: none;
        border-radius: 20px;
        font-size: 16px;
        margin: 10px;
        cursor: pointer;
        transition: 0.3s;
    }

    #yesBtn {
        background: #ba2a4e;
        color: white;
    }

    #noBtn {
        background: #ccc;
    }

    .message {
        margin-top: 15px;
        font-size: 14px;
        color: #060506;
    }
</style>
</head>

<body>

<div class="heart">
    <h1>Will you be my Valentine Baby? 🥺</h1>

    <button id="yesBtn" onclick="sayYes()">Yes 💕</button>
    <button id="noBtn" onclick="sayNo()">No :(</button>

    <div class="message" id="message"></div>
</div>

<script>

let noCount = 0;

function sayNo() {
    noCount++;
    const msg = document.getElementById("message");
    const noBtn = document.getElementById("noBtn");

    const responses = [
        "Are you sure? 🥺",
        "I'll give you chocolates...",
        "And hugs...",
        "And kisses...",
        "Aese karegi?",
        "Aese mat kr naaaa",
        "I love you yawrrr.",
        "Another teddy dunga.",
        "Last chance... I promise I'll behave(thoda kam pareshan krunga pakka) 😇.",
    ];

    msg.innerText = responses[Math.min(noCount - 1, responses.length - 1)];

    // move the No button randomly (playful)
    noBtn.style.position = "absolute";
    noBtn.style.left = Math.random() * 80 + "%";
    noBtn.style.top = Math.random() * 80 + "%";
}

function sayYes() {
    document.body.innerHTML = `
        <div style="display:flex;justify-content:center;align-items:center;height:100vh;background:linear-gradient(135deg,#ff758c,#ff7eb3);color:white;font-size:30px;text-align:center;">
            OMG YAYYYY😻😽😻😽
        </div>
    `;
}

</script>

</body>
</html>
