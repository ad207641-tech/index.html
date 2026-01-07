# index.htmll
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CSS3 Image Effects Assignment</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
      padding: 30px;
    }

    h1 {
      text-align: center;
      margin-bottom: 40px;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }

    figure {
      background: #fff;
      padding: 15px;
      text-align: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    figure img {
      width: 100%;
      height: auto;
    }

    figcaption {
      margin-top: 10px;
      font-weight: bold;
    }

    /* 1. Butterfly */
    .butterfly {
      filter: drop-shadow(10px 10px 10px rgba(0,0,0,0.5));
      transform: rotate(-5deg);
    }

    /* 2. Dinosaur */
    .dinosaur {
      filter: grayscale(100%) blur(2px);
    }

    /* 3. Penguins – vignette */
    .penguins {
      position: relative;
    }

    .penguins::after {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle, transparent 45%, rgba(0,0,0,0.6));
      pointer-events: none;
    }

    /* 4. Seagull */
    .seagull {
      filter: sepia(80%) contrast(140%);
    }

    /* 5. Theater stage spotlight */
    .stage {
      position: relative;
    }

    .stage::after {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle, transparent 30%, rgba(0,0,0,0.85));
    }

    /* 6. Football field – multiple backgrounds */
    .field {
      width: 100%;
      height: 220px;
      background:
        url("tic-tac-toe.png") center/180px no-repeat,
        url("football_field.jpg") center/cover no-repeat;
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
