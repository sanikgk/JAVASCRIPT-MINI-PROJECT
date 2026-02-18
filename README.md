# JAVASCRIPT-MINI-PROJECT

<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title> Multiplication Table Generator </title>

<style>
    body {
    padding: 30px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-image: url("/background_img.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    }

    .box {
    padding: 40px;
    max-width: 560px;
    margin: auto;
    border-radius: 20px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.08);
    background: linear-gradient(to right, #3a9bfb, hsl(180, 76%, 50%));
    }

    h2 {
    margin-top: 0;
    color: #000205;
    }

    select, button {
    padding: 10px;
    font-size: 20px;
    margin-top: 10px;
    width: 100%;
    border-radius: 8px;
    border: 1px solid hsl(220, 84%, 48%);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }

    button {
    color: rgb(15, 3, 67);
    border: none;
    cursor: pointer;
    margin-top: 12px;
    background: linear-gradient(to right, #6af197, #f2ff04);
    }

    ul {
    padding-left: 0;
    list-style: none;
    margin-top: 16px;
    }

    li {
    background: #f1f5f9;
    margin: 7px 0;
    padding: 10px;
    border-radius: 8px;
    }
</style>

</head>

<body>
<div class="box">
    <h2> Multiplication Table Generator </h2>

    <label for="numSelect">Choose a number</label>
    
    <select id="numSelect"></select>

    <button id="btnGenerate">Generate Table</button>

    <ul id="result"></ul>
</div>

<script>
let select = document.getElementById("numSelect");
let result = document.getElementById("result");
let button = document.getElementById("btnGenerate");

for (let i = 1; i <= 20; i++) {
select.innerHTML += `<option value="${i}">${i}</option>`;
}

function generateMultiplicationTable() {
let number = Number(select.value);
result.innerHTML = "";

for (let i = 0; i <= 10; i++) {
result.innerHTML += `<li>${number} × ${i} = ${number * i}</li>`;
}
}

button.addEventListener("click", generateMultiplicationTable);

generateMultiplicationTable();  
</script>

</body>
</html>


