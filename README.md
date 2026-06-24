<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>QuitGum Pakistan — Quit Smoking, Start Living</title>
<style>
  *{margin:0;padding:0;box-sizing:border-box}
  :root{
    --green:#3B6D11;--green-light:#EAF3DE;--green-mid:#639922;
    --teal:#0F6E56;--teal-light:#E1F5EE;--teal-mid:#1D9E75;
    --amber:#854F0B;--amber-light:#FAEEDA;
    --text-dark:#2C2C2A;--text-mid:#5F5E5A;--text-light:#888780;
    --bg:#F8FBF6;--white:#ffffff
  }
  html{scroll-behavior:smooth}
  body{font-family:'Segoe UI',Arial,sans-serif;background:var(--bg);color:var(--text-dark);line-height:1.7}

  /* NAV */
  nav{background:#fff;border-bottom:1.5px solid #C0DD97;padding:14px 32px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:999;box-shadow:0 2px 8px rgba(0,0,0,.04)}
  .nav-logo{display:flex;align-items:center;gap:10px}
  .logo-icon{width:40px;height:40px;border-radius:50%;background:var(--green-light);border:2px solid var(--green-mid);display:flex;align-items:center;justify-content:center;font-size:22px}
  .logo-text{font-size:17px;font-weight:700;color:var(--green)}
  .logo-sub{font-size:11px;color:var(--text-mid);margin-top:-2px}
  .nav-links{display:flex;gap:6px;list-style:none}
  .nav-links a{font-size:13px;color:var(--text-mid);text-decoration:none;font-weight:500;padding:6px 12px;border-radius:6px;transition:.2s}
  .nav-links a:hover{background:var(--green-light);color:var(--green)}
  .nav-cta{background:var(--green);color:#fff !important;border-radius:6px;padding:6px 16px !important}
  .nav-cta:hover{background:var(--teal) !important;color:#fff !important}

  /* HERO */
  .hero{background:linear-gradient(135deg,#EAF3DE 0%,#E1F5EE 55%,#FAEEDA 100%);padding:80px 24px 64px;text-align:center}
  .hero-badge{display:inline-block;background:#fff;color:var(--green);border:1.5px solid #97C459;font-size:12px;font-weight:700;padding:6px 16px;border-radius:20px;margin-bottom:24px;letter-spacing:.5px}
  .hero h1{font-size:48px;font-weight:800;color:var(--green);line-height:1.1;margin-bottom:18px}
  .hero h1 span{color:var(--teal)}
  .hero-sub{font-size:17px;color:var(--text-mid);max-width:560px;margin:0 auto 32px}
  .hero-btns{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;margin-bottom:28px}
  .btn-primary{background:var(--green);color:#fff;border:none;padding:14px 32px;border-radius:10px;font-size:15px;font-weight:700;cursor:pointer;text-decoration:none;display:inline-block;transition:.2s}
  .btn-primary:hover{background:var(--teal);transform:translateY(-1px)}
  .btn-secondary{background:#fff;color:var(--green);border:2px solid var(--green-mid);padding:14px 32px;border-radius:10px;font-size:15px;font-weight:700;cursor:pointer;text-decoration:none;display:inline-block;transition:.2s}
  .btn-secondary:hover{background:var(--green-light);transform:translateY(-1px)}
  .hero-price{background:#fff;display:inline-block;padding:12px 28px;border-radius:30px;border:1.5px solid #C0DD97;font-size:14px;color:var(--text-mid)}
  .hero-price strong{color:var(--green);font-size:20px}
  .hero-stats{display:flex;gap:32px;justify-content:center;margin-top:36px;flex-wrap:wrap}
  .stat{text-align:center}
  .stat-num{font-size:28px;font-weight:800;color:var(--green)}
  .stat-label{font-size:12px;color:var(--text-mid);margin-top:2px}

  /* SECTIONS */
  .section{padding:60px 24px}
  .section-title{text-align:center;margin-bottom:40px}
  .section-title h2{font-size:30px;font-weight:800;color:var(--text-dark);margin-bottom:8px}
  .section-title p{font-size:15px;color:var(--text-mid)}
  .line{width:56px;height:3px;background:var(--green-mid);margin:12px auto 0;border-radius:2px}

  /* FEATURES */
  .features-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:18px;max-width:960px;margin:0 auto}
  .feature-card{background:#fff;border:1px solid #C0DD97;border-radius:14px;padding:26px 20px;text-align:center;transition:.2s}
  .feature-card:hover{transform:translateY(-3px);box-shadow:0 8px 24px rgba(63,109,17,.1)}
  .feature-icon{width:56px;height:56px;background:var(--green-light);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:26px;margin:0 auto 16px}
  .feature-card h3{font-size:15px;font-weight:700;color:var(--green);margin-bottom:8px}
  .feature-card p{font-size:13px;color:var(--text-mid)}

  /* HOW IT WORKS */
  .how-bg{background:#EAF3DE}
  .steps{display:flex;max-width:900px;margin:0 auto;flex-wrap:wrap;justify-content:center;gap:8px}
  .step{flex:1;min-width:160px;max-width:200px;text-align:center;padding:24px 12px;position:relative}
  .step-num{width:48px;height:48px;background:var(--green);color:#fff;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:20px;font-weight:800;margin:0 auto 14px}
  .step h3{font-size:14px;font-weight:700;color:var(--green);margin-bottom:6px}
  .step p{font-size:12px;color:var(--text-mid)}
  .step-arrow{font-size:20px;color:#97C459;display:flex;align-items:center;padding-top:36px}

  /* PRICING */
  .pricing-card{max-width:520px;margin:0 auto;background:#fff;border:2.5px solid var(--green-mid);border-radius:20px;overflow:hidden;box-shadow:0 12px 40px rgba(63,109,17,.12)}
  .pricing-head{background:linear-gradient(135deg,var(--green),var(--teal));color:#fff;padding:32px;text-align:center}
  .pricing-head h3{font-size:20px;font-weight:700;margin-bottom:4px;opacity:.9}
  .pricing-head .price{font-size:52px;font-weight:900;line-height:1}
  .pricing-head .price-sub{font-size:13px;opacity:.8;margin-top:6px}
  .pricing-body{padding:28px}
  .pricing-row{display:flex;justify-content:space-between;align-items:center;padding:12px 0;border-bottom:1px solid #EAF3DE;font-size:14px}
  .pricing-row:last-of-type{border-bottom:none}
  .pricing-row .label{color:var(--text-mid)}
  .pricing-row .val{font-weight:700;color:var(--text-dark)}
  .profit-badge{background:var(--teal-light);color:var(--teal);padding:4px 12px;border-radius:20px;font-size:12px;font-weight:700}

  /* STP */
  .stp-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;max-width:860px;margin:0 auto}
  .stp-card{background:#fff;border-radius:14px;border:1px solid #C0DD97;padding:24px 20px}
  .stp-label{font-size:11px;font-weight:800;letter-spacing:1px;color:var(--green-mid);text-transform:uppercase;margin-bottom:10px}
  .stp-card h3{font-size:17px;font-weight:700;color:var(--text-dark);margin-bottom:8px}
  .stp-card p{font-size:13px;color:var(--text-mid)}

  /* ANSOFF */
  .ansoff-grid{display:grid;grid-template-columns:1fr 1fr;gap:3px;max-width:600px;margin:0 auto;border-radius:14px;overflow:hidden;border:1px solid #C0DD97}
  .ansoff-cell{padding:24px 20px;background:#fff}
  .ansoff-cell:nth-child(1){background:#EAF3DE}
  .ansoff-cell:nth-child(2){background:#E1F5EE}
  .ansoff-cell:nth-child(3){background:#FAEEDA}
  .ansoff-cell:nth-child(4){background:#EAF3DE}
  .ansoff-tag{font-size:10px;font-weight:800;letter-spacing:1px;text-transform:uppercase;margin-bottom:6px;color:var(--text-mid)}
  .ansoff-cell h4{font-size:14px;font-weight:700;color:var(--text-dark);margin-bottom:4px}
  .ansoff-cell p{font-size:12px;color:var(--text-mid)}

  /* TESTIMONIALS */
  .testi-bg{background:#E1F5EE}
  .testimonial-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px;max-width:960px;margin:0 auto}
  .testimonial-card{background:#fff;border-radius:14px;padding:22px;border:1px solid #9FE1CB;transition:.2s}
  .testimonial-card:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(0,0,0,.07)}
  .t-text{font-size:14px;color:var(--text-dark);font-style:italic;margin-bottom:16px;line-height:1.6}
  .t-author{display:flex;align-items:center;gap:10px}
  .t-avatar{width:38px;height:38px;border-radius:50%;background:var(--teal-light);color:var(--teal);display:flex;align-items:center;justify-content:center;font-weight:800;font-size:13px}
  .t-name{font-size:13px;font-weight:700}
  .t-role{font-size:11px;color:var(--text-light)}
  .stars{color:#EF9F27;font-size:15px;margin-bottom:10px}

  /* CONTACT */
  .contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:28px;max-width:860px;margin:0 auto}
  .contact-info h3{font-size:20px;font-weight:700;color:var(--green);margin-bottom:20px}
  .contact-item{display:flex;align-items:flex-start;gap:14px;margin-bottom:18px}
  .c-icon{width:40px;height:40px;background:var(--green-light);border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
  .c-text p{font-size:14px;font-weight:700;color:var(--text-dark)}
  .c-text span{font-size:12px;color:var(--text-mid)}
  .contact-form{background:#fff;border-radius:16px;border:1px solid #C0DD97;padding:28px;box-shadow:0 4px 16px rgba(0,0,0,.05)}
  .form-group{margin-bottom:16px}
  .form-group label{font-size:12px;font-weight:700;color:var(--text-mid);display:block;margin-bottom:6px;text-transform:uppercase;letter-spacing:.5px}
  .form-group input,.form-group textarea{width:100%;border:1.5px solid #D3D1C7;border-radius:10px;padding:10px 14px;font-size:14px;font-family:inherit;color:var(--text-dark);outline:none;transition:.2s;background:#FAFAF9}
  .form-group input:focus,.form-group textarea:focus{border-color:var(--green-mid);background:#fff}
  .form-group textarea{resize:vertical;min-height:90px}
  .form-submit{width:100%;background:var(--green);color:#fff;border:none;padding:13px;border-radius:10px;font-size:16px;font-weight:700;cursor:pointer;transition:.2s}
  .form-submit:hover{background:var(--teal);transform:translateY(-1px)}

  /* WARNING */
  .warning-section{background:#FAEEDA;padding:32px 24px}
  .warning-box{max-width:700px;margin:0 auto;text-align:center}
  .warning-box h3{font-size:16px;color:#854F0B;margin-bottom:8px;font-weight:700}
  .warning-box p{font-size:13px;color:#633806;line-height:1.7}

  /* FOOTER */
  footer{background:#173404;color:#C0DD97;padding:40px 24px;text-align:center}
  .f-logo{font-size:22px;font-weight:800;color:#fff;margin-bottom:6px}
  .f-tagline{font-size:13px;color:#97C459;margin-bottom:24px}
  .f-links{display:flex;gap:20px;justify-content:center;flex-wrap:wrap;margin-bottom:24px}
  .f-links a{color:#C0DD97;text-decoration:none;font-size:13px;transition:.2s}
  .f-links a:hover{color:#fff}
  .f-divider{width:60px;height:1px;background:#3B6D11;margin:0 auto 20px}
  .f-copy{font-size:12px;color:#3B6D11}

  /* RESPONSIVE */
  @media(max-width:700px){
    .nav-links{display:none}
    .hero h1{font-size:32px}
    .contact-grid{grid-template-columns:1fr}
    .ansoff-grid{grid-template-columns:1fr}
    .step-arrow{display:none}
    .hero-stats{gap:20px}
  }
</style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <div class="nav-logo">
    <div class="logo-icon">🌿</div>
    <div>
      <div class="logo-text">QuitGum Pakistan</div>
      <div class="logo-sub">Nicotine Gum — Quit Smoking</div>
    </div>
  </div>
  <ul class="nav-links">
    <li><a href="#features">Features</a></li>
    <li><a href="#how">How It Works</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#reviews">Reviews</a></li>
    <li><a href="#contact" class="nav-cta">Order Now</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-badge">🇵🇰 Available at CUSIT, Peshawar — Pakistan</div>
  <h1>Quit Smoking.<br><span>Start Living.</span></h1>
  <p class="hero-sub">Pakistan's nicotine gum that helps you break free from cigarette addiction. Safe, clinically proven, and easy to use — anytime, anywhere.</p>
  <div class="hero-btns">
    <a class="btn-primary" href="#pricing">Buy Now — Rs. 5,000</a>
    <a class="btn-secondary" href="#how">How Does It Work?</a>
  </div>
  <div class="hero-price">
    1 Box = <strong>Rs. 5,000</strong> &nbsp;|&nbsp; 7 Packs &nbsp;|&nbsp; Per Pack = Rs. 800
  </div>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num">7</div><div class="stat-label">Packs Per Box</div></div>
    <div class="stat"><div class="stat-num">Rs.80</div><div class="stat-label">Profit Per Pack</div></div>
    <div class="stat"><div class="stat-num">100%</div><div class="stat-label">Nicotine Replacement</div></div>
    <div class="stat"><div class="stat-num">0</div><div class="stat-label">Harmful Chemicals</div></div>
  </div>
</section>

<!-- FEATURES -->
<section class="section" id="features">
  <div class="section-title">
    <h2>Product Features</h2>
    <p>Everything you need to quit smoking for good</p>
    <div class="line"></div>
  </div>
  <div class="features-grid">
    <div class="feature-card">
      <div class="feature-icon">💊</div>
      <h3>Controlled Nicotine</h3>
      <p>Safe dose that reduces cravings without the harmful chemicals found in cigarettes</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">⚡</div>
      <h3>Instant Relief</h3>
      <p>Use the gum whenever a cigarette craving hits — fast-acting formula that works</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">👝</div>
      <h3>Portable & Easy</h3>
      <p>Compact size — carry it anywhere, use it anytime with no hassle or equipment</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">📉</div>
      <h3>Gradual Reduction</h3>
      <p>Slowly and safely reduces nicotine dependence over time at your own pace</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">❤️</div>
      <h3>Healthier Lifestyle</h3>
      <p>Your first real step toward a smoke-free, healthier life for you and your family</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">✅</div>
      <h3>Clinically Proven</h3>
      <p>Nicotine replacement therapy — a globally tested and trusted quit-smoking method</p>
    </div>
  </div>
</section>

<!-- HOW IT WORKS -->
<section class="section how-bg" id="how">
  <div class="section-title">
    <h2>How It Works</h2>
    <p>5 simple steps to becoming smoke-free</p>
    <div class="line"></div>
  </div>
  <div class="steps">
    <div class="step">
      <div class="step-num">1</div>
      <h3>Feel the Craving</h3>
      <p>When the urge to smoke hits, put down the cigarette</p>
    </div>
    <div class="step-arrow">➔</div>
    <div class="step">
      <div class="step-num">2</div>
      <h3>Chew the Gum</h3>
      <p>Chew QuitGum — nicotine is safely absorbed into your body</p>
    </div>
    <div class="step-arrow">➔</div>
    <div class="step">
      <div class="step-num">3</div>
      <h3>Craving Fades</h3>
      <p>Withdrawal symptoms like anxiety and irritability go away</p>
    </div>
    <div class="step-arrow">➔</div>
    <div class="step">
      <div class="step-num">4</div>
      <h3>Use Less Over Time</h3>
      <p>Reduce gum usage each week as cravings get weaker</p>
    </div>
    <div class="step-arrow">➔</div>
    <div class="step">
      <div class="step-num">5</div>
      <h3>Smoke-Free Life</h3>
      <p>Break free from cigarettes permanently — live healthy</p>
    </div>
  </div>
</section>

<!-- PRICING -->
<section class="section" id="pricing">
  <div class="section-title">
    <h2>Pricing</h2>
    <p>Affordable and accessible for everyone in Pakistan</p>
    <div class="line"></div>
  </div>
  <div class="pricing-card">
    <div class="pricing-head">
      <h3>QuitGum Starter Box</h3>
      <div class="price">Rs. 5,000</div>
      <div class="price-sub">1 Box — 7 Packs — Complete Treatment Pack</div>
    </div>
    <div class="pricing-body">
      <div class="pricing-row">
        <span class="label">📦 Box Contents</span>
        <span class="val">7 Packs</span>
      </div>
      <div class="pricing-row">
        <span class="label">🏷️ Per Pack Price</span>
        <span class="val">Rs. 800</span>
      </div>
      <div class="pricing-row">
        <span class="label">💰 Profit Margin (per pack)</span>
        <span class="val"><span class="profit-badge">+ Rs. 80 profit</span></span>
      </div>
      <div class="pricing-row">
        <span class="label">📍 Currently Available At</span>
        <span class="val">CUSIT, Peshawar</span>
      </div>
      <div class="pricing-row">
        <span class="label">🚀 Expanding Soon To</span>
        <span class="val">Pharmacies & Online</span>
      </div>
      <div style="margin-top:20px">
        <a class="btn-primary" href="#contact" style="width:100%;padding:14px;text-align:center;display:block;border-radius:10px;font-size:16px">Order Now — Contact Us 📩</a>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT / STP -->
<section class="section" id="about" style="background:#F8FBF6">
  <div class="section-title">
    <h2>Who Is This For?</h2>
    <p>Our target audience, market strategy, and positioning</p>
    <div class="line"></div>
  </div>
  <div class="stp-grid" style="margin-bottom:40px">
    <div class="stp-card">
      <div class="stp-label">🎯 Segmentation</div>
      <h3>Who We Serve</h3>
      <p>Smoking addicts, young adults, university students, and people who want to quit — especially in CUSIT and Peshawar</p>
    </div>
    <div class="stp-card">
      <div class="stp-label">📍 Targeting</div>
      <h3>Primary Target</h3>
      <p>Smokers who want to quit and young people at risk of addiction — primarily ages 18 to 35 in KPK</p>
    </div>
    <div class="stp-card">
      <div class="stp-label">💡 Positioning</div>
      <h3>Our Mission</h3>
      <p>A safer, healthier alternative to cigarettes — a supportive product that helps people quit addiction step by step</p>
    </div>
  </div>

  <div class="section-title" style="margin-top:48px;margin-bottom:28px">
    <h2>Growth Strategy</h2>
    <p>Ansoff Matrix — our roadmap for expansion</p>
    <div class="line"></div>
  </div>
  <div class="ansoff-grid">
    <div class="ansoff-cell">
      <div class="ansoff-tag">📈 Market Penetration</div>
      <h4>Grow in Current Market</h4>
      <p>Increase sales among existing smokers at CUSIT and Peshawar</p>
    </div>
    <div class="ansoff-cell">
      <div class="ansoff-tag">🧪 Product Development</div>
      <h4>New Product Variants</h4>
      <p>Introduce flavored nicotine gums to attract more users</p>
    </div>
    <div class="ansoff-cell">
      <div class="ansoff-tag">🗺️ Market Development</div>
      <h4>Enter New Markets</h4>
      <p>Expand to new cities, pharmacies, and online platforms across Pakistan</p>
    </div>
    <div class="ansoff-cell">
      <div class="ansoff-tag">🚀 Diversification</div>
      <h4>New Health Products</h4>
      <p>Develop other health-related products for a growing wellness brand</p>
    </div>
  </div>
</section>

<!-- REVIEWS -->
<section class="section testi-bg" id="reviews">
  <div class="section-title">
    <h2>Customer Reviews</h2>
    <p>What our users are saying about QuitGum</p>
    <div class="line"></div>
  </div>
  <div class="testimonial-grid">
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="t-text">"I had been smoking for 5 years. QuitGum helped me quit within 3 months. Highly recommend to everyone trying to stop!"</p>
      <div class="t-author">
        <div class="t-avatar">AK</div>
        <div>
          <div class="t-name">Ahmad Khan</div>
          <div class="t-role">CUSIT Student, Peshawar</div>
        </div>
      </div>
    </div>
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="t-text">"Very effective product. Whenever I felt a craving, I used the gum and instantly felt better. It really works!"</p>
      <div class="t-author">
        <div class="t-avatar">ZA</div>
        <div>
          <div class="t-name">Zubair Afridi</div>
          <div class="t-role">Working Professional, Peshawar</div>
        </div>
      </div>
    </div>
    <div class="testimonial-card">
      <div class="stars">★★★★☆</div>
      <p class="t-text">"Price seems a bit high but the quality and effect are excellent. Bought it for my family and everyone benefited from it."</p>
      <div class="t-author">
        <div class="t-avatar">SM</div>
        <div>
          <div class="t-name">Salman Mohmand</div>
          <div class="t-role">Teacher, Hayatabad</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- HEALTH WARNING -->
<div class="warning-section">
  <div class="warning-box">
    <div style="font-size:30px;margin-bottom:10px">⚠️</div>
    <h3>Health Awareness</h3>
    <p>Smoking causes lung cancer, heart disease, and serious health problems. QuitGum can help you quit — but always consult a doctor before starting any nicotine replacement treatment. Quitting smoking is essential for you and your family's long-term health.</p>
  </div>
</div>

<!-- CONTACT -->
<section class="section" id="contact">
  <div class="section-title">
    <h2>Contact & Order</h2>
    <p>Get in touch to place your order or ask any questions</p>
    <div class="line"></div>
  </div>
  <div class="contact-grid">
    <div class="contact-info">
      <h3>Get In Touch</h3>
      <div class="contact-item">
        <div class="c-icon">📍</div>
        <div class="c-text">
          <p>City University of Science & IT</p>
          <span>CUSIT, Peshawar, KPK, Pakistan</span>
        </div>
      </div>
      <div class="contact-item">
        <div class="c-icon">📱</div>
        <div class="c-text">
          <p>WhatsApp / Call</p>
          <span>+92 XXX XXXXXXX</span>
        </div>
      </div>
      <div class="contact-item">
        <div class="c-icon">📧</div>
        <div class="c-text">
          <p>Email</p>
          <span>quitgum.pk@gmail.com</span>
        </div>
      </div>
      <div class="contact-item">
        <div class="c-icon">📣</div>
        <div class="c-text">
          <p>Social Media</p>
          <span>#QuitSmoking &nbsp; #QuitGumPK</span>
        </div>
      </div>
      <div class="contact-item">
        <div class="c-icon">🕐</div>
        <div class="c-text">
          <p>Available Hours</p>
          <span>Mon – Sat, 9:00 AM – 6:00 PM</span>
        </div>
      </div>
    </div>
    <div class="contact-form">
      <div class="form-group">
        <label>Your Name</label>
        <input type="text" id="f-name" placeholder="e.g. Ali Hassan">
      </div>
      <div class="form-group">
        <label>Phone Number</label>
        <input type="tel" id="f-phone" placeholder="+92 300 0000000">
      </div>
      <div class="form-group">
        <label>Email (optional)</label>
        <input type="email" id="f-email" placeholder="your@email.com">
      </div>
      <div class="form-group">
        <label>Your Message or Order</label>
        <textarea id="f-msg" placeholder="e.g. I would like to order 2 boxes. Please contact me on WhatsApp."></textarea>
      </div>
      <button class="form-submit" onclick="submitForm()">Send Message 📩</button>
      <div id="form-success" style="display:none;margin-top:14px;background:#EAF3DE;color:#3B6D11;padding:12px;border-radius:8px;font-size:14px;font-weight:600;text-align:center">
        ✅ Thank you! We will contact you shortly.
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="f-logo">🌿 QuitGum Pakistan</div>
  <div class="f-tagline">A Healthier Pakistan — One Gum at a Time</div>
  <div class="f-links">
    <a href="#features">Features</a>
    <a href="#how">How It Works</a>
    <a href="#pricing">Pricing</a>
    <a href="#about">About</a>
    <a href="#reviews">Reviews</a>
    <a href="#contact">Contact</a>
  </div>
  <div class="f-divider"></div>
  <div class="f-copy">© 2025 QuitGum Pakistan — CUSIT Peshawar | MVP Product &nbsp;|&nbsp; All Rights Reserved</div>
</footer>

<script>
  function submitForm(){
    var name=document.getElementById('f-name').value.trim();
    var phone=document.getElementById('f-phone').value.trim();
    var msg=document.getElementById('f-msg').value.trim();
    if(!name||!phone||!msg){
      alert('Please fill in your Name, Phone Number, and Message.');
      return;
    }
    document.getElementById('form-success').style.display='block';
    document.getElementById('f-name').value='';
    document.getElementById('f-phone').value='';
    document.getElementById('f-email').value='';
    document.getElementById('f-msg').value='';
    setTimeout(function(){document.getElementById('form-success').style.display='none';},5000);
  }

  // Smooth nav highlight on scroll
  window.addEventListener('scroll',function(){
    var sections=document.querySelectorAll('section[id]');
    var links=document.querySelectorAll('.nav-links a');
    var scrollY=window.scrollY+80;
    sections.forEach(function(sec){
      if(scrollY>=sec.offsetTop && scrollY<sec.offsetTop+sec.offsetHeight){
        links.forEach(function(l){l.style.color='';l.style.background='';});
        var active=document.querySelector('.nav-links a[href="#'+sec.id+'"]');
        if(active&&!active.classList.contains('nav-cta')){
          active.style.color='var(--green)';
          active.style.background='var(--green-light)';
        }
      }
    });
  });
</script>
</body>
</html>
