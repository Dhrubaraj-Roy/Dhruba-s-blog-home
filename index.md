---
layout: default
title: Home
---

<div class="blog-container">
  <header class="site-header">
    <div class="logo-container">
      <img src="/skills-github-pages/assets/logo.png" alt="Dhruba's Blog Logo" class="site-logo">
    </div>
    <div class="glitch-container">
      <h1 class="glitch" data-text="DHRUBA'S LOG">DHRUBA'S LOG</h1>
    </div>
    <p class="site-description">Exploring code, life, and everything in between</p>
  </header>

  <div class="posts-container">
    <div class="section-header">
      <div class="header-line"></div>
      <h2>LATEST ENTRIES</h2>
      <div class="header-line"></div>
    </div>
    
    <ul class="posts-list">
      {% for post in site.posts %}
        <li class="post-item">
          <span class="post-date">{{ post.date | date: "%d/%m/%Y" }}</span>
          <a href="{{ site.baseurl }}{{ post.url }}" class="post-link">
            <span class="post-title">{{ post.title }}</span>
            <span class="arrow">→</span>
          </a>
        </li>
      {% endfor %}
    </ul>
  </div>

  <div class="subscription-container">
    <div class="section-header">
      <div class="header-line"></div>
      <h2>JOIN THE LIST</h2>
      <div class="header-line"></div>
    </div>
    
    <div class="subscription-box">
      <p>Get notified when new thoughts are published. No spam.</p>
      
      <!-- MailerLite Form -->
      <div class="ml-embedded" data-form="EyeZih"></div>
    </div>
  </div>

  <footer class="site-footer">
    <p>&copy; 2025 Dhruba's Log | Built with <span class="heart">♥</span> on GitHub Pages</p>
  </footer>
</div>

<!-- MailerLite Universal -->
<script>
    (function(w,d,e,u,f,l,n){w[f]=w[f]||function(){(w[f].q=w[f].q||[])
    .push(arguments);},l=d.createElement(e),l.async=1,l.src=u,
    n=d.getElementsByTagName(e)[0],n.parentNode.insertBefore(l,n);})
    (window,document,'script','https://assets.mailerlite.com/js/universal.js','ml');
    ml('account', '1463895');
</script>
<!-- End MailerLite Universal -->

<style>
  /* Header styles with glitch effect */
  .site-header {
    text-align: center;
    margin-bottom: 3rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #333;
  }

  /* ADD THESE STYLES RIGHT HERE */
  .logo-container {
    text-align: center;
    margin-bottom: 1rem;
  }
  
  .site-logo {
    max-width: 120px;
    height: auto;
    filter: drop-shadow(0 0 5px rgba(0, 255, 0, 0.3));
  }
  /* END OF ADDED STYLES */

  .glitch-container {
    margin-bottom: 0.5rem;
  }
  
  /* Base styles */
  body {
    background-color: #0d0d0d;
    color: #d9d9d9;
    font-family: 'Courier New', monospace;
    margin: 0;
    padding: 0;
    line-height: 1.6;
  }

  .blog-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
  }

  /* Header styles with glitch effect */
  .site-header {
    text-align: center;
    margin-bottom: 3rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #333;
  }

  .glitch-container {
    margin-bottom: 0.5rem;
  }

  .glitch {
    font-size: 3rem;
    font-weight: bold;
    text-transform: uppercase;
    position: relative;
    color: #0f0;
    letter-spacing: 0.1em;
    margin: 0;
    animation: glitch 2s infinite;
  }

  .glitch::before,
  .glitch::after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  .glitch::before {
    left: 2px;
    text-shadow: -2px 0 #ff00c1;
    clip: rect(44px, 450px, 56px, 0);
    animation: glitch-anim 5s infinite linear alternate-reverse;
  }

  .glitch::after {
    left: -2px;
    text-shadow: -2px 0 #00fff9, 2px 2px #ff00c1;
    animation: glitch-anim2 1s infinite linear alternate-reverse;
  }

  .site-description {
    color: #999;
    font-size: 1.1rem;
    margin-top: 0.5rem;
  }

  /* Section headers */
  .section-header {
    display: flex;
    align-items: center;
    margin: 2rem 0;
  }

  .section-header h2 {
    margin: 0 1rem;
    font-size: 1.5rem;
    color: #0f0;
    letter-spacing: 0.1em;
    white-space: nowrap;
  }

  .header-line {
    height: 1px;
    flex-grow: 1;
    background: linear-gradient(to right, transparent, #0f0, transparent);
  }

  /* Posts list */
  .posts-list {
    list-style: none;
    padding: 0;
  }

  .post-item {
    margin-bottom: 1.5rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid #222;
    display: flex;
    align-items: center;
    transition: transform 0.3s ease;
  }

  .post-item:hover {
    transform: translateX(10px);
  }

  .post-date {
    background-color: #222;
    color: #0f0;
    padding: 0.3rem 0.7rem;
    border-radius: 3px;
    font-size: 0.9rem;
    margin-right: 1rem;
    font-family: monospace;
  }

  .post-link {
    color: #d9d9d9;
    text-decoration: none;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-grow: 1;
    padding: 0.5rem 0;
  }

  .post-title {
    font-weight: bold;
    font-size: 1.1rem;
  }

  .arrow {
    color: #0f0;
    font-weight: bold;
    opacity: 0;
    transition: opacity 0.3s ease, transform 0.3s ease;
    transform: translateX(-10px);
  }

  .post-item:hover .arrow {
    opacity: 1;
    transform: translateX(0);
  }

  /* Subscription box */
  .subscription-container {
    margin-top: 4rem;
  }

  .subscription-box {
    background: linear-gradient(145deg, #1a1a1a, #0d0d0d);
    border: 1px solid #333;
    border-radius: 5px;
    padding: 2rem;
    box-shadow: 0 0 20px rgba(0, 255, 0, 0.1);
  }

  .subscription-box p {
    margin-top: 0;
    margin-bottom: 1.5rem;
    color: #bbb;
  }

  /* MailerLite Form Styling */
  .ml-embedded form {
    background: transparent !important;
    border: none !important;
  }

  .ml-embedded input[type="email"] {
    background: #1a1a1a !important;
    border: 1px solid #333 !important;
    color: #fff !important;
    font-family: 'Courier New', monospace !important;
    padding: 10px 15px !important;
    width: 100% !important;
    margin-bottom: 10px !important;
  }

  .ml-embedded button[type="submit"] {
    background: #0f0 !important;
    color: #000 !important;
    border: none !important;
    padding: 10px 20px !important;
    font-family: 'Courier New', monospace !important;
    font-weight: bold !important;
    cursor: pointer !important;
    transition: background-color 0.3s !important;
  }

  .ml-embedded button[type="submit"]:hover {
    background: #00cc00 !important;
  }

  /* Footer */
  .site-footer {
    margin-top: 4rem;
    padding-top: 2rem;
    text-align: center;
    color: #666;
    font-size: 0.9rem;
    border-top: 1px solid #222;
  }

  .heart {
    color: #ff0066;
    display: inline-block;
    animation: heartbeat 1.5s infinite;
  }

  /* Animations */
  @keyframes glitch-anim {
    0% {
      clip: rect(5px, 9999px, 75px, 0);
    }
    5% {
      clip: rect(79px, 9999px, 13px, 0);
    }
    10% {
      clip: rect(32px, 9999px, 92px, 0);
    }
    15% {
      clip: rect(25px, 9999px, 5px, 0);
    }
    20% {
      clip: rect(88px, 9999px, 37px, 0);
    }
    25% {
      clip: rect(13px, 9999px, 80px, 0);
    }
    30% {
      clip: rect(41px, 9999px, 91px, 0);
    }
    /* ...more randomness... */
    100% {
      clip: rect(67px, 9999px, 51px, 0);
    }
  }

  @keyframes glitch-anim2 {
    0% {
      clip: rect(65px, 9999px, 30px, 0);
    }
    5% {
      clip: rect(5px, 9999px, 91px, 0);
    }
    10% {
      clip: rect(63px, 9999px, 30px, 0);
    }
    15% {
      clip: rect(84px, 9999px, 45px, 0);
    }
    /* ...more randomness... */
    100% {
      clip: rect(46px, 9999px, 33px, 0);
    }
  }

  @keyframes heartbeat {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.2); }
  }

  /* Mobile responsiveness */
  @media (max-width: 600px) {
    .blog-container {
      padding: 1rem;
    }
    
    .glitch {
      font-size: 2rem;
    }
    
    .section-header h2 {
      font-size: 1.2rem;
    }
    
    .post-item {
      flex-direction: column;
      align-items: flex-start;
    }
    
    .post-date {
      margin-bottom: 0.5rem;
    }
  }
</style>
