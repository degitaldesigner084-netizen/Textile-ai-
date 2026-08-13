<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Textile AI</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  font-family:Arial,sans-serif;
  background:#f5f7fb;
  color:#172033;
}

header{
  background:#ffffff;
  padding:18px 25px;
  border-bottom:1px solid #ddd;
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.logo{
  font-size:24px;
  font-weight:bold;
}

.hero{
  text-align:center;
  padding:55px 20px 30px;
}

.hero h1{
  font-size:42px;
  margin-bottom:12px;
}

.hero p{
  color:#687386;
  font-size:17px;
}

.upload-box{
  max-width:700px;
  margin:20px auto;
  background:white;
  border:2px dashed #aeb9cc;
  border-radius:20px;
  padding:50px 20px;
  text-align:center;
}

.upload-icon{
  font-size:55px;
  margin-bottom:15px;
}

.upload-box h2{
  margin-bottom:10px;
}

.upload-box p{
  color:#777;
  margin-bottom:20px;
}

button{
  border:none;
  background:#2864d7;
  color:white;
  padding:13px 25px;
  border-radius:10px;
  font-size:16px;
  font-weight:bold;
  cursor:pointer;
}

button:hover{
  background:#174fae;
}

#preview{
  display:none;
  max-width:90%;
  max-height:400px;
  margin:25px auto;
  border-radius:12px;
}

.tools{
  max-width:900px;
  margin:30px auto;
  padding:20px;
}

.tools h2{
  margin-bottom:20px;
}

.cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
  gap:15px;
}

.card{
  background:white;
  padding:22px;
  border-radius:14px;
  border:1px solid #e1e5ec;
  text-align:center;
}

.card span{
  font-size:30px;
  display:block;
  margin-bottom:10px;
}

footer{
  text-align:center;
  padding:30px;
  color:#777;
}
</style>
</head>

<body>

<header>
  <div class="logo">🧵 Textile AI</div>
  <div>AI Textile Design</div>
</header>

<section class="hero">
  <h1>Textile AI</h1>
  <p>Upload your textile design and create clean, sharp, HD artwork.</p>
</section>

<section class="upload-box">

  <div class="upload-icon">☁️</div>

  <h2>Upload Your Design</h2>

  <p>
    JPG, PNG or WEBP
  </p>

  <input
    type="file"
    id="fileInput"
    accept="image/*"
    hidden
  >

  <button onclick="document.getElementById('fileInput').click()">
    Upload Design
  </button>

  <img id="preview">

  <br><br>

  <button id="enhanceBtn" style="display:none;">
    ✨ Enhance Design
  </button>

</section>

<section class="tools">

<h2>Textile AI Tools</h2>

<div class="cards">

<div class="card">
<span>✨</span>
HD Enhancement
</div>

<div class="card">
<span>🧹</span>
Clean Design
</div>

<div class="card">
<span>🔁</span>
Seamless Repeat
</div>

<div class="card">
<span>🎨</span>
Color Separation
</div>

<div class="card">
<span>🌈</span>
Colorways
</div>

<div class="card">
<span>👗</span>
Dress → Print
</div>

</div>

</section>

<footer>
© 2026 Textile AI — Professional Textile Design
</footer>

<script>

const fileInput = document.getElementById("fileInput");
const preview = document.getElementById("preview");
const enhanceBtn = document.getElementById("enhanceBtn");

fileInput.addEventListener("change", function(){

  const file = this.files[0];

  if(file){

    const reader = new FileReader();

    reader.onload = function(e){

      preview.src = e.target.result;
      preview.style.display = "block";
      enhanceBtn.style.display = "inline-block";

    };

    reader.readAsDataURL(file);
  }

});

enhanceBtn.addEventListener("click", function(){

  alert(
    "AI Enhancement system will be connected in the next step."
  );

});

</script>

</body>
</html>
