<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>For You my girl❤️</title>
  <meta name="description" content="A little website I made to tell you how much you mean to me."/>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg-1:#0f1022; --bg-2:#1a1b3a; --pink:#ff5faf; --rose:#ff8fb1; --gold:#ffd166; --mint:#b8f2e6; --white:#fff; --fade:#ffffffa8;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0}
    body{
      font-family:'Poppins',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
      color:var(--white);
      background: radial-gradient(1200px 800px at 10% 10%, #2a2356 0%, transparent 60%) ,
                  radial-gradient(1000px 700px at 90% 30%, #1d3a5a 0%, transparent 60%),
                  linear-gradient(135deg, var(--bg-1), var(--bg-2));
      overflow-x:hidden;
    }
    /* Floating hearts */
    .hearts{position:fixed; inset:0; pointer-events:none; z-index:1; overflow:hidden}
    .heart{position:absolute; font-size:18px; opacity:.5; animation:float 8s linear infinite}
    @keyframes float{from{transform:translateY(100vh) translateX(0) rotate(0)} to{transform:translateY(-10vh) translateX(40px) rotate(360deg)}}

    header{
      position:relative; z-index:2; display:flex; align-items:center; justify-content:center; text-align:center;
      min-height:90vh; padding:64px 20px 32px; isolation:isolate;
    }
    .hero-card{
      background: rgba(255,255,255,0.06); backdrop-filter: blur(8px);
      border:1px solid rgba(255,255,255,.12);
      border-radius:28px; padding:32px; max-width:920px; width:100%; box-shadow:0 20px 60px rgba(0,0,0,.35);
    }
    .script{font-family:'Great Vibes', cursive; font-size:56px; line-height:1; color:var(--rose)}
    .title{font-weight:800; font-size:34px; margin:8px 0 6px}
    .sub{color:var(--fade); font-size:16px}
    .divider{height:1px; background:linear-gradient(90deg,transparent, rgba(255,255,255,.25), transparent); margin:22px 0}

    .cta{
      display:flex; gap:12px; flex-wrap:wrap; justify-content:center; margin-top:18px
    }
    .btn{
      border:none; border-radius:999px; padding:14px 22px; font-weight:700; letter-spacing:.3px; cursor:pointer;
      transition: transform .08s ease, box-shadow .2s ease; position:relative
    }
    .btn:active{transform:translateY(1px)}
    .btn-primary{background:linear-gradient(135deg, var(--rose), var(--pink)); color:#1a0210; box-shadow:0 10px 24px rgba(255,95,175,.35)}
    .btn-ghost{background:transparent; color:var(--white); border:1px solid rgba(255,255,255,.25)}

    /* Sections */
    section{position:relative; z-index:2; padding:64px 20px}
    .wrap{max-width:1100px; margin:0 auto}
    h2{margin:0 0 14px; font-size:28px}
    p.lead{color:var(--fade)}

    /* Video card */
    .card{background:rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.12); border-radius:20px; padding:14px}
    video, img{max-width:100%; border-radius:16px; display:block}

    /* Gallery */
    .grid{display:grid; grid-template-columns:repeat(12,1fr); gap:12px}
    .col-6{grid-column:span 6}
    .col-4{grid-column:span 4}
    .col-3{grid-column:span 3}
    @media (max-width:900px){ .col-6,.col-4,.col-3{grid-column:span 12} }

    .thumb{position:relative; overflow:hidden; border-radius:14px; cursor:pointer}
    .thumb img{transition: transform .5s ease}
    .thumb:hover img{transform:scale(1.06)}

    /* Timeline */
    .timeline{position:relative; margin:26px 0 0; padding-left:20px}
    .timeline:before{content:""; position:absolute; left:10px; top:0; bottom:0; width:2px; background:rgba(255,255,255,.18)}
    .t-item{position:relative; margin:18px 0 18px 18px}
    .t-item:before{content:"❤"; position:absolute; left:-26px; top:0; filter:drop-shadow(0 2px 6px rgba(0,0,0,.35))}
    .t-title{font-weight:700}
    .t-note{color:var(--fade)}

    /* Lightbox */
    .lightbox{position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(0,0,0,.75); z-index:50}
    .lightbox.open{display:flex}
    .lightbox img{max-width:92vw; max-height:86vh}

    /* Music Toggle */
    .music{position:fixed; right:20px; bottom:20px; z-index:30}
    .music button{background:rgba(255,255,255,.12); border:1px solid rgba(255,255,255,.25); color:var(--white); border-radius:999px; padding:10px 14px; font-weight:700; cursor:pointer}

    /* Proposal Modal */
    .modal{position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(0,0,0,.6); z-index:60}
    .modal.open{display:flex}
    .modal-card{background:#1b1429; border:1px solid rgba(255,255,255,.18); border-radius:22px; padding:26px; width:min(560px, 92vw); text-align:center}
    .modal-card h3{margin:0 0 10px}
    .modal-card p{color:var(--fade)}
  </style>
</head>
<body>
  <!-- Floating hearts -->
  <div class="hearts" aria-hidden="true" id="hearts"></div>

  <header>
    <div class="hero-card">
      <div class="script">For my favorite person</div>
      <div class="title">Hey <span id="herName">You</span>, I have something to say…</div>
      <div class="sub" id="typewrite">I made this just for you ✨</div>
      <div class="divider"></div>
      <p class="sub">Every moment with you feels like home. So I built a tiny home on the internet… our home. Scroll down with me? ♡</p>
      <div class="cta">
        <button class="btn btn-primary" id="btnAsk">Will you be mine? 💍</button>
        <button class="btn btn-ghost" id="btnScroll">See our memories ⟶</button>
      </div>
    </div>
  </header>

  <section>
    <div class="wrap">
      <h2>Our Little Movie 🎞️</h2>
      <p class="lead">Press play and relive our sweetest moments. (Replace this with your video!)</p>
      <div class="card">
        <video id="memVideo" controls poster="assets/video-cover.jpg">
          <source src="assets/our-moments.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <h2>Snapshots I Love 📸</h2>
      <p class="lead">A few frames where time decided to stop and smile.</p>
      <div class="grid" id="gallery">
        <!-- Replace image sources with your own -->
        <div class="col-4"><div class="thumb"><img src="assets/img1.jpg" alt="Memory 1"></div></div>
        <div class="col-4"><div class="thumb"><img src="assets/img2.jpg" alt="Memory 2"></div></div>
        <div class="col-4"><div class="thumb"><img src="assets/img3.jpg" alt="Memory 3"></div></div>
        <div class="col-3"><div class="thumb"><img src="assets/img4.jpg" alt="Memory 4"></div></div>
        <div class="col-6"><div class="thumb"><img src="assets/img5.jpg" alt="Memory 5"></div></div>
        <div class="col-3"><div class="thumb"><img src="assets/img6.jpg" alt="Memory 6"></div></div>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <h2>Our Storyline 🗓️</h2>
      <div class="timeline">
        <div class="t-item">
          <div class="t-title">The first hello</div>
          <div class="t-note">I didn’t know a simple hi could change so much.</div>
        </div>
        <div class="t-item">
          <div class="t-title">First laugh together</div>
          <div class="t-note">That sound still lives rent‑free in my head.</div>
        </div>
        <div class="t-item">
          <div class="t-title">Our secret place</div>
          <div class="t-note">Where the world went quiet and it was just us.</div>
        </div>
        <div class="t-item">
          <div class="t-title">Today</div>
          <div class="t-note">I’m asking you to be my forever.</div>
        </div>
      </div>
    </div>
  </section>

  <footer style="text-align:center; padding:40px 20px; color:var(--fade)">
    Made with all my love • <span id="footerName">— yours always</span> 💖
  </footer>

  <!-- Lightbox -->
  <div class="lightbox" id="lightbox" role="dialog" aria-modal="true">
    <img src="" alt="Expanded memory" id="lightboxImg"/>
  </div>

  <!-- Proposal Modal -->
  <div class="modal" id="modal">
    <div class="modal-card">
      <div class="script" style="font-size:44px; color:var(--gold)">Will you be mine?</div>
      <h3>Not just today — every day.</h3>
      <p>From this moment on, I want to collect seconds with you. The ordinary ones, the loud ones, the quiet ones — all of them. If you say yes, I promise to keep choosing you in every chapter. 💫</p>
      <div class="cta">
        <button class="btn btn-primary" id="btnYes">Yes 💖</button>
        <button class="btn btn-ghost" id="btnShy">I'm shy 🙈</button>
      </div>
    </div>
  </div>

  <!-- Music Toggle -->
  <div class="music">
    <button id="musicBtn">Play music ♫</button>
    <audio id="song" preload="none">
      <source src="assets/song.mp3" type="audio/mpeg" />
    </audio>
  </div>

  <script>
    // ===== Personalize quickly =====
    const HER_NAME = 'My Love'; // ← change this
    const YOUR_NAME = 'Shivay'; // ← change this (shows in footer)
    document.getElementById('herName').textContent = HER_NAME;
    document.getElementById('footerName').textContent = `— ${YOUR_NAME}`;

    // ===== Floating hearts =====
    const hearts = document.getElementById('hearts');
    const heartSymbols = ['❤','💖','💗','💓','💕'];
    function spawnHeart(){
      const h = document.createElement('div');
      h.className='heart';
      h.textContent = heartSymbols[Math.floor(Math.random()*heartSymbols.length)];
      h.style.left = Math.random()*100 + 'vw';
      h.style.animationDuration = 6 + Math.random()*6 + 's';
      h.style.fontSize = 14 + Math.random()*20 + 'px';
      hearts.appendChild(h);
      setTimeout(()=>h.remove(), 12000);
    }
    for(let i=0;i<24;i++) setTimeout(spawnHeart, i*300);
    setInterval(spawnHeart, 700);

    // ===== Typewriter effect =====
    const tw = document.getElementById('typewrite');
    const messages = [
      'I made this just for you ✨',
      'Because you make everything better 💫',
      'Scroll to see our memories 📸'
    ];
    let mi=0, ci=0, typing=true;
    function type(){
      const txt = messages[mi];
      if(typing){
        tw.textContent = txt.slice(0, ++ci);
        if(ci===txt.length){ typing=false; setTimeout(type, 1200); return; }
      } else {
        tw.textContent = txt.slice(0, --ci);
        if(ci===0){ typing=true; mi=(mi+1)%messages.length; }
      }
      setTimeout(type, typing?45:25);
    }
    setTimeout(type, 800);

    // ===== Scroll to memories =====
    document.getElementById('btnScroll').addEventListener('click', ()=>{
      window.scrollTo({top: window.innerHeight, behavior:'smooth'});
    });

    // ===== Lightbox =====
    const lb = document.getElementById('lightbox');
    const lbImg = document.getElementById('lightboxImg');
    document.getElementById('gallery').addEventListener('click', e=>{
      const img = e.target.closest('img');
      if(!img) return;
      lbImg.src = img.src; lb.classList.add('open');
    });
    lb.addEventListener('click', ()=> lb.classList.remove('open'));

    // ===== Music toggle =====
    const audio = document.getElementById('song');
    const musicBtn = document.getElementById('musicBtn');
    let playing = false;
    musicBtn.addEventListener('click', async ()=>{
      try{
        if(!playing){ await audio.play(); playing = true; musicBtn.textContent='Pause music ⏸'; }
        else{ audio.pause(); playing=false; musicBtn.textContent='Play music ♫'; }
      }catch(err){ alert('Tap the screen once, then try play again (browser needs interaction).'); }
    });

    // ===== Proposal modal =====
    const modal = document.getElementById('modal');
    document.getElementById('btnAsk').addEventListener('click', ()=> modal.classList.add('open'));
    document.getElementById('btnShy').addEventListener('click', ()=> modal.classList.remove('open'));

    // ===== Confetti on YES =====
    document.getElementById('btnYes').addEventListener('click', ()=>{
      modal.classList.remove('open');
      celebration();
      setTimeout(()=>{
        // Optional: scroll to video after yes
        document.getElementById('memVideo').scrollIntoView({behavior:'smooth'});
      }, 400);
    });

    function celebration(){
      // simple emoji confetti
      for(let i=0;i<120;i++){
        setTimeout(()=>{
          const span=document.createElement('span');
          span.textContent = ['🎉','✨','💖','🌟','💍'][Math.floor(Math.random()*5)];
          span.style.position='fixed';
          span.style.left = Math.random()*100 + 'vw';
          span.style.top = '-10px';
          span.style.fontSize = (16+Math.random()*24)+'px';
          span.style.zIndex = 100;
          span.style.transition = 'transform 1.2s ease-out, opacity 1.2s ease-out';
          document.body.appendChild(span);
          requestAnimationFrame(()=>{
            span.style.transform = `translateY(${110+Math.random()*40}vh) rotate(${(Math.random()*720-360)}deg)`;
            span.style.opacity = .1;
          });
          setTimeout(()=>span.remove(), 1500);
        }, i*8);
      }
    }
  </script>
</body>
</html>
