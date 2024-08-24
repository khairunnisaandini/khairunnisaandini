<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wijaya Teknik </title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(120deg, #89f7fe, #66a6ff);
            font-family: Arial, sans-serif;
        }
        .ad-container {
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            width: 320px;
            text-align: center;
        }
        .ad-header {
            background-color: #007BFF;
            color: white;
            padding: 15px;
            font-size: 24px;
        }
        .ad-body {
            padding: 20px;
        }
        .ad-text {
            font-size: 16px;
            color: #333;
            margin-bottom: 20px;
        }
        .ad-button, .chat-button {
            background-color: #007BFF;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            display: inline-block;
            margin-bottom: 20px;
        }
        .upload-section {
            margin-top: 20px;
        }
        input[type="file"] {
            display: none;
        }
        .custom-file-upload {
            border: 1px solid #ccc;
            display: inline-block;
            padding: 6px 12px;
            cursor: pointer;
            border-radius: 5px;
            background-color: #2bce7a;
            color: white;
        }
        .preview {
            margin-top: 10px;
        }
        .preview img {
            width: 100%;
            border-radius: 10px;
            margin-top: 10px;
        }
        .emojis {
            font-size: 24px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="ad-container">
        <div class="ad-header">Perbaikan Kulkas, Mesin Cuci & AC Specialis</div>
        <div class="ad-body">
            <div class="emojis">🔧🌟🚿</div>
            <div class="ad-text">Profesional, cepat, dan terpercaya. Hubungi kami sekarang untuk layanan terbaik kamu!</div>
            <a href="tel:+6281234567890" class="ad-button">Hubungi Sekarang</a>
            <a href="https://wa.me/6282181930901" class="chat-button">Chat via WhatsApp</a>
            <div class="upload-section">
                <label for="upload-photos" class="custom-file-upload">📸 Unggah Foto Hasil Servis</label>
                <input type="file" id="upload-photos" name="upload-photos" accept="image/*" multiple onchange="previewImages(event)">
                <div class="preview" id="preview"></div>
            </div>
        </div>
    </div>
    <script>
        function previewImages(event) {
            const files = event.target.files;
            const preview = document.getElementById('preview');
            preview.innerHTML = '';
            for (let i = 0; i < files.length; i++) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = document.createElement('img');
                    img.src = e.target.result;
                    preview.appendChild(img);
                };
                reader.readAsDataURL(files[i]);
            }
        }
    </script>
</body>
</html>



