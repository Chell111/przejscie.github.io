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
     
      /* fallback background color while image loads */
  background-color: #222;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 2rem;
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

    
  </style>
</head>
<body>

  <!-- Example A: apply background via CSS on the body -->
  <main class="bg-css" aria-label="images/Strona główna.png">
    <div class="content" role="article">
            </div>
  </main>

</body>
</html>
