<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Full-page Background Photo Examples</title>
  <style>
    /* Reset and ensure page fills viewport */
    html, body { height: 100%; margin: 0; }

    

    /* Option B: full-screen <img> with object-fit */
  .bg-img-wrap {
      position: relative;
      min-height: 100vh;
      overflow: hidden;
      color: white;
    }
    .bg-img.bg-img {
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

  <!-- Example B: Use a full-screen <img> with object-fit (uncomment to test) -->
  
  <section class="img" aria-label="Background image using &lt;img&gt;">
    <img class="bg-img" src="images/Strona główna.png" alt="" aria-hidden="true" />
    <div class="overlay" aria-hidden="true"></div>
    <div class="content">
      
    </div>
  </section>
  -->

</body>
</html>
