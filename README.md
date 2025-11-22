<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PixelPro GFX</title>
  <link rel="stylesheet" href="style.css" />
  <style>
    body { margin:0; font-family: Arial, sans-serif; background:#0a0a0a; color:white; overflow-x:hidden; }
    /* Preloader */
    #preloader { position:fixed; top:0; left:0; width:100%; height:100%; background:#000; display:flex; align-items:center; justify-content:center; z-index:9999; }
    #preloader .loader { width:60px; height:60px; border:6px solid #222; border-top-color:#0ff; border-radius:50%; animation:spin 1s linear infinite; }
    @keyframes spin { to { transform:rotate(360deg);} }

    /* Scroll Animation */
    .reveal { opacity:0; transform:translateY(40px); transition:0.7s; }
    .reveal.active { opacity:1; transform:translateY(0); }

    header { text-align:center; padding:60px 20px; }
    h1 { font-size:3rem; color:#0ff; text-shadow:0 0 15px #0ff; }
    .section { padding:60px 20px; max-width:900px; margin:auto; }

    /* Reviews */
    .reviews { display:grid; gap:20px; }
    .review-card { background:rgba(255,255,255,0.05); border-radius:20px; padding:20px; backdrop-filter:blur(10px); border:1px solid rgba(255,255,255,0.1); }
    .review-card h3 { margin:0; color:#0ff; }

  </style>
</head>
<body>

  <!-- PRELOADER -->
  <div id="preloader"><div class="loader"></div></div>

  <header class="reveal">
    <h1>PixelPro GFX</h1>
    <p>Professional Gaming Thumbnails • Fast Delivery • High Quality</p>
  </header>

  <!-- Reviews Section -->
  <section class="section reveal">
    <h2 style="color:#0ff; text-shadow:0 0 10px #0ff;">Client Reviews ⭐</h2>
    <div class="reviews">
      <div class="review-card">
        <h3>@ShadowYT</h3>
        <p>“Bro delivered in 10 minutes 🔥🔥 Absolutely insane quality!”</p>
      </div>
      <div class="review-card">
        <h3>@FrostGamer</h3>
        <p>“Clean designs and fast edits. Worth every rupee 💯”</p>
      </div>
      <div class="review-card">
        <h3>@RoguePlays</h3>
        <p>“Better than paid designers on Fiverr. Respect 👑”</p>
      </div>
    </div>
  </section>

  <script>
    // Preloader
    window.addEventListener('load', () => {
      document.getElementById('preloader').style.display='none';
    });

    // Reveal on scroll
    function reveal(){
      let reveals = document.querySelectorAll('.reveal');
      for(let r of reveals){
        let windowHeight = window.innerHeight;
        let elementTop = r.getBoundingClientRect().top;
        if(elementTop < windowHeight - 50){ r.classList.add('active'); }
      }
    }
    window.addEventListener('scroll', reveal);
    reveal();
  </script>
</body>
</html>
