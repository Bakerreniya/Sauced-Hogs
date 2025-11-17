<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sauced Hogs • Firehouse BBQ</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Roboto+Condensed:wght@300;400;700&display=swap');

    body {
      margin: 0;
      background: #1a0f0a;
      color: #f7e9db;
      font-family: 'Roboto Condensed', sans-serif;
    }

    /* HEADER */
    header {
      width: 100%;
      height: 320px;
      background-image: url('https://raw.githubusercontent.com/Bakerreniya/Sauced-Hogs/7645ea3afe6ac7f011dad032b15680985996c8c5/IMG_6762.jpeg');
      background-size: cover;
      background-position: center;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.6);
    }
    header h1 {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 4rem;
      color: #fff3d9;
      letter-spacing: 3px;
      text-shadow: 0 0 18px rgba(255, 80, 0, 0.9);
      background: rgba(0,0,0,0.45);
      padding: 10px 25px;
      border-radius: 10px;
      border: 2px solid rgba(255, 110, 40, 0.8);
    }

    /* NAV BAR */
    nav {
      width: 100%;
      background: #2b120b;
      display: flex;
      justify-content: center;
      gap: 40px;
      padding: 12px;
      border-bottom: 2px solid #ff7b32;
    }
    nav a {
      color: #ffd8b3;
      text-decoration: none;
      font-family: 'Anton';
      letter-spacing: 2px;
      font-size: 1.1rem;
      transition: 0.3s;
    }
    nav a:hover {
      color: #ff8a3c;
    }

    /* SECTION */
    section {
      max-width: 1150px;
      margin: auto;
      margin-top: 40px;
      padding: 25px;
      background: #2e1a14;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.4);
      border: 1px solid #ff7b32;
    }
    h2 {
      font-family: 'Bebas Neue', sans-serif;
      letter-spacing: 2px;
      font-size: 2.2rem;
      color: #ffb37a;
      text-shadow: 0 0 8px rgba(255,70,20,0.7);
      margin-bottom: 10px;
    }

    /* GALLERY */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 15px;
      margin-top: 20px;
    }
    .gallery img {
      width: 100%;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.5);
      transition: 0.3s;
    }
    .gallery img:hover {
      transform: scale(1.03);
    }

    /* INTERACTIVE BUTTON */
    .btn {
      display: inline-block;
      margin-top: 15px;
      padding: 12px 22px;
      border-radius: 8px;
      background: linear-gradient(90deg, #ff5e00, #ff9a3c);
      color: #1a0f0a;
      text-decoration: none;
      font-family: 'Anton';
      letter-spacing: 2px;
      font-size: 1rem;
      transition: 0.3s;
    }
    .btn:hover {
      filter: brightness(1.15);
    }

    /* MENU IMG */
    .menu-img img {
      width: 100%;
      margin-top: 15px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.6);
    }

    footer {
      text-align: center;
      color: #fcd9bd;
      padding: 30px;
      margin-top: 40px;
      background: #2b120b;
      border-top: 2px solid #ff7b32;
    }
  </style>
<script>
// 🔥 Interactive Hover Fire Glow on Images
function addFireGlow() {
  document.querySelectorAll('.gallery img').forEach(img => {
    img.addEventListener('mouseenter', () => {
      img.style.filter = 'brightness(1.3) drop-shadow(0 0 20px #ff4500)';
    });
    img.addEventListener('mouseleave', () => {
      img.style.filter = 'brightness(1) drop-shadow(0 0 0px black)';
    });
  });
}

// 🔥 Click to Ignite Button Effect
function igniteButtons() {
  document.querySelectorAll('.btn').forEach(btn => {
    btn.addEventListener('click', () => {
      btn.style.transform = 'scale(0.95)';
      btn.style.boxShadow = '0 0 20px #ff3c00';
      setTimeout(() => {
        btn.style.transform = 'scale(1)';
        btn.style.boxShadow = 'none';
      }, 200);
    });
  });
}

// 🔥 Flickering Header Fire Animation
function flickerHeader() {
  const header = document.querySelector('header h1');
  setInterval(() => {
    header.style.textShadow = `0 0 ${Math.random()*20}px rgba(255,70,0,${Math.random()})`;
  }, 120);
}

// 🔥 Smooth Scroll for Nav Bar
function smoothScroll() {
  document.querySelectorAll('nav a').forEach(link => {
    link.addEventListener('click', (e) => {
      e.preventDefault();
      const target = document.querySelector(e.target.getAttribute('href'));
      target.scrollIntoView({ behavior: 'smooth' });
    });
  });
}

// Initialize all interactions
window.onload = () => {
  addFireGlow();
  igniteButtons();
  flickerHeader();
  smoothScroll();
};
</script>
</head>
<body style="background:#120905 url('https://i.imgur.com/d9uo7j0.jpeg') no-repeat center top / cover; background-attachment: fixed;">

<header>
  <h1>Sauced Hogs</h1>
</header>

<nav>
  <a href="#about">ABOUT</a>
  <a href="#vibe">THE GRILL VIBE</a>
  <a href="#menu">MENU</a>
  <a href="#contact">CONTACT</a>
</nav>

<section id="about" style="cursor:pointer;" onclick="alert('🔥 Welcome to Sauced Hogs! Where the grill is always hot! 🔥')">
  <h2>About Us</h2>
  <p>Sauced Hogs isn’t just a BBQ joint — it’s a whole atmosphere. The smell of smoky ribs hits before you even walk in. The grill marks run deep. This place brings the heat like a firehouse cookout mixed with a biker bar and a backyard smoke session. Nothing fancy. Nothing fake. Just real food made over real fire.</p>
  <p>We’re located in Hernando, Florida, serving up the perfect mix of comfort, chaos, and char. Locals know our pitmasters don’t play — every plate comes out sizzling like it survived a battle with the flames.</p>
  <p><strong>Address:</strong> 2408 N Fatima Ave, Hernando, Florida</p>
  <p><strong>Phone:</strong> (352) 419-8990</p>
  <p><strong>Email:</strong> sauced.hogs@yahoo.com</p>
  <a class="btn" href="https://www.facebook.com/sauced.hogs" target="_blank">VISIT OUR FACEBOOK</a>
</section>

<section id="vibe">
  <h2>The Grill House Vibe</h2>
  <p>Imagine this: flames rising, metal grates glowing red, smoke drifting like it has a personality, and the sound of meat hitting the grill. That’s Sauced Hogs. The whole restaurant gives off a firehouse energy — bold, loud, and blazing with flavor.</p>
  <p>Walk in and you’ll feel the heat — literally. Our grill masters stay locked in, flipping ribs, pulling pork, and watching flames dance across a steel grate like a fire pit at a weekend cookout. The walls are decorated with rustic wood, glowing signs, flame accents, and that classic smoky atmosphere.</p>
  <p>Every Thursday, karaoke brings chaos and fun. People start singing like they’ve never touched a mic before. It’s loud. It’s messy. It’s hilarious. And it’s peak Sauced Hogs energy.</p>

  <div class="gallery">
    <img src="https://raw.githubusercontent.com/Bakerreniya/Sauced-Hogs/7645ea3afe6ac7f011dad032b15680985996c8c5/IMG_6764.jpeg" />
    <img src="https://raw.githubusercontent.com/Bakerreniya/Sauced-Hogs/7645ea3afe6ac7f011dad032b15680985996c8c5/IMG_6765.jpeg" />
  </div>
</section>

<section id="menu" class="menu-img">
  <h2>Menu Snapshot</h2>
  <p>If fire had a flavor — this would be it. Everything on this menu is built different. Charred, smoky, seasoned, and slapped straight from the flames to your plate. The portions? Huge. The flavor? Dangerous.</p>
  <p>Even our plates look like they came out of a smokehouse challenge. We don’t do small bites here. We do fire-grilled feasts.</p>
  <img src="https://raw.githubusercontent.com/Bakerreniya/Sauced-Hogs/7645ea3afe6ac7f011dad032b15680985996c8c5/IMG_6766.jpeg" />
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <p>Hungry? Curious? Ready to meet the grill? Pull up, call in, or hit us on Facebook. We’re always cooking, always flaming, always serving.</p>
  <a class="btn" href="https://www.facebook.com/sauced.hogs" target="_blank">FACEBOOK PAGE</a>
</section>

<footer>
  © 2025 Sauced Hogs • Firehouse BBQ Website Edition
</footer>

</body>
</html>
