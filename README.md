<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>PDF Viewer</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        .lang-switch {
            padding: 10px;
            text-align: center;
            background: #f5f5f5;
        }

        .lang-switch button {
            padding: 8px 16px;
            margin: 0 5px;
            cursor: pointer;
            border: 1px solid #ccc;
            background: #fff;
        }

        iframe {
            width: 100%;
            height: calc(100vh - 60px);
            border: none;
        }
    </style>
</head>
<body>

<div class="lang-switch">
    <button onclick="setLang('ru')">Русский</button>
    <button onclick="setLang('en')">English</button>
</div>

<iframe id="pdfViewer" src="pdf/file_ru.pdf"></iframe>

<script>
    function setLang(lang) {
        const viewer = document.getElementById('pdfViewer');

        if (lang === 'ru') {
            viewer.src = 'pdf/file_ru.pdf';
            document.documentElement.lang = 'ru';
        } else {
            viewer.src = 'pdf/file_en.pdf';
            document.documentElement.lang = 'en';
        }
    }
</script>

</body>
</html>
