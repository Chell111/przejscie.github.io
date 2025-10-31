<html lang="pl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Zdjęcia konkursowe</title>
  <style>
    :root{
      --bg:#e8b97c;
      --card:#c19564;
      --muted:#111;
      --accent:#111;
      --radius:12px;
      --gap:1rem;
      --max-width:1100px;
    }

    /* Page reset and layout */
  *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:system-ui,-apple-system,"Segoe UI",Roboto,Arial; background:var(--bg); color:#111}
    .wrap{max-width:var(--max-width);margin:0 auto;padding:1rem;}

  header{
      text-align:center;
      padding:1.25rem 0 0.5rem;
    }
    header h1{margin:.2rem 0;font-size:clamp(1.25rem,3.5vw,1.9rem)}
    header p{margin:0;color:var(--muted);font-size:0.95rem}

    /* Gallery grid - mobile first */
  .gallery{
      display:grid;
      grid-template-columns:1fr;
      gap:var(--gap);
      margin-top:1rem;
    }

  figure.card{
      margin:0;
      background:var(--card);
      border-radius:var(--radius);
      overflow:hidden;
      box-shadow: 0 6px 18px rgba(12,12,15,0.06);
      transition:transform .18s ease, box-shadow .18s ease;
      display:flex;
      flex-direction:column;
      min-height:140px;
    }
    figure.card:hover{ transform:translateY(-6px); box-shadow:0 14px 30px rgba(12,12,15,0.10) }

  .thumb{
      width:100%;
      display:block;
      aspect-ratio: 16 / 10;
      object-fit:cover;
    }

  figcaption{
      padding:0.85rem 0.9rem 1rem;
      flex:1;
      display:flex;
      flex-direction:column;
      gap:0.5rem;
    }
    figcaption h3{margin:0;font-size:1rem}
    figcaption p{margin:0;color:var(--muted);font-size:0.92rem;line-height:1.3}

  .meta{
      margin-top:auto;
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:0.5rem;
    }
    .meta .btn{
      background:transparent;
      border:1px solid rgba(0,0,0,0.06);
      color:var(--accent);
      padding:0.35rem 0.55rem;
      border-radius:8px;
      font-weight:600;
      font-size:0.9rem;
      cursor:pointer;
    }

    /* Responsive breakpoints */
  @media (min-width:600px){
      .gallery{ grid-template-columns: repeat(2, 1fr); }
    }
    @media (min-width:1000px){
      .gallery{ grid-template-columns: repeat(3, 1fr); }
    }

    /* Modal (image lightbox) */
  .modal{
      position:fixed;
      inset:0;
      display:none;
      align-items:center;
      justify-content:center;
      background:rgba(2,6,23,0.6);
      z-index:9999;
      padding:1rem;
    }
    .modal.open{ display:flex }
    .modal .modal-inner{
      max-width:1200px;
      width:100%;
      border-radius:10px;
      overflow:hidden;
      background:#111;
      box-shadow:0 20px 60px rgba(2,6,23,0.6);
    }
    .modal img{
      width:100%;
      height:auto;
      display:block;
      max-height:80vh;
      object-fit:contain;
      background:#000;
    }
    .modal .caption{
      padding:0.8rem 1rem;
      color:#eee;
      font-size:0.95rem;
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:0.6rem;
    }
    .modal .close{
      background:transparent;
      border:0;
      color:#ddd;
      font-size:1.05rem;
      cursor:pointer;
    }

    /* Small accessibility helpers */
  a{color:var(--accent)}
    @media (prefers-reduced-motion: reduce){
      *{transition:none!important}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <h1>NA KOGO ZAGŁOSUJESZ?</h1>
      <p>Wybierz mądrze</p>
    </header>

    <!--
      Replace the images below with your own files.
      Put your images in an "images/" folder next to this HTML file (or adjust the paths).
      For each <figure>:
        - Update src and data-full attributes to point to the image file (full-size in data-full optional).
        - Update alt text and captions.
      The img elements use loading="lazy" for better performance on mobile.
    -->
  <main class="gallery" aria-live="polite">
      <figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/image.jpg?raw=true"
             srcset="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/image.jpg?raw=true 600w, https://github.com/Chell111/przejsciestron.github.io/blob/main/images/image.jpg?raw=true 1000w, https://github.com/Chell111/przejsciestron.github.io/blob/main/images/image.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 1"
             loading="lazy"
             data-full="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/image.jpg?raw=true">
        <figcaption>
          <h3>Winston</h3>
          <p>11/12 lat. Wielki tchórz, hater plebsu</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

  <figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Iwan%20w%20pude%C5%82ku.png?raw=true"
             srcset="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Iwan%20w%20pude%C5%82ku.png?raw=true 600w, https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Iwan%20w%20pude%C5%82ku.png?raw=true 1000w, https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Iwan%20w%20pude%C5%82ku.png?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 2"
             loading="lazy"
             data-full="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Iwan%20w%20pude%C5%82ku.png?raw=true">
        <figcaption>
          <h3>Ivan 6</h3>
          <p>6 lat. Sprzedał by matkę za 3 krewetki</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

  <figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Maciej.jpg?raw=true"
             srcset="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Maciej.jpg?raw=true 600w, https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Maciej.jpg?raw=true 1000w, https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Maciej.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejsciestron.github.io/blob/main/images/Maciej.jpg?raw=true">
        <figcaption>
          <h3>Maciej Abraham Abdul III</h3>
          <p>3 lata. Nie przyznaje się do syna</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

<figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejscie.github.io/blob/main/images/Burbon.jpg?raw=true"
             srcset="https://github.com/Chell111/przejscie.github.io/blob/main/images/Burbon.jpg?raw=true 600w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Burbon.jpg?raw=true 1000w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Burbon.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejscie.github.io/blob/main/images/Burbon.jpg?raw=true">
        <figcaption>
          <h3>Burbon</h3>
          <p>wiek 8 lat. Groźne spojrzenie ale bardzo kochający</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>
      
<figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejscie.github.io/blob/main/images/Charli.jpg?raw=true"
             srcset="https://github.com/Chell111/przejscie.github.io/blob/main/images/Charli.jpg?raw=true 600w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Charli.jpg?raw=true 1000w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Charli.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejscie.github.io/blob/main/images/Charli.jpg?raw=true">
        <figcaption>
          <h3>Charli</h3>
          <p>6 lat. Bardzo przywiązana do matki</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

<figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejscie.github.io/blob/main/images/Gibi.jpg?raw=true"
             srcset="https://github.com/Chell111/przejscie.github.io/blob/main/images/Gibi.jpg?raw=true 600w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Gibi.jpg?raw=true 1000w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Gibi.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejscie.github.io/blob/main/images/Gibi.jpg?raw=true">
        <figcaption>
          <h3>Gibi</h3>
          <p>1,5 lat. Głodompr, szcza na zasłony</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

<figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejscie.github.io/blob/main/images/Loki.jpg?raw=true"
             srcset="https://github.com/Chell111/przejscie.github.io/blob/main/images/Loki.jpg?raw=true 600w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Loki.jpg?raw=true 1000w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Loki.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejscie.github.io/blob/main/images/Loki.jpg?raw=true">
        <figcaption>
          <h3>Loki</h3>
          <p>9,5 lat. Kocha matkę i głaskanie</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

  <figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejscie.github.io/blob/main/images/Rysiu.jpg?raw=true"
             srcset="https://github.com/Chell111/przejscie.github.io/blob/main/images/Rysiu.jpg?raw=true 600w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Rysiu.jpg?raw=true 1000w, https://github.com/Chell111/przejscie.github.io/blob/main/images/Rysiu.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejscie.github.io/blob/main/images/Rysiu.jpg?raw=true">
        <figcaption>
          <h3>Rysiu</h3>
          <p>5 lat. Znaleziony na ulicy, w nowym domu pokochał życie na nowo</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>

<figure class="card">
        <img class="thumb"
             src="https://github.com/Chell111/przejscie.github.io/blob/main/images/piesek%20oli.jpg?raw=true"
             srcset="https://github.com/Chell111/przejscie.github.io/blob/main/images/piesek%20oli.jpg?raw=true 600w, https://github.com/Chell111/przejscie.github.io/blob/main/images/piesek%20oli.jpg?raw=true 1000w, https://github.com/Chell111/przejscie.github.io/blob/main/images/piesek%20oli.jpg?raw=true 1600w"
             sizes="(max-width:599px) 100vw, (max-width:999px) 48vw, 32vw"
             alt="Krótki opis zdjęcia 3"
             loading="lazy"
             data-full="https://github.com/Chell111/przejscie.github.io/blob/main/images/piesek%20oli.jpg?raw=true">
        <figcaption>
          <h3>Fifek</h3>
          <p>?? lat. Greedy</p>
          <div class="meta">
            <span style="color:var(--muted);font-size:.9rem">4b</span>
            <button class="btn open-btn" type="button" aria-label="Powiększ zdjęcie">Powiększ</button>
          </div>
        </figcaption>
      </figure>
      
      <!-- Add more <figure class="card"> blocks as needed -->
    </main>
  </div>

  <!-- Modal / Lightbox -->
  <div class="modal" id="lightbox" role="dialog" aria-modal="true" aria-hidden="true">
    <div class="modal-inner" role="document">
      <img id="lightbox-img" src="" alt="">
      <div class="caption">
        <div id="lightbox-caption" style="flex:1;"></div>
        <button id="lightbox-close" class="close" aria-label="Zamknij">✕</button>
      </div>
    </div>
  </div>

  <script>
    // Simple lightbox behavior
    (function(){
      const openBtns = document.querySelectorAll('.open-btn');
      const lightbox = document.getElementById('lightbox');
      const lbImg = document.getElementById('lightbox-img');
      const lbCaption = document.getElementById('lightbox-caption');
      const lbClose = document.getElementById('lightbox-close');

      function openFromElement(el){
        // el is the figure.card or a descendant button
        const fig = el.closest('figure.card');
        if(!fig) return;
        const img = fig.querySelector('img');
        const full = img.dataset.full || img.src;
        const alt = img.alt || '';
        const title = fig.querySelector('h3')?.textContent || '';
        const desc = fig.querySelector('p')?.textContent || '';
        lbImg.src = full;
        lbImg.alt = alt;
        lbCaption.textContent = title ? (title + (desc ? ' — ' + desc : '')) : desc || alt;
        lightbox.classList.add('open');
        lightbox.setAttribute('aria-hidden','false');
        // prevent scrolling behind on mobile
        document.documentElement.style.overflow = 'hidden';
      }

      openBtns.forEach(btn=>{
        btn.addEventListener('click', e => openFromElement(e.currentTarget));
      });

      // Allow clicking the image directly as well
      document.querySelectorAll('.thumb').forEach(t=>{
        t.addEventListener('click', e => openFromElement(e.currentTarget));
      });

      function closeLB(){
        lightbox.classList.remove('open');
        lightbox.setAttribute('aria-hidden','true');
        lbImg.src = '';
        lbImg.alt = '';
        document.documentElement.style.overflow = '';
      }

      lbClose.addEventListener('click', closeLB);
      lightbox.addEventListener('click', (e)=>{
        if(e.target === lightbox) closeLB();
      });
      document.addEventListener('keydown', (e)=>{ if(e.key === 'Escape') closeLB(); });
    })();
  </script>
</body>
</html>
