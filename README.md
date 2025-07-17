<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Random Meme</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #000;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    img {
      max-width: 100%;
      max-height: 100vh;
      object-fit: contain;
    }
  </style>
</head>
<body>
  <img id="randomImage" src="" alt="Random meme" />
  <script>
    async function loadMeme() {
      try {
        const response = await fetch('https://meme-api.com/gimme');
        const data = await response.json();
        document.getElementById('randomImage').src = data.url;
      } catch (error) {
        console.error("Failed to load meme:", error);
      }
    }

    loadMeme();
  </script>
</body>
</html>
