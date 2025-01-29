<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator Pangkat</title>
    <style>
        body {
            font-family: "Gill Sans MT", "Gill Sans", sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(to right, #00008B, #90EE90);
        }
        .calculator {
            background: linear-gradient(45deg, #00172d, #00264d);
            padding: 30px;
            border-radius: 50px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        input, button {
            border-radius: 50px;
            margin: 10px;
            padding: 10px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h2 style="color: white;">Kalkulator Pangkat Meon</h2>
        <input type="number" id="base" placeholder="Masukkan angka dasar">
        <input type="number" id="exponent" placeholder="Masukkan pangkat">
        <button onclick="hitungPangkat()">Hitung</button>
        <h3 style="color: white;">Hasil: <span id="result">-</span></h3>
    </div>

    <script>
        function hitungPangkat() {
            let base = parseFloat(document.getElementById('base').value);
            let exponent = parseFloat(document.getElementById('exponent').value);
            if (!isNaN(base) && !isNaN(exponent)) {
                document.getElementById('result').innerText = Math.pow(base, exponent);
            } else {
                document.getElementById('result').innerText = 'Input tidak valid';
            }
        }
    </script>
</body>
</html>
