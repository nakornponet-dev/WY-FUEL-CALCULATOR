# WY-FUEL-CALCULATOR
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>WY Fuel Calculator</title>

<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#111827">

<link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">

<h1>✈️ WY Fuel Calculator</h1>

<div class="card">
<h2>Fuel Data</h2>

<label>Arrival Fuel</label>
<input type="number" id="arrival">

<label>Before Fueling</label>
<input type="number" id="before">

<label>Total Final Fuel</label>
<input type="number" id="finalFuel">

<label>Density (SG)</label>
<input type="number" step="0.001" id="density">

<label>Litres</label>
<input type="number" id="litres">
</div>

<div class="card">
<h2>Tank Quantity</h2>

<label>Left Tank</label>
<input type="number" id="leftTank">

<label>Centre Tank</label>
<input type="number" id="centreTank">

<label>Right Tank</label>
<input type="number" id="rightTank">
</div>

<div class="buttons">
<button onclick="calculate()">Calculate</button>
<button onclick="clearAll()">Clear</button>
</div>

<div class="card result">

<h2>Results</h2>

<div class="row">
<span>Fuel Used</span>
<span id="fuelUsed">0</span>
</div>

<div class="row">
<span>Conversion</span>
<span id="conversion">0</span>
</div>

<div class="row">
<span>Uplift</span>
<span id="uplift">0</span>
</div>

<div class="row">
<span>Total ECAM</span>
<span id="totalEcam">0</span>
</div>

<div class="row">
<span>Onboard (I-B)</span>
<span id="onboard">0</span>
</div>

<div class="row">
<span>Discrepancy %</span>
<span id="discrepancy">0</span>
</div>

<div class="row">
<span>Calculated LT</span>
<span id="calcLitres">0</span>
</div>

</div>

</div>

<script src="app.js"></script>

<script>
if ('serviceWorker' in navigator) {
 navigator.serviceWorker.register('sw.js');
}
</script>

</body>
</html>
*{
box-sizing:border-box;
font-family:-apple-system,BlinkMacSystemFont,sans-serif;
}

body{
margin:0;
background:#111827;
color:white;
padding:15px;
}

.container{
max-width:600px;
margin:auto;
}

h1{
text-align:center;
}

.card{
background:#1f2937;
padding:15px;
border-radius:12px;
margin-bottom:15px;
}

label{
display:block;
margin-top:10px;
font-size:14px;
}

input{
width:100%;
padding:12px;
margin-top:4px;
border:none;
border-radius:8px;
background:#374151;
color:white;
}

.buttons{
display:flex;
gap:10px;
margin-bottom:15px;
}

button{
flex:1;
padding:14px;
border:none;
border-radius:10px;
font-weight:bold;
font-size:16px;
}

button:first-child{
background:#10b981;
color:white;
}

button:last-child{
background:#ef4444;
color:white;
}

.row{
display:flex;
justify-content:space-between;
padding:8px 0;
border-bottom:1px solid #374151;
}