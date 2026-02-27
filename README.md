<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Luxury Beauty Salon offering premium hair, skin and spa services. Book your appointment today.">
<title>Luxury Beauty Salon</title>

<style>
/* =====================
   RESET
===================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: "Segoe UI", sans-serif;
  background: #000;
  color: #fff;
  line-height: 1.6;
}

/* =====================
   VARIABLES
===================== */
:root {
  --gold: #d4af37;
  --dark: #000;
  --soft-dark: #111;
}

/* =====================
   GLOBAL
===================== */
.container {
  width: 90%;
  max-width: 1200px;
  margin: auto;
}

section {
  padding: 80px 0;
}

h1, h2, h3 {
  color: var(--gold);
  margin-bottom: 20px;
}

p {
  margin-bottom: 15px;
}

.btn {
  display: inline-block;
  padding: 12px 25px;
  background: var(--gold);
  color: #000;
  border-radius: 30px;
  text-decoration: none;
  font-weight: bold;
  transition: 0.3s ease;
}

.btn:hover {
  background: #fff;
}

/* =====================
   NAVIGATION
===================== */
header {
  background: #000;
  border-bottom: 1px solid var(--gold);
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

.nav ul {
  display: flex;
  list-style: none;
  gap: 20px;
}

.nav a {
  color: var(--gold);
  text-decoration: none;
  font-weight: 500;
}

.nav a:hover {
  color: #fff;
}

/* =====================
   HERO
===================== */
.hero {
  height: 90vh;
  display: flex;
  align-items: center;
  text-align: center;
  background: linear-gradient(rgba(0,0,0,0.85), rgba(0,0,0,0.85));
}

.hero-content {
  width: 100%;
  animation: fadeIn 1.5s ease;
}

@keyframes fadeIn {
  from {opacity: 0; transform: translateY(30px);}
  to {opacity: 1; transform: translateY(0);}
}

/* =====================
   SERVICES
===================== */
.services-grid {
  display: grid;
  gap: 30px;
}

.service-card {
  background: var(--soft-dark);
  padding: 30px;
  border-radius: 10px;
  border: 1px solid var(--gold);
  transition: 0.3s ease;
}

.service-card:hover {
  transform: translateY(-5px);
}

/* =====================
   TESTIMONIALS
===================== */
.testimonial {
  background: var(--soft-dark);
  padding: 30px;
  border-left: 5px solid var(--gold);
  margin-bottom: 20px;
}

/* =====================
   FORM
===================== */
form {
  display: grid;
  gap: 20px;
}

input, textarea {
  padding: 12px;
  border: 1px solid var(--gold);
  background: #000;
  color: #fff;
  border-radius: 5px;
}

input:focus, textarea:focus {
  outline: none;
  border-color: #fff;
}

.error {
  color: red;
  font-size: 14px;
}

/* =====================
   FOOTER
===================== */
footer {
  background: #000;
  border-top: 1px solid var(--gold);
  text-align: center;
  padding: 20px 0;
  color: var(--gold);
}

/* =====================
   RESPONSIVE
===================== */
@media (min-width: 768px) {
  .services-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
</head>

<body>

<header>
  <div class="container nav">
    <h2>Beauty Salon</h2>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#booking">Booking</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<section class="hero" id="home">
  <div class="container hero-content">
    <h1>Luxury Beauty Experience</h1>
    <p>Premium hair, skin & spa treatments tailored for elegance.</p>
    <a href="#booking" class="btn">Book Appointment</a>
  </div>
</section>

<section id="services">
  <div class="container">
    <h2>Our Services</h2>
    <div class="services-grid">
      <div class="service-card">
        <h3>Hair Styling</h3>
        <p>Professional cuts, coloring and styling.</p>
      </div>
      <div class="service-card">
        <h3>Facial Treatments</h3>
        <p>Luxury skin care and rejuvenation.</p>
      </div>
      <div class="service-card">
        <h3>Bridal Packages</h3>
        <p>Exclusive bridal beauty experiences.</p>
      </div>
    </div>
  </div>
</section>

<section id="booking">
  <div class="container">
    <h2>Book Appointment</h2>
    <form id="bookingForm" novalidate>
      <input type="text" id="name" placeholder="Full Name" required>
      <input type="email" id="email" placeholder="Email Address" required>
      <input type="date" id="date" required>
      <textarea id="message" placeholder="Additional Notes"></textarea>
      <button type="submit" class="btn">Submit</button>
      <div id="formMessage"></div>
    </form>
  </div>
</section>

<section id="contact">
  <div class="container">
    <h2>Contact Us</h2>
    <p>Email: info@beautysalon.com</p>
    <p>Phone: +123 456 7890</p>
  </div>
</section>

<footer>
  <p>&copy; 2026 Luxury Beauty Salon. All Rights Reserved.</p>
</footer>

<script>
document.getElementById("bookingForm").addEventListener("submit", function(e) {
  e.preventDefault();
  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();
  const date = document.getElementById("date").value;
  const messageBox = document.getElementById("formMessage");

  if (!name || !email || !date) {
    messageBox.innerHTML = "<p class='error'>Please fill in all required fields.</p>";
    return;
  }

  messageBox.innerHTML = "<p style='color: var(--gold);'>Appointment request submitted successfully!</p>";
  this.reset();
});
</script>

</body>
</html>
