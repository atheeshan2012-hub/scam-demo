<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>பரிசு மழை - Win 1 Crore!</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            background: white;
            border-radius: 20px;
            padding: 30px;
            max-width: 500px;
            width: 100%;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }
        
        .header {
            text-align: center;
            margin-bottom: 25px;
        }
        
        .header h1 {
            color: #ff6b6b;
            font-size: 24px;
            margin-bottom: 10px;
            animation: pulse 2s infinite;
        }
        
        .header p {
            color: #333;
            font-size: 18px;
            font-weight: bold;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        .warning-banner {
            background: #ff4444;
            color: white;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
            font-weight: bold;
            text-align: center;
            display: none;
        }
        
        .warning-banner.show {
            display: block;
            animation: shake 0.5s;
        }
        
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-10px); }
            75% { transform: translateX(10px); }
        }
        
        .question {
            margin-bottom: 20px;
        }
        
        .question label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #333;
        }
        
        .question select,
        .question input {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
        }
        
        .btn {
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 20px;
            transition: transform 0.2s;
        }
        
        .btn:hover {
            transform: scale(1.05);
        }
        
        .gift-boxes {
            display: none;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-top: 20px;
        }
        
        .gift-boxes.show {
            display: grid;
        }
        
        .gift-box {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .gift-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
        }
        
        .gift-box::before {
            content: '🎁';
            font-size: 40px;
            display: block;
            animation: bounce 1s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .explanation {
            display: none;
            background: #fff3cd;
            border: 3px solid #ffc107;
            border-radius: 15px;
            padding: 20px;
            margin-top: 20px;
        }
        
        .explanation.show {
            display: block;
        }
        
        .explanation h2 {
            color: #856404;
            margin-bottom: 15px;
        }
        
        .explanation ul {
            margin-left: 20px;
            line-height: 1.8;
            color: #856404;
        }
        
        .explanation ul li {
            margin-bottom: 10px;
        }
        
        .timer {
            background: #ff4444;
            color: white;
            padding: 10px;
            border-radius: 8px;
            text-align: center;
            font-weight: bold;
            margin-bottom: 20px;
            display: none;
        }
        
        .timer.show {
            display: block;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎉 பரிசு மழை 🎉</h1>
            <p>நீங்களும் வெல்லலாம் ₹1 கோடி!</p>
        </div>
        
        <div class="warning-banner" id="warningBanner">
            ⚠️ THIS IS A SCAM DEMONSTRATION - DO NOT SHARE PERSONAL INFO! ⚠️
        </div>
        
        <div class="timer" id="timer">
            ⏰ Time Left: <span id="countdown">05:00</span> - Hurry Up!
        </div>
        
        <div id="questionSection">
            <div class="question">
                <label>Gender / பாலினம்:</label>
                <select id="gender">
                    <option value="">Select / தேர்ந்தெடுக்கவும்</option>
                    <option value="male">Male / ஆண்</option>
                    <option value="female">Female / பெண்</option>
                </select>
            </div>
            
            <div class="question">
                <label>Age / வயது:</label>
                <input type="number" id="age" placeholder="Enter your age / உங்கள் வயதை உள்ளிடவும்">
            </div>
            
            <div class="question">
                <label>Phone Number / தொலைபேசி எண்:</label>
                <input type="tel" id="phone" placeholder="Enter phone number / தொலைபேசி எண்ணை உள்ளிடவும்">
            </div>
            
            <button class="btn" onclick="showGifts()">Continue to Win Prize! 🎁</button>
        </div>
        
        <div class="gift-boxes" id="giftBoxes">
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
            <div class="gift-box" onclick="revealScam()"></div>
        </div>
        
        <div class="explanation" id="explanation">
            <h2>🚨 This is How Scams Work! 🚨</h2>
            <ul>
                <li><strong>Fake Urgency:</strong> Countdown timers create pressure to act quickly without thinking</li>
                <li><strong>Personal Data Collection:</strong> They collect your phone, age, gender for spam/fraud</li>
                <li><strong>False Prizes:</strong> No real prizes exist - it's designed to steal your information</li>
                <li><strong>Never Ends:</strong> After clicking boxes, they ask for more info, OTP, or payment</li>
                <li><strong>Spread via Links:</strong> Scammers want you to share the link with friends</li>
                <li><strong>Red Flags:</strong> Too good to be true, asking personal info, urgent timers</li>
            </ul>
            <p style="margin-top: 15px; font-weight: bold; color: #d9534f;">
                ⚠️ Never share personal information on suspicious websites!<br>
                ⚠️ Never click on unknown prize links!<br>
                ⚠️ If it seems too good to be true, it probably is!
            </p>
        </div>
    </div>
    
    <script>
        let countdownInterval;
        
        function showGifts() {
            document.getElementById('warningBanner').classList.add('show');
            document.getElementById('timer').classList.add('show');
            document.getElementById('questionSection').style.display = 'none';
            document.getElementById('giftBoxes').classList.add('show');
            
            let timeLeft = 300;
            countdownInterval = setInterval(() => {
                timeLeft--;
                let minutes = Math.floor(timeLeft / 60);
                let seconds = timeLeft % 60;
                document.getElementById('countdown').textContent = 
                    `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                
                if (timeLeft <= 0) {
                    clearInterval(countdownInterval);
                }
            }, 1000);
        }
        
        function revealScam() {
            clearInterval(countdownInterval);
            document.getElementById('giftBoxes').style.display = 'none';
            document.getElementById('timer').style.display = 'none';
            document.getElementById('explanation').classList.add('show');
        }
    </script>
</body>
</html>
