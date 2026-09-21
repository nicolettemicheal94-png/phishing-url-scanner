<!DOCTYPE html>
<html>
<head>
<title>AI Phishing URL Scanner</title>
<style>
body{font-family:Arial;text-align:center;padding:40px;background:#eef2f7}
.box{background:white;padding:30px;border-radius:20px;max-width:500px;margin:auto}
input{width:90%;padding:15px;font-size:16px}
button{padding:15px 30px;margin:15px;background:#2864dc;color:white;border:0;border-radius:10px}
#result{font-size:18px;font-weight:bold}
</style>
</head>
<body>
<div class="box">
<h1>AI Phishing URL Scanner</h1>
<p>Enter a website URL to check for suspicious signs.</p>
<input id="url" placeholder="https://example.com">
<button onclick="scan()">Scan URL</button>
<p id="result"></p>
</div>
<script>
function scan(){
let u=document.getElementById("url").value.toLowerCase();
let r=document.getElementById("result");
if(!u){r.innerText="Please enter a URL.";return;}
if(u.includes("login")||u.includes("verify")||u.includes("free")||u.includes("@"))
r.innerText="⚠️ Suspicious URL";
else
r.innerText="✅ URL looks safe";
}
</script>
</body>
</html>
