# Indexx.html
/css-images-assignment
│── index.html
│── butterfly.jpg
│── dinosaur.png
│── football_field.jpg
│── tic-tac-toe.png
│── penguins.jpg
│── seagull.png
│── theater_stage.jpg
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CSS3 Image Manipulation</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      padding: 30px;
    }

    h1 {
      text-align: center;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
    }

    figure {
      background: white;
      padding: 15px;
      text-align: center;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }

    figure img {
      max-width: 100%;
    }

    figcaption {
      margin-top: 10px;
      font-weight: bold;
    }

    /* 1. Butterfly – drop shadow + rotation */
    .butterfly {
      filter: drop-shadow(10px 10px 10px rgba(0,0,0,0.5));
      transform: rotate(-5deg);
    }

    /* 2. Dinosaur – grayscale + blur */
    .dinosaur {
      filter: grayscale(100%) blur(2px);
    }

    /* 3. Penguins – vignette using gradient overlay */
    .penguins {
      position: relative;
    }

    .penguins::after {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle, transparent 50%, rgba(0,0,0,0.6));
      pointer-events: none;
    }

    /* 4. Seagull – sepia + contrast */
    .seagull {
      filter: sepia(80%) contrast(140%);
    }

    /* 5. Theater Stage – spotlight effect */
    .stage {
      position: relative;
    }

    .stage::after {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at center, transparent 30%, rgba(0,0,0,0.85));
    }

    /* 6. Football field – layered images */
    .field {
      width: 100%;
      height: 200px;
      background:
        url("tic-tac-toe.png") center/200px no-repeat,
        url("football_field.jpg") center/cover no-repeat;
      border: 6px solid white;
      box-shadow: inset 0 0 20px rgba(0,0,0,0.7);
    }
  </style>
</head>

<body>
  <h1>CSS3 Image Effects Assignment</h1>

  <section class="gallery">

    <figure>
      <img src="butterfly.jpg" class="butterfly" alt="Butterfly">
      <figcaption>Drop Shadow & Rotation</figcaption>
    </figure>

    <figure>
      <img src="dinosaur.png" class="dinosaur" alt="Dinosaur">
      <figcaption>Grayscale & Blur</figcaption>
    </figure>

    <figure class="penguins">
      <img src="penguins.jpg" alt="Penguins">
      <figcaption>Vignette Gradient</figcaption>
    </figure>

    <figure>
      <img src="seagull.png" class="seagull" alt="Seagull">
      <figcaption>Sepia & Contrast</figcaption>
    </figure>

    <figure class="stage">
      <img src="theater_stage.jpg" alt="Theater Stage">
      <figcaption>Spotlight Effect</figcaption>
    </figure>

    <figure>
      <div class="field"></div>
      <figcaption>Multiple Background Images</figcaption>
    </figure>

  </section>
</body>
</html>
