<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Tools</title>
<style>
    body {
        background-color: #0d1117; /* Dark GitHub-like background */
        color: white;
        font-family: Arial, sans-serif;
        text-align: center;
        margin: 0;
        padding: 0;
    }
    h1 {
        margin-top: 30px;
        font-size: 28px;
        color: #58a6ff;
    }
    .tools {
        display: flex;
        justify-content: center;
        gap: 40px; /* Space between icons */
        margin-top: 40px;
        flex-wrap: wrap; /* Wrap if screen is small */
    }
    .tool {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .tool img {
        width: 80px;
        height: 80px;
        object-fit: contain;
        margin-bottom: 8px;
        background-color: white;
        padding: 10px;
        border-radius: 15px;
        box-shadow: 0px 4px 10px rgba(0,0,0,0.4);
        transition: transform 0.2s ease-in-out;
    }
    .tool img:hover {
        transform: scale(1.15);
    }
    .tool-name {
        font-size: 14px;
        color: #c9d1d9;
        margin-top: 5px;
    }
</style>
</head>
<body>

<h1>🚀 My Tools</h1>
<div class="tools">
    <div class="tool">
        <img src="html-logo.png" alt="HTML">
        <div class="tool-name">HTML</div>
    </div>
    <div class="tool">
        <img src="css-logo.png" alt="CSS">
        <div class="tool-name">CSS</div>
    </div>
    <div class="tool">
        <img src="js-logo.png" alt="JavaScript">
        <div class="tool-name">JavaScript</div>
    </div>
    <div class="tool">
        <img src="c-logo.png" alt="C Language">
        <div class="tool-name">C Language</div>
    </div>
    <div class="tool">
        <img src="arduino-mega-logo.png" alt="Arduino Mega">
        <div class="tool-name">Arduino Mega</div>
    </div>
    <div class="tool">
        <img src="esp32-cam-logo.png" alt="ESP32-CAM">
        <div class="tool-name">ESP32-CAM</div>
    </div>
    <div class="tool">
        <img src="python-logo.png" alt="Python">
        <div class="tool-name">Python</div>
    </div>
</div>

</body>
</html>
