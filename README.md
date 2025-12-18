# Apology-letter-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>QR Surprise 💝</title>

<style>
  body {
    font-family: Poppins, sans-serif;
    background: #ffe6eb;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .box {
    background: white;
    padding: 30px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 15px 40px rgba(0,0,0,.15);
  }

  input {
    width: 100%;
    padding: 10px;
    border-radius: 10px;
    border: 1px solid #ccc;
    margin-bottom: 15px;
  }
</style>
</head>

<body>

<div class="box">
  <h2>💌 QR Surprise</h2>
  <p>Paste the URL of <b>letter.html</b></p>
  <input id="url" placeholder="https://your-site/letter.html">
  <div id="qrcode"></div>
</div>

<script src="https://cdn.jsdelivr.net/npm/qrcodejs@1.0.0/qrcode.min.js"></script>
<script>
  const input = document.getElementById("url");
  input.addEventListener("change", () => {
    document.getElementById("qrcode").innerHTML = "";
    new QRCode("qrcode", {
      text: input.value,
      width: 200,
      height: 200,
      colorDark: "#ff4f8b",
      colorLight: "#ffffff"
    });
  });
</script>

</body>
</html>
