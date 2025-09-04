# fabicoo
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fabico fashion</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  /* Global Styles */
  * {margin:0; padding:0; box-sizing:border-box; font-family:'Poppins', sans-serif;}
  body {scroll-behavior:smooth; background:#f0f4f8; color:#333;}
  a {text-decoration:none; color:inherit;}
  section {padding:100px 20px; max-width:1200px; margin:0 auto;}
  .section-title {text-align:center; margin-bottom:50px; font-size:2.2rem; font-weight:700; color:#FF6B81;}

  /* Header */
  header {
    position:fixed; top:0; width:100%; z-index:1000;
    background:#ffffff; padding:20px 60px; display:flex; justify-content:space-between; align-items:center;
    box-shadow:0 4px 20px rgba(0,0,0,0.1);
    transition:0.3s;
  }
  header h1 {color:#FF6B6B; font-weight:700; font-size:1.8rem;}
  nav a {margin-left:25px; font-weight:500; color:#555; transition:0.3s;}
  nav a:hover {color:#1DD1A1;}

  /* Hero with animated gradient */
  .hero {
    height:100vh; display:flex; flex-direction:column; justify-content:center; align-items:center;
    text-align:center; color:#fff; overflow:hidden; position:relative;
    background: linear-gradient(-45deg, #70A1FF, #FF9FF3, #54a0ff, #ff6b81);
    background-size: 400% 400%;
    animation:gradientBG 15s ease infinite;
  }
  @keyframes gradientBG {
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
  }
  .hero h2 {font-size:3rem; margin-bottom:20px; animation:fadeIn 2s;}
  .hero p {font-size:1.2rem; margin-bottom:30px; max-width:600px; animation:fadeIn 2.5s;}
  .hero a {
    background:#FF6B6B; color:#fff; padding:15px 50px; border-radius:50px; font-weight:bold;
    transition:0.3s; animation:fadeIn 3s;
  }
  .hero a:hover {background:#1DD1A1; transform:scale(1.1);}

  @keyframes fadeIn {0%{opacity:0; transform:translateY(20px);}100%{opacity:1; transform:translateY(0);}}

  /* Luxury Cards */
  .luxury-card {
    background:#ffffff; border-radius:25px; padding:60px 40px;
    box-shadow:0 15px 35px rgba(0,0,0,0.1); margin-bottom:60px;
    transition:transform 0.3s, box-shadow 0.3s;
    opacity:0; transform:translateY(50px);
  }
  .luxury-card.visible {opacity:1; transform:translateY(0); transition:all 1s;}
  .luxury-card:hover {transform:translateY(-10px); box-shadow:0 20px 45px rgba(0,0,0,0.15);}

  /* Services */
  .services-cards {display:flex; flex-wrap:wrap; gap:30px; justify-content:center;}
  .service-card {
    flex:1 1 250px; text-align:center; padding:30px; border-radius:25px;
    background:linear-gradient(135deg, #ffeaa7, #fab1a0);
    box-shadow:0 10px 30px rgba(0,0,0,0.1);
    transition:transform 0.3s, box-shadow 0.3s;
    opacity:0; transform:translateY(50px);
  }
  .service-card.visible {opacity:1; transform:translateY(0); transition:all 1s;}
  .service-card:hover {transform:translateY(-10px); box-shadow:0 15px 35px rgba(0,0,0,0.2);}
  .service-card i {font-size:2.5rem; color:#6c5ce7; margin-bottom:20px;}

  /* Testimonials */
  .testimonials-slider {display:flex; overflow-x:auto; gap:30px; scroll-behavior:smooth; padding-bottom:20px;}
  .testimonial-card {
    min-width:300px; background:#dff9fb; color:#130f40; padding:30px; border-radius:25px;
    flex-shrink:0; box-shadow:0 10px 30px rgba(0,0,0,0.1); transition:transform 0.3s; opacity:0; transform:translateY(50px);
  }
  .testimonial-card.visible {opacity:1; transform:translateY(0); transition:all 1s;}
  .testimonial-card:hover {transform:translateY(-5px);}
  .testimonial-card p {font-style:italic; margin-bottom:15px;}

  /* Contact */
  .contact-info {display:flex; flex-direction:column; gap:20px; align-items:center; padding:50px 0;}
  .contact-info div {
    background:#f1f2f6; padding:25px 40px; border-radius:25px;
    box-shadow:0 10px 30px rgba(0,0,0,0.1); width:100%; max-width:500px;
    text-align:center; transition:transform 0.3s, box-shadow 0.3s; opacity:0; transform:translateY(50px);
  }
  .contact-info div.visible {opacity:1; transform:translateY(0); transition:all 1s;}
  .contact-info div:hover {transform:translateY(-5px); box-shadow:0 12px 35px rgba(0,0,0,0.15);}
  .contact-info i {color:#54a0ff; margin-bottom:10px; font-size:1.5rem;}

  /* Footer */
  footer {background:#ffffff; color:#333; text-align:center; padding:40px; box-shadow:0 -2px 8px rgba(0,0,0,0.05);}
  footer a {color:#FF6B6B; margin:0 15px; font-size:1.3rem; transition:0.3s;}
  footer a:hover {color:#1dd1a1; transform:scale(1.1);}

  @media(max-width:768px){.services-cards{flex-direction:column; align-items:center;} header{flex-direction:column;} nav{margin-top:10px;}}
</style>
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>

<header>
  <h1>Fabico</h1>
  <nav>
    
    <a href="#goal">Our Goal</a>
    <a href="#services">Services</a>
    <a href="#testimonials">Testimonials</a>
    
    <a href="#about">About Us</a>
  </nav>
</header>

<section class="hero">
  <div class="hero-content">
    <h2>Welcome to Fabico Fashion</h2>
    <p>We provide the best product and service.</p>
    <a href="#contact">Contact with us</a>
  </div>
</section>


<section id="services">
  <h2 class="section-title">Our Services</h2>
  <div class="services-cards">
    <div class="service-card"><i class="fas fa-laptop-code"></i><h3>Wholesale</h3><p>We sell wholesale clothing nationwide. We have more than 20 clothing items. You can also purchase products wholesale online.</p></div>
    <div class="service-card"><i class="fas fa-bullhorn"></i><h3>Business with us</h3><p>Anyone who wants to do business with us can open a showroom. For this, please contact the number given below.</p></div>
    <div class="service-card"><i class="fas fa-mobile-alt"></i><h3>Fabico Store</h3><p>Expand your business online as well as offline or join as a proud reseller or seller of Fabico Store. To join as a seller or reseller of Fabico Store, contact us at the number given below.</p></div>
  </div>
</section>



<section id="mission" class="luxury-card">
  <h2 class="section-title">Managing Director of the company</h2>
  <p>⭐⭐Assalamu Alaikum and a very warm welcome to all of you,

It is both an honor and a privilege to stand before you today as the Managing Director of Fabico Fashion. Our journey began with a simple yet powerful vision—to redefine fashion with elegance, quality, and creativity. Today, Fabico Fashion is more than a brand; it is a name that reflects style, trust, and excellence.

At Fabico Fashion, our mission is clear:

To deliver premium-quality fashion that blends comfort, sophistication, and individuality.

To ensure every customer feels confident, unique, and inspired when they choose Fabico.

To make fashion not just a product, but an experience.

Our goals are driven by passion and ambition:

We aim to become a global name in the fashion industry, representing both modern trends and timeless elegance.

We want to create opportunities, empower our team, and build long-lasting relationships with our valued clients.

Most importantly, we want to contribute positively to the community by promoting ethical practices and sustainable fashion.

As for our services, Fabico Fashion proudly offers:

Exclusive clothing collections for men, women, and youth.

Stylish accessories designed to complement modern lifestyles.

Personalized fashion solutions tailored to meet the unique needs of our customers.

In every step we take, we promise innovation, quality, and integrity. Our customers are not just buyers—they are part of the Fabico Fashion family. Together, we are not only creating fashion; we are creating confidence, pride, and a lasting legacy.

Thank you for believing in us, for walking this journey with us, and for making Fabico Fashion a brand of trust and elegance. The best is yet to come, InshaAllah..</p>
</section>

<section id="goal" class="luxury-card">
  <h2 class="section-title">Our Goal</h2>
  <p>⭐⭐At Fabico Fashion, our primary goal is to build a brand that reflects luxury, trust, and timeless elegance. We are not just creating clothes; we are shaping lifestyles and inspiring confidence in everyone who wears Fabico.

Our goals are clear and ambitious:

Global Recognition – We aim to position Fabico Fashion as a world-class brand that represents modern creativity with a touch of tradition.

Customer Excellence – Our goal is to exceed expectations by offering products and services that provide true value and unmatched quality.

Innovation & Sustainability – We strive to innovate in design, while also promoting sustainable practices that protect our future generations.

Community & Empowerment – We want to empower people, create opportunities, and contribute positively to society through ethical business practices.

Long-Term Growth – Our vision is to expand our reach, not just in Bangladesh, but across international markets, making Fabico Fashion a name of pride worldwide.

These goals are not just written words—they are promises. Promises to our customers, to our partners, and to ourselves. With the dedication of our team, the trust of our clients, and the blessings of the Almighty, I am confident we will achieve them, InshaAllah..</p>
</section>

<section id="testimonials" class="luxury-card">
  <h2 class="section-title">Testimonials</h2>
  
<div   
 <div class="testimonial-card"><p>⭐⭐⭐⭐⭐
“Fabico Fashion has completely changed the way I see style. Every piece feels luxurious, elegant, and unique. I receive compliments every time I wear their collection.” "</p><strong>-— Ayesha Rahman, Dhaka</strong></div>

 <div class="testimonial-card"><p>⭐⭐⭐⭐⭐“The quality of Fabico Fashion is unmatched. From fabric to finishing, everything speaks of perfection. Truly a brand that values its customers.” "</p><strong>*— Shahidul Islam, Chittagong</strong></div>

 <div class="testimonial-card"><p>⭐⭐⭐⭐⭐“I love how Fabico combines modern trends with timeless elegance. Their designs make me feel confident and stylish in every occasion.” "</p><strong>*— Nusrat Jahan, Sylhet</strong></div>

 <div class="testimonial-card"><p>⭐⭐⭐⭐⭐“What I admire about Fabico Fashion is not just the clothing but the whole experience. Professional service, premium quality, and always on time. Highly recommended!” "</p><strong>*— Arif Khan, London</strong></div>

 <div class="testimonial-card"><p>⭐⭐⭐⭐⭐ “Fabico Fashion isn’t just a brand, it’s an emotion. Every collection feels special, and the detailing shows how much passion goes into their work.”"</p><strong>*Riyadul Islam ,Rajshahi</strong></div>
    
</section>

<section id="about" class="luxury-card">
  <h2 class="section-title">About Us</h2>
  <p> *-->*At Fabico Fashion, we believe that style is more than just clothing—it’s a statement of individuality, confidence, and creativity. Since our inception, we have been dedicated to bringing high-quality, trendy, and affordable fashion to our valued customers.

Our mission is simple: to help people express themselves through fashion. Whether it’s everyday wear, special occasions, or seasonal collections, Fabico Fashion focuses on combining comfort, style, and innovation in every piece we create.

We pride ourselves on staying ahead of the latest fashion trends while maintaining a strong commitment to quality and customer satisfaction. Every garment and accessory we offer is carefully curated to meet the diverse tastes and preferences of our growing clientele.

At Fabico Fashion, our core values are creativity, integrity, and excellence. We are passionate about making fashion accessible to everyone, empowering our customers to feel confident and stylish every day.

Join us on our journey as we continue to redefine modern fashion and create a community where style meets individuality. Fabico Fashion – Designed for You.</p>
</section>


<section id="contact">
  <h2 class="section-title">Contact Us</h2>
  <div class="contact-info">
    <div><i class="fas fa-phone-alt"></i><p><strong>Phone:</strong> +8801836-500191 </p></div>
    <div><i class="fas fa-envelope"></i><p><strong>Email:</strong> info.fabico@gmail.com </p></div>

   <div><i class="fas fa-map-marker-alt"></i><p><strong>Address:</strong> Uttora,359 no building,Dhaka, Bangladesh </p></div>
  </div>


<footer>
  <p>Follow Us
  <div>

<a href="https://www.facebook.com/fabicogroup">Facebook</a>
<a href="https://www.youtube.com/@EverHigh-k4r">Youtube</a>


<footer>
  <p>Our Online Retail Store
  <div>
<a href="https://fabico.sellbd.shop/">Fabico store</a>

  </div>
</footer>

<footer>
  <p>&copy; 2025 fabico Ltd. All Rights Reserved.</p>
  <div>


<script>
  // Scroll animation for sections
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        entry.target.classList.add('visible');
      }
    });
  }, {threshold: 0.2});

  document.querySelectorAll('.luxury-card, .service-card, .testimonial-card, .contact-info div').forEach(el => observer.observe(el));
</script>

</body>
</html>
