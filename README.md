<html lang="en">
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
      background-image: url("https://chell111.github.io/przejscie.github.io/images/Strona%20g%C5%82%C3%B3wna.png");
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
  <main class="bg-css" aria-label="Background image using CSS">
    <div class="content" role="article">
      
    </div>
  </main>
  </body>
</html>
