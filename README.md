<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Random Funny Image Viewer</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      padding: 50px;
      background-color: #f9f9f9;
    }
    img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>
  <img id="randomImage" src="" alt="Random funny image" />
  <script>
    function getRandomImage() {
      // Picsum provides random images via a unique URL with a random query param
      const width = 600;
      const height = 400;
      const randomSeed = Math.floor(Math.random() * 10000);
      const randomImageUrl = `https://picsum.photos/seed/${randomSeed}/${width}/${height}`;
      document.getElementById('randomImage').src = randomImageUrl;
    }

    getRandomImage();
  </script>
</body>
</html>
