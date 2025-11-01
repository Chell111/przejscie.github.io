<html lang="">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Full-page Background Photo Examples</title>
  <style>
    /* Reset and ensure page fills viewport */
    html, body { height: 100%; margin: 0; }

    /* Option A: CSS background on the <body> */
  .bg-css {
      min-height: 100%;
      /* Replace with your image path or full URL */
      background-image: url("images/Strona główna.png");
      background-size: cover;          /* cover the whole area */
      background-position: center;     /* center the image */
      background-repeat: no-repeat;
      background-attachment: fixed;    /* optional: fixed during scroll */
      /* fallback background color while image loads */
      background-color: #222;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 2rem;
    }

    /* Option B: full-screen <https://github.com/Chell111/przejscie.github.io/blob/main/images/IMG_5440.JPG?raw=true> with object-fit */
  .bg-img-wrap {
      position: relative;
      min-height: 100vh;
      overflow: hidden;
      color: white;
    }
    .bg-images/Strona główna.png.bg-images/Strona główna.png {
      position: absolute;
      inset: 0;               /* top:0; right:0; bottom:0; left:0 */
      width: 100%;
      height: 100%;
      object-fit: cover;      /* preserve aspect ratio and cover area */
      object-position: center;
      z-index: -1;            /* sit behind content */
    }

    /* Optional dark overlay for readability */
  .overlay {
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.35);
      z-index: 0;
    }

    /* Content styling for both examples */
  .content {
      position: relative;
      z-index: 1;
      max-width: 900px;
      margin: 2rem;
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

  h1 { margin: 0 0 0.5rem 0; font-size: clamp(1.5rem, 3vw, 2.4rem); }
    p  { margin: 0; font-size: clamp(1rem, 2vw, 1.1rem); }

    /* Small-screen adjustments */
  @media (max-width: 520px) {
      .content { margin: 1rem; }
    }
  </style>
</head>
<body>

  <!-- Example A: apply background via CSS on the body -->
  <main class="bg-css" aria-label="images/Strona główna.png">
    <div class="content" role="article">
            </div>
  </main>

  <!-- Example B: Use a full-screen <img> with object-fit (uncomment to test) -->
  
<section class="bg-images/Strona główna.png-wrap" aria-label="Background image using &lt;img&gt;">
    <img class="bg-img" src="images/Strona główna.png" alt="" aria-hidden="true" />
    <div class="overlay" aria-hidden="true"></div>
    <div class="content">
          </div>
  </section>
  -->

</body>
</html>
