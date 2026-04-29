# Falaadata
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>QuickData GH</title>

<style>
body {
  font-family: Arial;
  margin: 0;
  background: #f5f5f5;
}

.header {
  background: #0a3d62;
  color: white;
  padding: 15px;
  text-align: center;
}

.container {
  padding: 15px;
}

.card {
  background: white;
  padding: 15px;
  border-radius: 10px;
  margin-bottom: 15px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

input, select, button {
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
}

button {
  background: #0a3d62;
  color: white;
  border: none;
}

button:hover {
  background: #074a8b;
}
</style>
</head>

<body>

<div class="header">
  <h2>QuickData GH</h2>
</div>

<div class="container">

  <div class="card">
    <h3>Buy Data</h3>

    <select id="network">
      <option value="MTN">MTN</option>
      <option value="AirtelTigo">AirtelTigo</option>
      <option value="Telecel">Telecel</option>
    </select>

    <input type="text" id="phone" placeholder="Enter Phone Number">

    <select id="bundle">
      <option value="1GB">1GB - GHS 5</option>
      <option value="2GB">2GB - GHS 9</option>
      <option value="5GB">5GB - GHS 20</option>
    </select>

    <button onclick="buyData()">Buy Now</button>
  </div>

</div>

<script>
function buyData() {
  let network = document.getElementById("network").value;
  let phone = document.getElementById("phone").value;
  let bundle = document.getElementById("bundle").value;

  if (!phone) {
    alert("Enter phone number");
    return;
  }

  alert(`Processing ${bundle} for ${phone} on ${network}`);

  // Here you will connect to backend API
}
</script>

</body>
</html>
