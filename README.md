<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Cuddle of Lurve</title>
  <meta name="description" content="Cuddle of Lurve — professional cuddling services. Comfortable, safe, and consensual cuddling sessions." />
  <style>
    :root{
      --bg:#0b0b0c; /* very dark */
      --panel:#0f0f10;
      --accent:#ff2b2b;
      --muted:#bdbdbd;
      --glass: rgba(255,255,255,0.03);
    }
    html,body{height:100%;}
    body{
      margin:0; font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(255,43,43,0.03), transparent),
                  radial-gradient(1000px 400px at 90% 90%, rgba(255,43,43,0.02), transparent),
                  var(--bg);
      color:#fff;
      -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
      display:flex; align-items:center; justify-content:center; padding:28px;
    }
    .card{
      width:100%; max-width:920px; background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:16px; box-shadow:0 10px 30px rgba(0,0,0,0.6); padding:28px; border:1px solid rgba(255,255,255,0.03);
    }
    header{display:flex; align-items:center; gap:18px;}
    .logo{
      width:72px; height:72px; border-radius:12px; background:linear-gradient(135deg,var(--panel), #121212); display:flex; align-items:center; justify-content:center; font-size:28px; font-weight:700;
      color:#fff; box-shadow:0 6px 18px rgba(0,0,0,0.6);
      border:1px solid rgba(255,255,255,0.02);
    }
    h1{margin:0; font-size:28px; letter-spacing:0.4px; text-shadow:0 0 12px rgba(255,43,43,0.22), 0 0 28px rgba(255,0,0,0.08);}
    p.lead{margin:8px 0 0; color:var(--muted);}    

    .grid{display:grid; grid-template-columns: 1fr 320px; gap:20px; margin-top:22px;}
    .box{background:var(--glass); padding:18px; border-radius:12px; border:1px solid rgba(255,255,255,0.02);}

    .services h2, .booking h2{margin:0 0 12px; font-size:18px; color:#fff; text-shadow:0 0 8px rgba(255,43,43,0.18);}
    .service{display:flex; align-items:center; justify-content:space-between; padding:12px 0; border-bottom:1px dashed rgba(255,255,255,0.03);} 
    .service:last-child{border-bottom:0}
    .service .name{font-weight:600}
    .service .meta{color:var(--muted); font-size:14px}

    .cta{display:flex; gap:10px; margin-top:14px}
    .btn{background:linear-gradient(180deg, rgba(255,43,43,0.12), rgba(255,43,43,0.06)); padding:10px 14px; border-radius:10px; border:1px solid rgba(255,43,43,0.14); cursor:pointer; color:#fff; text-decoration:none; font-weight:600}
    .btn.ghost{background:transparent; border:1px solid rgba(255,255,255,0.06);}

    .note{font-size:13px; color:var(--muted); margin-top:10px}

    .contact-field{display:flex; flex-direction:column; gap:8px;}
    label{font-size:13px; color:var(--muted)}
    input,textarea,select{background:transparent; border:1px solid rgba(255,255,255,0.06); padding:10px; border-radius:8px; color:#fff; outline:none}
    input::placeholder, textarea::placeholder{color:rgba(255,255,255,0.25)}

    footer{margin-top:18px; text-align:center; color:var(--muted); font-size:13px}

    @media (max-width:880px){
      .grid{grid-template-columns:1fr;}
      header{flex-direction:row;}
    }
  </style>
</head>
<body>
  <main class="card">
    <header>
      <div class="logo">💕</div>
      <div>
        <h1>Cuddle of Lurve</h1>
        <p class="lead">Comforting, professional and fully consensual cuddling sessions. Safe space. Clear boundaries.</p>
      </div>
    </header>

    <div class="grid">
      <section class="box services">
        <h2>Our Services & Rates</h2>

        <div class="service">
          <div>
            <div class="name">30 minutes</div>
            <div class="meta">Quick comfort session — ideal for a short unwind</div>
          </div>
          <div class="price">NZ$45</div>
        </div>

        <div class="service">
          <div>
            <div class="name">1 hour</div>
            <div class="meta">Full relaxation session</div>
          </div>
          <div class="price">NZ$80</div>
        </div>

        <p class="note">All sessions are non-sexual. Client and provider consent and comfort are required. Please read the house rules before booking.</p>

        <div class="cta">
          <!-- Replace youremail@example.com with your real contact email -->
          <a class="btn" href="mailto:youremail@example.com?subject=Booking%20Request%20%7C%20Cuddle%20of%20Lurve&body=Hi%2C%0A%0AI%20would%20like%20to%20book%20a%20session.%20Please%20let%20me%20know%20your%20availability.%0A%0D%0AName%3A%0APhone%3A%0APreferred%20Service%3A%20(30%20mins%20%2F%201%20hour)%0A%0AThanks.">Book by email</a>
          <a class="btn ghost" href="#contact">Contact / Questions</a>
        </div>

      </section>

      <aside class="box booking" id="contact">
        <h2>Contact & Quick Booking</h2>
        <p class="note">Use the email button to open your mail app. Or fill the quick message below (note: this just prepares text; it won't send from static GitHub Pages).</p>

        <form onsubmit="prepareMail(event)">
          <div class="contact-field">
            <label for="name">Your name</label>
            <input id="name" placeholder="Your full name" required />
          </div>
          <div class="contact-field">
            <label for="phone">Phone (optional)</label>
            <input id="phone" placeholder="e.g. +64 21 123 4567" />
          </div>
          <div class="contact-field">
            <label for="service">Choose a service</label>
            <select id="service">
              <option>30 minutes — NZ$45</option>
              <option>1 hour — NZ$80</option>
            </select>
          </div>
          <div class="contact-field">
            <label for="notes">Notes / preferred date & time</label>
            <textarea id="notes" rows="4" placeholder="Any preferences or questions"></textarea>
          </div>

          <div style="margin-top:12px; display:flex; gap:10px;">
            <button class="btn" type="submit">Prepare email</button>
            <button class="btn ghost" type="button" onclick="resetForm()">Reset</button>
          </div>
        </form>

        <script>
          function prepareMail(e){
            e.preventDefault();
            const name = document.getElementById('name').value || '';
            const phone = document.getElementById('phone').value || '';
            const service = document.getElementById('service').value;
            const notes = document.getElementById('notes').value || '';
            const subject = encodeURIComponent('Booking Request | Cuddle of Lurve');
            const body = encodeURIComponent(`Hi,%0D%0A%0D%0AI%20would%20like%20to%20book%20a%20session.%0D%0A%0D%0AName: ${name}%0D%0APhone: ${phone}%0D%0AService: ${service}%0D%0AInfo: ${notes}%0D%0A%0D%0AThanks.`);
            // Replace youremail@example.com in the href below with your real email address in the file.
            const mailto = `mailto:youremail@example.com?subject=${subject}&body=${body}`;
            window.location.href = mailto;
          }
          function resetForm(){
            document.getElementById('name').value='';
            document.getElementById('phone').value='';
            document.getElementById('notes').value='';
            document.getElementById('service').selectedIndex = 0;
          }
        </script>

      </aside>
    </div>

    <footer>
      <div>© Cuddle of Lurve — Professional cuddling. All bookings subject to terms.</div>
    </footer>
  </main>
</body>
</html>
