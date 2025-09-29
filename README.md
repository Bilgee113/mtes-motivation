<!DOCTYPE html>
<html lang="mn">
<head>
  <meta charset="UTF-8">
  <title>МТЭС Random Text</title>
  <style>
    body {
      font-family: "Poppins", sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(135deg, #000000, #ff5100);
      margin: 0;
    }
    .container {
      text-align: center;
      padding: 20px 40px;
      background: black;
      border-radius: 20px;
      box-shadow: 0 6px 20px rgba(0,0,0,0.15);
    }
    .container img {
      max-width: 160px; /* Дээд хэмжээ */
      width: 100%;       /* Контейнерт уян хатан тохирно */
      height: auto;      /* Зурагны харьцааг хадгална */
      margin-bottom: 8px;
    }
    h1 {
      font-size: 26px;
      font-weight: 600;
      color: #ff4800;
      margin: 10px 0;
      text-shadow: 1px 1px 4px rgba(255, 255, 255, 0.27);
    }
    button {
      margin-top: 12px;
      padding: 8px 16px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      background-color: #ff5100;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #ff784e;
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="mtes logo.png" alt="МТЭС Лого">
    <h1 id="randomText"></h1>
    <button onclick="generateText()">Дахин унших</button>
  </div>

  <script>
    const texts = [
      "Чи өнөөдөр гайхалтай харагдаж байна!",
      "Чамд бүх зүйл амжилттай болно!",
      "Өнөөдөр шинэ боломж чамд ирнэ!",
      "Чиний инээмсэглэл бүхнийг гэрэлтүүлнэ!",
      "Чи хийж чадахгүй зүйл гэж үгүй!"
    ];
    function generateText() {
      const randomIndex = Math.floor(Math.random() * texts.length);
      document.getElementById("randomText").innerText = texts[randomIndex];
    }
    // Эхлэх үед шууд нэг мессеж харуулах
    generateText();
  </script>
</body>
</html>
