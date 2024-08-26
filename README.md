<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Open URL in 10 Tabs</title>
</head>
<body>
    <h1>Open URL in 10 Tabs</h1>
    <form id="urlForm">
        <input type="text" id="urlInput" placeholder="Enter URL" required>
        <button type="submit">Open</button>
    </form>

    <script>
        document.getElementById('urlForm').addEventListener('submit', function(event) {
            event.preventDefault(); // フォームのデフォルトの送信を防ぐ
            const url = document.getElementById('urlInput').value;
            for (let i = 0; i < 10; i++) {
                window.open(url, '_blank');
            }
        });
    </script>
</body>
</html>
