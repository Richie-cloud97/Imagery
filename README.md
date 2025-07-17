<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Random Image Viewer</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      padding: 50px;
    }
    img {
      max-width: 100%;
      height: auto;
    }
  </style>
</head>
<body>
  <h1>Here's your random image!</h1>
  <img id="randomImage" src="" alt="Random image" />
  <script>
    async function getRandomImage() {
      // Example using Unsplash's random image API
      const randomImageUrl = `https://source.unsplash.com/random?sig=${Math.floor(Math.random() * 10000)}`;
      document.getElementById('randomImage').src = randomImageUrl;
    }

    getRandomImage();
  </script>
</body>
</html>
