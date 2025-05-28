# 🎨 **QR Code Generator** 🎨

## 🚀 **Descrição do Projeto**
Este é um **gerador de QR Code** simples e elegante, construído com **HTML, CSS e JavaScript** usando a biblioteca **QRious**. Insira qualquer URL ou texto e gere um QR Code instantaneamente!


## 🛠 **Funcionalidades**
- 🔹 Campo de entrada para URL ou texto
- 🔹 Botão para gerar o QR Code
- 🔹 QR Code exibido diretamente abaixo do botão com espaçamento adequado
- 🔹 Estilo moderno com tema escuro

## 📋 **Instruções de Uso**
1. **Clone o repositório:**
    ```sh
    git clone https://github.com/bruno-a-dias/qr-code-generator.git
    ```
2. **Navegue até o diretório do projeto:**
    ```sh
    cd qr-code-generator
    ```
3. **Abra o arquivo `index.html` em seu navegador:**

## ✨ **Código**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QR Code Generator</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            background-color: #2c2c2c;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            text-align: center;
            background-color: #3b3b3b;
            padding: 30px;
            border-radius: 10px;
        }
        .form-control {
            background-color: #5a5a5a;
            color: #fff;
            border: none;
        }
        .btn {
            background-color: #007bff;
            border: none;
        }
        #qrcode {
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>QR Code Generator</h1>
        <div class="form-group">
            <label for="address">Digite o endereço aqui:</label>
            <input type="text" class="form-control" id="address" placeholder="Enter URL or text">
        </div>
        <button class="btn btn-primary" onclick="generateQRCode()">Gerar QR Code</button>
        <br><br>
        <h4>Salve a imagem gerada logo abaixo.</h4>
        <br><br>
        <canvas id="qrcode"></canvas>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/qrious@4.0.2/dist/qrious.min.js"></script>
    <script>
        function generateQRCode() {
            var qr = new QRious({
                element: document.getElementById('qrcode'),
                size: 200,
                value: document.getElementById('address').value
            });
        }
    </script>
</body>
</html>
