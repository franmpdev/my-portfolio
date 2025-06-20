<template>
  <header>
    <nav>
      <ul>
        <li><a href="#hero">Inicio</a></li>
        <li><a href="#about">Sobre mí</a></li>
        <li><a href="#projects">Proyectos</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contacto</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <!-- Hero -->
    <section id="hero">
      <img src="../src/assets/perfil.png" alt="Avatar Fran Moreno" class="avatar" />
      <h1>¡Hola! Soy <span class="highlight">Fran Moreno</span></h1>
      <p class="subtitle">Desarrollador Web Fullstack</p>
      <div class="social-links">
        <a href="https://github.com/franmpdev" target="_blank" aria-label="GitHub">
          <i class="fab fa-github"></i>
        </a>
        <a href="https://linkedin.com/in/francisco-javier-moreno-peco" target="_blank" aria-label="LinkedIn">
          <i class="fab fa-linkedin"></i>
        </a>
        <a href="mailto:franmorenopecofmp@gmail.com" aria-label="Email">
          <i class="fas fa-envelope"></i>
        </a>
      </div>
      <a href="#contact" class="cta">Contáctame</a>
    </section>

    <!-- Sobre mí -->
    <section id="about">
      <h2>Sobre mí</h2>
      <p>
        Soy un apasionado desarrollador web fullstack con experiencia en la creación de aplicaciones modernas, escalables y atractivas. Me encanta aprender nuevas tecnologías y afrontar retos que me permitan crecer profesionalmente.
      </p>
      <ul class="about-list">
        <li>💡 Apasionado por la innovación y el desarrollo web</li>
        <li>🤝 Abierto a colaboraciones y nuevos proyectos</li>
      </ul>
    </section>

    <!-- Proyectos -->
    <section id="projects">
      <h2>Proyectos Destacados</h2>
      <div class="projects-grid">
        <div class="project-card">
          <h3>App de Tareas</h3>
          <p>Aplicación desarrollada con Nest js, Angular y MySQL para gestionar tareas con autenticación.</p>
          <a href="https://github.com/tuusuario/proyecto1" target="_blank">Ver código</a>
        </div>
        <div class="project-card">
          <!-- aqui imagen-->
          <h3>Portfolio Animado</h3>
          <p>Portfolio interactivo con animaciones y efectos modernos usando Vue.</p>
          <a href="https://github.com/tuusuario/proyecto2" target="_blank">Ver código</a>
        </div>
        <div class="project-card">

          <h3>Gestión de peluquería canina</h3>
          <p>Aplicación desarrollada con Nest js, Angular y MySQL para la gestión de citas, clientes y mascotas de una peluquería canina.</p>
          <a href="https://github.com/tuusuario/proyecto3" target="_blank">Ver código</a>
        </div>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills">
      <h2>Skills</h2>
      <div class="skills-list">
        <span>JavaScript</span>
        <span>TypeScript</span>
        <span>Vue.js</span>
        <span>React</span>
        <span>Node.js</span>
        <span>Java</span>
        <span>PHP</span>
        <span>C#</span>
        <span>.Net</span>
        <span>SQL</span>
        <span>Tailwind CSS</span>
        <span>Express</span>
        <span>MongoDB</span>
        <span>HTML5</span>
        <span>CSS3</span>
        <span>Tailwind CSS</span>
        <span>Git & GitHub</span>
        <span>Docker</span>
      </div>
    </section>

    <!-- Contacto -->
    <section id="contact">
      <h2>Contacto</h2>
      <form class="contact-form" @submit.prevent>
        <input type="text" placeholder="Tu nombre" required />
        <input type="email" placeholder="Tu email" required />
        <textarea placeholder="Tu mensaje" required></textarea>
        <button type="submit">Enviar mensaje</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Francisco. Todos los derechos reservados.</p>
  </footer>
</template>

<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css');

html {
  scroll-behavior: smooth;
}

header {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.5rem 0;
  background: rgba(255,255,255,0.6);
  box-shadow: 0 2px 16px rgba(0,0,0,0.9);
  position: sticky;
  top: 0;
  z-index: 10;
  backdrop-filter: blur(8px);
}

nav ul {
  display: flex;
  gap: 2.5rem;
  list-style: none;
  padding: 0;
  margin: 0;
}

nav a {
  text-decoration: none;
  color: #222;
  font-weight: 500;
  font-size: 1.1rem;
  transition: color 0.6s;
  position: relative;
}

nav a::after {
  content: '';
  display: block;
  width: 0;
  height: 2px;
  background: #0077ff;
  transition: width 0.3s;
  position: absolute;
  left: 0;
  bottom: -4px;
}

nav a:hover {
  color: #0077ff;
}

nav a:hover::after {
  width: 100%;
}

main {
  max-width: 1000px;
  margin: 2.5rem auto;
  padding: 2.5rem;
  background: rgba(255,255,255,0.65); /* Más transparente */
  border-radius: 22px;
  box-shadow: 0 8px 40px rgba(0,119,255,0.10);
  backdrop-filter: blur(8px);
}

#hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.2rem;
  padding: 3rem 0 2rem 0;
  text-align: center;
  animation: fadeInHero 1.2s cubic-bezier(.4,0,.2,1);
}
@keyframes fadeInHero {
  0% { opacity: 0; transform: translateY(40px);}
  100% { opacity: 1; transform: translateY(0);}
}

.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #0077ff;
  box-shadow: 0 4px 24px rgba(0,119,255,0.10);
  margin-bottom: 1rem;
  background: #fff;
}

.highlight {
  color: #0077ff;
}

.subtitle {
  font-size: 1.3rem;
  color: #444;
  margin-bottom: 0.5rem;
}

.social-links {
  display: flex;
  gap: 1.2rem;
  margin-bottom: 1.2rem;
  justify-content: center;
}

.social-links a {
  color: #0077ff;
  font-size: 1.7rem;
  transition: color 0.2s, transform 0.2s;
}

.social-links a:hover {
  color: #00c6ff;
  transform: scale(1.15);
}

.cta {
  margin-top: 1.2rem;
  padding: 0.8rem 2.2rem;
  background: linear-gradient(90deg, #0077ff 60%, #00c6ff 100%);
  color: #fff;
  border: none;
  border-radius: 30px;
  font-weight: 600;
  font-size: 1.1rem;
  text-decoration: none;
  box-shadow: 0 2px 8px rgba(0,119,255,0.08);
  transition: background 0.2s, transform 0.2s;
  display: inline-block;
}

.cta:hover {
  background: linear-gradient(90deg, #005fcc 60%, #0099cc 100%);
  transform: translateY(-2px) scale(1.04);
}

section {
  margin: 3rem 0;
}

h2 {
  font-size: 2rem;
  color: #0077ff;
  margin-bottom: 1.2rem;
  text-align: center;
}

.about-list {
  list-style: none;
  padding: 0;
  margin: 1.2rem 0 0 0;
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
  align-items: center;
  color: #444;
  font-size: 1.1rem;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.project-card {
  background: #f7faff;
  border-radius: 16px;
  box-shadow: 0 2px 16px rgba(0,119,255,0.07);
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: transform 0.22s cubic-bezier(.4,0,.2,1), box-shadow 0.22s;
}
.project-card:hover {
  transform: translateY(-10px) scale(1.04) rotate(-1deg);
  box-shadow: 0 12px 40px rgba(0,119,255,0.18);
}

.project-card img {
  width: 100%;
  max-width: 220px;
  border-radius: 12px;
  margin-bottom: 1rem;
  box-shadow: 0 2px 8px rgba(0,119,255,0.08);
}

.project-card h3 {
  margin: 0.5rem 0 0.3rem 0;
  color: #0077ff;
  font-size: 1.2rem;
}

.project-card p {
  color: #444;
  font-size: 1rem;
  margin-bottom: 1rem;
  text-align: center;
}

.project-card a {
  color: #fff;
  background: #0077ff;
  padding: 0.5rem 1.2rem;
  border-radius: 20px;
  text-decoration: none;
  font-weight: 500;
  transition: background 0.2s;
}

.project-card a:hover {
  background: #005fcc;
}

.skills-list {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
  margin-top: 1.5rem;
}

.skills-list span {
  background: linear-gradient(90deg, #e0e7ff 60%, #f0fdfa 100%);
  color: #0077ff;
  padding: 0.6rem 1.2rem;
  border-radius: 18px;
  font-weight: 500;
  font-size: 1rem;
  box-shadow: 0 2px 8px rgba(0,119,255,0.06);
  margin-bottom: 0.5rem;
  transition: transform 0.18s, box-shadow 0.18s;
}
.skills-list span:hover {
  transform: scale(1.08) rotate(-2deg);
  box-shadow: 0 4px 16px rgba(0,119,255,0.13);
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 400px;
  margin: 0 auto;
  margin-top: 2rem;
}

.contact-form input,
.contact-form textarea {
  padding: 0.8rem 1rem;
  border-radius: 12px;
  border: 1px solid #c7d2fe;
  font-size: 1rem;
  background: #f7faff;
  resize: none;
  transition: border 0.2s;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none;
  border: 1.5px solid #0077ff;
}

.contact-form button {
  background: linear-gradient(90deg, #0077ff 60%, #00c6ff 100%);
  color: #fff;
  border: none;
  border-radius: 30px;
  font-weight: 600;
  font-size: 1.1rem;
  padding: 0.8rem 0;
  cursor: pointer;
  transition: background 0.2s, transform 0.2s;
}

.contact-form button:hover {
  background: linear-gradient(90deg, #005fcc 60%, #0099cc 100%);
  transform: translateY(-2px) scale(1.04);
}

footer {
  text-align: center;
  padding: 2rem 0 1rem 0;
  background: transparent;
  color: #888;
  font-size: 1rem;
}
.avatar {
  width: 170px;
  height: 170px;
  border-radius: 50%;
  object-fit: cover;
  border: 5px solid #0077ff;
  box-shadow: 0 6px 32px rgba(0,119,255,0.13);
  margin-bottom: 1.5rem;
  background: #fff;
}

#hero h1 {
  font-size: 3.2rem;
  font-weight: 800;
  color: #0077ff;
  margin-bottom: 0.7rem;
}

.subtitle {
  font-size: 1.7rem;
  color: #444;
  margin-bottom: 0.8rem;
}
</style>