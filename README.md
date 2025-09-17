
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>English Club — Modern UI</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#f5f7fb;
      --card:#ffffff;
      --muted:#6b7280;
      --accent1:#111827;
      --primaryA:#111827;
      --primaryB:#6b21a8;
      --glass: rgba(255,255,255,0.6);
    }
    *{box-sizing:border-box}
    body{font-family:'Poppins',sans-serif;margin:0;background:var(--bg);color:var(--primaryA);-webkit-font-smoothing:antialiased;}
    /* NAV */
    .nav-wrap{position:sticky;top:0;z-index:60;background:rgba(255,255,255,0.7);backdrop-filter: blur(6px);box-shadow:0 6px 18px rgba(15,23,42,0.06);}
    nav{max-width:1200px;margin:auto;display:flex;align-items:center;justify-content:space-between;padding:12px 20px;}
    .logo{font-weight:700;color:var(--primaryB);letter-spacing:-0.5px;}
    .menu{display:flex;gap:18px;align-items:center;}
    .menu a{color:var(--muted);text-decoration:none;font-weight:600;padding:8px 12px;border-radius:10px;transition:all .18s;}
    .menu a:hover{background:linear-gradient(90deg,var(--primaryB),#2575fc);color:#fff;transform:translateY(-2px);}
    .cta{background:linear-gradient(90deg,var(--primaryB),#2575fc);color:#fff;padding:10px 16px;border-radius:12px;text-decoration:none;font-weight:700;}
    /* HERO */
    .hero{max-width:1200px;margin:36px auto;padding:40px 20px;display:grid;grid-template-columns:1fr 520px;gap:30px;align-items:center;}
    .hero-left h1{font-size:46px;margin:0 0 18px 0;line-height:1.03;}
    .hero-left p{color:var(--muted);margin:0 0 22px 0;font-size:16px;}
    .hero-actions{display:flex;gap:12px;align-items:center;}
    .btn-outline{padding:12px 18px;border-radius:12px;border:1px solid rgba(17,24,39,0.08);background:#fff;font-weight:600;}
    .btn-solid{background:linear-gradient(90deg,var(--primaryB),#2575fc);color:#fff;padding:12px 18px;border-radius:12px;border:none;font-weight:700;}
    /* hero visual */
    .hero-right{position:relative;}
    .phone-card{border-radius:22px;padding:22px;background:linear-gradient(180deg,#fff 0%, #fbfdff 100%);box-shadow:0 18px 40px rgba(16,24,40,0.08);display:flex;justify-content:center;align-items:center;height:420px;}
    .phone-card img{max-width:85%;border-radius:14px;object-fit:cover;}
    /* callouts */
    .callout{position:absolute;background:#fff;padding:8px 12px;border-radius:999px;box-shadow:0 6px 20px rgba(16,24,40,0.08);font-size:13px;color:var(--muted);}
    .callout.one{top:28px;left:520px;}
    .callout.two{top:160px;left:440px;}
    .callout.three{top:300px;left:560px;}
    /* sections */
    .section{max-width:1200px;margin:32px auto;padding:40px 22px;}
    .grid{display:grid;gap:22px;}
    .grid-cols-4{grid-template-columns:repeat(auto-fit,minmax(220px,1fr));}
    .card{background:var(--card);border-radius:14px;padding:18px;box-shadow:0 8px 30px rgba(15,23,42,0.06);transition:transform .18s;}
    .card:hover{transform:translateY(-8px);}
    .card h3{margin:0 0 8px 0;}
    .muted{color:var(--muted);font-size:14px;}
    /* Popular / bestseller look */
    .bestsellers{display:flex;gap:18px;align-items:center;justify-content:space-between;margin-bottom:16px;}
    .bs-btn{background:#fff;border:1px solid rgba(16,24,40,0.06);padding:10px 14px;border-radius:12px;font-weight:700;}
    .cards-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;}
    .lesson-img{width:100%;height:160px;object-fit:cover;border-radius:10px;margin-bottom:12px;}
    /* grammar list style */
    .grammar-list{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:16px;}
    .link-item{display:block;padding:12px;border-radius:10px;background:linear-gradient(180deg, #fff,#fbfdff);box-shadow:inset 0 -1px 0 rgba(0,0,0,0.02);text-decoration:none;color:var(--primaryA);}
    .site-tag{display:inline-block;background:rgba(37,117,252,0.08);color:#2575fc;padding:6px 10px;border-radius:999px;font-weight:700;margin-left:8px;font-size:12px;}
    /* dictionary area */
    .dict-row{display:flex;gap:16px;flex-wrap:wrap;}
    .dict-left{flex:1;min-width:260px;}
    .dict-right{flex:1;min-width:320px;}
    .audio-btn{background:linear-gradient(90deg,var(--primaryB),#2575fc);color:#fff;padding:8px 12px;border-radius:999px;border:none;}
    /* responsive */
    @media(max-width:1000px){
      .hero{grid-template-columns:1fr;gap:26px;padding:24px 16px;}
      .hero-right{order:-1;height:360px;}
      .phone-card{height:320px;}
      .callout{display:none;}
    }
    @media(max-width:600px){
      .hero-left h1{font-size:28px;}
      nav{padding:8px 12px;}
      .menu{display:none}
    }
  </style>
</head>
<body>

  <div class="nav-wrap"><nav>
    <div class="logo">English<span style="color:#2575fc">Club</span></div>
    <div class="menu">
      <a href="#activities">Hoạt động</a>
      <a href="#vocabulary">Từ vựng</a>
      <a href="#grammar">Ngữ pháp</a>
      <a href="#dictionary">Từ điển</a>
      <a href="#videos">Video</a>
    </div>
    <a class="cta" href="#register">Tham gia ngay</a>
  </nav></div>

  <!-- HERO -->
  <header class="hero" aria-label="Giới thiệu">
    <div class="hero-left">
      <h1>Học tiếng Anh hiện đại — thực hành & tự tin</h1>
      <p>Giao diện này hướng tới trải nghiệm học năng động: bài học ngắn, từ điển tra nhanh, links tài nguyên uy tín và hoạt động thực tế cho CLB.</p>
      <div class="hero-actions">
        <a class="btn-solid" href="#grammar">Xem ngữ pháp</a>
        <a class="btn-outline" href="#dictionary">Tra từ ngay</a>
      </div>
      <div style="margin-top:18px;color:var(--muted);font-size:14px;">Các nguồn hữu ích: <span class="site-tag">British Council</span> <span class="site-tag">Cambridge</span> <span class="site-tag">Oxford</span></div>
    </div>

    <div class="hero-right">
      <div class="phone-card">
        <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=900&q=60" alt="illustration">
      </div>
      <div class="callout one">📝 Lesson hub</div>
      <div class="callout two">🔊 Pronunciation tips</div>
      <div class="callout three">🧠 Vocabulary boosters</div>
    </div>
  </header>

  <!-- Activities -->
  <section id="activities" class="section">
    <div class="bestsellers">
      <h2>Hoạt động nổi bật</h2>
      <a class="bs-btn" href="#register">Tham gia CLB</a>
    </div>
    <div class="grid grid-cols-4">
      <div class="card"><h3>Thảo luận chủ đề</h3><p class="muted">Discussion club - mỗi tuần 1 topic, chia đội, phản biện.</p></div>
      <div class="card"><h3>Practice & Roleplay</h3><p class="muted">Tình huống thực tế: phỏng vấn, order đồ, travel talk.</p></div>
      <div class="card"><h3>Mini contests</h3><p class="muted">Hùng biện, kể chuyện ngắn - thưởng điểm thành viên.</p></div>
      <div class="card"><h3>Exchange</h3><p class="muted">Giao lưu với bạn bè quốc tế qua Zoom.</p></div>
    </div>
  </section>

  <!-- Vocabulary -->
  <section id="vocabulary" class="section">
    <h2>Chủ đề từ vựng</h2>
    <div class="cards-row">
      <div class="card">
        <img class="lesson-img" src="https://images.unsplash.com/photo-1502920917128-1aa500764b33?auto=format&fit=crop&w=800&q=60" alt="Travel">
        <h3>Travel & Transport</h3>
        <p class="muted">airport, baggage, itinerary, boarding pass...</p>
      </div>
      <div class="card">
        <img class="lesson-img" src="https://images.unsplash.com/photo-1515879218367-8466d910aaa4?auto=format&fit=crop&w=800&q=60" alt="Food">
        <h3>Food & Dining</h3>
        <p class="muted">menu, reservation, appetizer, dessert...</p>
      </div>
      <div class="card">
        <img class="lesson-img" src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=800&q=60" alt="Tech">
        <h3>Technology</h3>
        <p class="muted">software, device, update, AI, network...</p>
      </div>
    </div>
  </section>

  <!-- Grammar modern links -->
  <section id="grammar" class="section">
    <h2>Ngữ pháp — Tài nguyên hữu ích (cập nhật)</h2>
    <p class="muted">Các link dưới đây dẫn đến nguồn uy tín (British Council, Cambridge, Oxford, Grammarly, Purdue, BBC, Khan Academy, Perfect-English-Grammar)</p>

    <div class="grammar-list" aria-label="Danh sách ngữ pháp">
      <!-- Tenses -->
      <a class="link-item" href="https://learnenglish.britishcouncil.org/grammar" target="_blank">
        <strong>Grammar Reference (British Council)</strong><span class="site-tag">British Council</span>
        <div class="muted">Bộ tham khảo ngữ pháp toàn diện: thì, câu, mệnh đề, câu điều kiện...</div>
      </a>

      <a class="link-item" href="https://dictionary.cambridge.org/grammar/british-grammar/" target="_blank">
        <strong>British & American Grammar (Cambridge Dictionary)</strong><span class="site-tag">Cambridge</span>
        <div class="muted">Giải thích ngắn gọn, ví dụ rõ ràng và khác biệt Uk/Us.</div>
      </a>

      <a class="link-item" href="https://www.oxfordonlineenglish.com/free-english-grammar-lessons" target="_blank">
        <strong>Free Grammar Lessons</strong><span class="site-tag">Oxford Online</span>
        <div class="muted">Bài học dạng video + văn bản, phù hợp tự học.</div>
      </a>

      <a class="link-item" href="https://www.grammarly.com/blog/grammar/" target="_blank">
        <strong>Grammar Tips & Guides</strong><span class="site-tag">Grammarly</span>
        <div class="muted">Mẹo, giải thích lỗi thường gặp và ví dụ đơn giản.</div>
      </a>

      <a class="link-item" href="https://owl.purdue.edu/owl/english_as_a_second_language/esl_students/grammar/index.html" target="_blank">
        <strong>Writing & Grammar (Purdue OWL)</strong><span class="site-tag">Purdue OWL</span>
        <div class="muted">Tập trung vào viết, cấu trúc câu, dấu câu, style.</div>
      </a>

      <a class="link-item" href="https://www.bbc.co.uk/learningenglish" target="_blank">
        <strong>BBC Learning English</strong><span class="site-tag">BBC</span>
        <div class="muted">Bài nghe + ngữ pháp theo chủ đề, hữu ích cho kỹ năng nghe.</div>
      </a>

      <a class="link-item" href="https://www.khanacademy.org/humanities/grammar" target="_blank">
        <strong>Khan Academy Grammar</strong><span class="site-tag">Khan Academy</span>
        <div class="muted">Video bài giảng & bài tập cơ bản đến nâng cao.</div>
      </a>

      <a class="link-item" href="https://www.perfect-english-grammar.com/" target="_blank">
        <strong>Perfect English Grammar</strong><span class="site-tag">PerfectEG</span>
        <div class="muted">Bài tập & giải thích hữu dụng cho luyện tập.</div>
      </a>

      <a class="link-item" href="https://www.englishpage.com/" target="_blank">
        <strong>EnglishPage — Grammar & Exercises</strong><span class="site-tag">EnglishPage</span>
        <div class="muted">Tài liệu luyện tập nâng cao: conditionals, modals, tenses.</div>
      </a>
    </div>
  </section>

  <!-- Dictionary -->
  <section id="dictionary" class="section">
    <h2>📚 Từ điển tra nhanh</h2>
    <div class="card dict-row">
      <div class="dict-left">
        <input id="wordInput" placeholder="Nhập từ (ví dụ: example)" />
        <div style="display:flex;gap:8px;margin-top:8px;">
          <button class="audio-btn" onclick="playTTS('uk')">🔊 UK</button>
          <button class="audio-btn" onclick="playTTS('us')">🔊 US</button>
        </div>
        <div id="result" style="margin-top:12px;"></div>
      </div>
      <div class="dict-right">
        <p class="muted">Nguồn dữ liệu: <strong>Free Dictionary API</strong> (dictionaryapi.dev). Nếu cần tích hợp Oxford/Cambridge API, bạn sẽ cần key API từ nhà cung cấp.</p>
        <p class="muted">Các phát âm UK/US dùng Text-to-Speech (gTTS proxy bằng URL miễn phí) — nếu muốn chất lượng cao hơn, tích hợp API TTS trả phí.</p>
      </div>
    </div>
  </section>

  <!-- Videos -->
  <section id="videos" class="section">
    <h2>Video học nổi bật</h2>
    <div class="cards-row">
      <div class="card"><h3>Ngữ pháp căn bản</h3><iframe src="https://www.youtube.com/embed/HAnw168huqA" frameborder="0" allowfullscreen></iframe></div>
      <div class="card"><h3>Từ vựng hiệu quả</h3><iframe src="https://www.youtube.com/embed/l1EssrLxt7E" frameborder="0" allowfullscreen></iframe></div>
    </div>
  </section>

  <!-- Register -->
  <section id="register" class="section">
    <h2>Tham gia CLB</h2>
    <div class="card" style="display:flex;gap:12px;flex-wrap:wrap;">
      <input placeholder="Họ và tên" id="rname" style="flex:1;min-width:220px;" />
      <input placeholder="Email" id="remail" style="flex:1;min-width:220px;" />
      <input placeholder="Số điện thoại (nếu có)" id="rphone" style="flex:1;min-width:220px;" />
      <input placeholder="Trình độ (ví dụ: A2/B1...)" id="rlevel" style="flex:1;min-width:220px;" />
      <button onclick="submitRegister()" style="margin-top:6px;">Gửi đăng ký</button>
      <div id="regmsg" style="width:100%;margin-top:8px;color:green;"></div>
    </div>
  </section>

  <footer style="padding:28px 20px;text-align:center;">
    <div style="max-width:1200px;margin:auto;color:#fff;">
      © 2025 English Club — Thiết kế hiện đại • Liên hệ: englishclub@example.com
    </div>
  </footer>

<script>
  async function lookupEntry(word){
    const res = await fetch(`https://api.dictionaryapi.dev/api/v2/entries/en/${encodeURIComponent(word)}`);
    if(!res.ok) return null;
    const data = await res.json();
    return data[0];
  }

  async function lookupWord(){
    const w = document.getElementById('wordInput').value.trim();
    if(!w) return;
    const entry = await lookupEntry(w);
    const out = document.getElementById('result');
    if(!entry){ out.innerHTML = '<p style="color:#b91c1c">Không tìm thấy từ.</p>'; return; }
    let html = `<h3 style="margin:0">${entry.word}</h3>`;
    // phonetics
    if(entry.phonetics && entry.phonetics.length){
      const phon = entry.phonetics.filter(p=>p.text).map(p=>p.text).join(' • ');
      if(phon) html += `<p class="muted">Phiên âm: ${phon}</p>`;
    }
    // audio list
    if(entry.phonetics && entry.phonetics.length){
      entry.phonetics.forEach(p=>{
        if(p.audio) html += `<audio controls src="${p.audio}" style="width:100%;margin-top:8px"></audio>`;
      });
    }
    // meanings
    entry.meanings.forEach(m=>{
      html += `<h4 style="margin:8px 0 4px 0">${m.partOfSpeech}</h4><ul>`;
      m.definitions.forEach(d=>{
        html += `<li>${d.definition}${d.example ? '<br><em style="color:var(--muted)">'+d.example+'</em>' : ''}</li>`;
      });
      html += `</ul>`;
      if(m.synonyms && m.synonyms.length) html += `<p class="muted">Synonyms: ${m.synonyms.slice(0,8).join(', ')}</p>`;
    });
    out.innerHTML = html;
  }

  // play TTS via a public TTS endpoint (NOTE: this is a lightweight demo; for production use paid TTS)
  function playTTS(variant){
    const w = document.getElementById('wordInput').value.trim();
    if(!w) return alert('Nhập từ trước khi phát âm');
    // use Google Translate TTS endpoint pattern (may be rate-limited); this is for demo only
    const t = variant === 'us' ? 'en' : 'en-GB';
    const url = `https://translate.google.com/translate_tts?ie=UTF-8&q=${encodeURIComponent(w)}&tl=${t}&client=tw-ob`;
    const audio = new Audio(url);
    audio.play().catch(()=> alert('Phát âm tạm thời không khả dụng. Với chất lượng cao hơn, tích hợp API TTS trả phí.'));
  }

  // submit register (demo)
  function submitRegister(){
    const n = document.getElementById('rname').value.trim();
    const e = document.getElementById('remail').value.trim();
    if(!n||!e){ document.getElementById('regmsg').innerText='Vui lòng nhập họ tên và email.'; return; }
    document.getElementById('regmsg').innerText = 'Cảm ơn ' + n + '! Chúng tôi đã nhận đăng ký.';
    // here you can add AJAX to send data to server or save to Google Sheets / Firebase
  }

  // auto lookup when pressing Enter
  document.getElementById('wordInput').addEventListener('keydown', function(e){
    if(e.key === 'Enter') lookupWord();
  });
</script>
</body>
</html>
