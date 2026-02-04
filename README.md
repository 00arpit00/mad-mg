<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Are you Mad?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        .container {
            text-align: center;
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
        }
        h1 {
            color: #333;
            margin-bottom: 30px;
        }
        .buttons {
            position: relative;
            height: 60px;
        }
        button {
            padding: 15px 40px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 0 10px;
            transition: transform 0.2s;
        }
        #yes {
            background: #4CAF50;
            color: white;
        }
        #no {
            background: #f44336;
            color: white;
            position: absolute;
            transition: all 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        button:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Are you Mad?</h1>
        <div class="buttons">
            <button id="yes">Yes</button>
            <button id="no">No</button>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('no');
        const yesBtn = document.getElementById('yes');

        noBtn.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - 150);
            const y = Math.random() * (window.innerHeight - 60);
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
            noBtn.style.position = 'fixed';
        });

        yesBtn.addEventListener('click', () => {
            alert('Honesty is the best policy! 😊');
        });
    </script>
</body>
</html>
