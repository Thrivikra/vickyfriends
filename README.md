<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Friendship Certificate Generator</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display&family=Zeyada&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Playfair Display', serif;
      background: linear-gradient(135deg, #cce0ff, #e6ffe6);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      background-color: rgba(255, 255, 255, 0.6);
    }

    .friendship-page {
      text-align: center;
      padding: 50px;
    }

    .friendship-page h1 {
      font-size: 48px;
      color: #6a1b9a;
    }

    .friendship-page p {
      font-size: 20px;
      max-width: 800px;
      margin: 0 auto;
      color: #333;
    }

    .name-form {
      margin-top: 40px;
    }

    input[type="text"] {
      font-size: 20px;
      padding: 10px;
      width: 300px;
      border-radius: 10px;
      border: 2px solid #6a1b9a;
    }

    button {
      font-size: 18px;
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      background: #6a1b9a;
      color: white;
      margin-left: 10px;
      cursor: pointer;
    }

    .certificate {
      display: none;
      background: white;
      margin: 50px auto;
      padding: 40px;
      width: 800px;
      border: 10px solid transparent;
      border-image: linear-gradient(45deg, #8e24aa, #2196f3) 1;
      border-radius: 30px;
      font-family: 'Playfair Display', serif;
      text-align: center;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      position: relative;
    }

    .certificate::after {
      content: "";
      position: absolute;
      top: 15px;
      left: 15px;
      right: 15px;
      bottom: 15px;
      border: 3px solid gold;
      border-radius: 20px;
      pointer-events: none;
    }

    .certificate h2 {
      font-size: 40px;
      margin: 10px 0;
    }

    .certificate h3 {
      font-size: 30px;
      margin: 20px 0;
      font-family: 'Great Vibes', cursive;
    }

    .signature {
      margin-top: 50px;
      font-family: 'Zeyada', cursive;
      font-size: 28px;
      text-align: right;
      padding-right: 30px;
      color: #000;
    }
  

    

    
      100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
    }

    </style>
</head>
<body>
  <div class="friendship-page" style="position: relative; overflow: hidden; height: 100vh;">
    
    </script>
    <h1>Celebrate Friendship!</h1>
    <p>
      True friendship is a priceless gift that lasts a lifetime. Celebrate the bond with your best friend and
      share the joy through a personalized certificate. A simple way to say "Thank you for being my friend."
    </p>
    <div class="name-form">
      <input type="text" id="friendName" placeholder="Enter your name">
      <button onclick="generateCertificate()">Generate Certificate</button>
    </div>
  </div>

  <div class="certificate" id="certificate">
    <h2>KANNAYA GROUP OF COMPANIES</h2>
    <h2>Certificate of Friendship</h2>
    <h3 id="friendOutput">[Friend's Name]</h3>
    <p>This certificate is awarded in honor of the wonderful friendship shared, a symbol of lasting trust, support, and fun times together.</p>
    <div class="signature" style="font-size: 28px; font-family: 'Zeyada', cursive; color: #000; text-align: right; padding-right: 30px; position: relative; width: fit-content; margin-left: auto;">
      <div style="border-bottom: 2px solid gold; display: inline-block; padding-bottom: 5px;">THRIVIKRAM</div>
    </div>
    <div style="font-family: 'Zeyada', cursive; font-size: 20px; text-align: right; padding-right: 30px;"> CEO OF COMPANEY</div>
  </div>

  <script>
    function generateCertificate() {
      const name = document.getElementById('friendName').value.trim();
      if (name) {
        document.getElementById('friendOutput').innerText = name;
        document.getElementById('certificate').style.display = 'block';
        document.querySelector('.friendship-page').scrollIntoView({ behavior: 'smooth' });
        setTimeout(() => {
          document.getElementById('certificate').scrollIntoView({ behavior: 'smooth' });
        }, 500);
      } else {
        alert("Please enter your name.");
      }
    }
  </script>
</body>
</html>
