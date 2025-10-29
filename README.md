# Araba-oyunu1
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Araba Oyunu 🚗</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background-color: #87CEEB;
    }
    #oyun {
      width: 100vw;
      height: 100vh;
      background: linear-gradient(#4CAF50, #228B22);
      position: relative;
      overflow: hidden;
    }
    .araba {
      width: 100px;
      height: 50px;
      background: red;
      border-radius: 10px;
      position: absolute;
      bottom: 20px;
      left: 50px;
    }
    .ağaç, .ev {
      position: absolute;
      bottom: 0;
    }
    .ağaç {
      width: 40px;
      height: 80px;
      background: brown;
    }
    .ağaç::after {
      content: '';
      width: 80px;
      height: 60px;
      background: green;
      position: absolute;
      top: -40px;
      left: -20px;
      border-radius: 50%;
    }
    .ev {
      width: 120px;
      height: 100px;
      background: #FFD700;
      border: 2px solid #000;
    }
  </style>
</head>
<body>
  <div id="oyun">
    <div class="araba" id="araba"></div>
    <div class="ağaç" style="left:300px;"></div>
    <div class="ev" style="left:600px;"></div>
  </div>

  <script>
    const araba = document.getElementById("araba");
    let pozisyon = 50;

    document.addEventListener("keydown", (e) => {
      if (e.key === "ArrowRight") pozisyon += 10;
      if (e.key === "ArrowLeft") pozisyon -= 10;
      araba.style.left = pozisyon + "px";
    });
  </script>
</body>
</html>
