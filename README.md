<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Portfólio</title>
    <link rel="stylesheet" href="css/styles.css" />
  </head>
  <body> 
    <style>
    * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  text-decoration: none;
  border: none;
  outline: none;
  scroll-behavior: smooth;
  font-family: "poppins", sans-serif;
}
:root {
  --bg-color: #080808;
  --second-bg-color: #131313;
  --text-color: white;
  --main-color: #e100ff;
}
html {
  font-size: 60%;
  overflow-x: hidden;
}
body {
  background: var(--bg-color);
  color: var(--text-color);
}
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 4rem 12% 4rem;
  background: rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(10px);
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 5;
}
::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background-color: var(--bg-color);
  width: 50px;
}
::-webkit-scrollbar-thumb {
  background-color: var(--main-color);
}
.logo {
  font-size: 3rem;
  color: var(--text-color);
  font-weight: 800;
  cursor: pointer;
  transition: 0.3s ease;
}
.logo:hover {
  transform: scale(1.1);
}
.logo span {
  text-shadow: 0 0 25px var(--main-color);
}
.navbar a {
  font-size: 1.8rem;
  color: var(--text-color);
  margin-left: 4rem;
  font-weight: 500;
  transition: 0.3s ease;
  border-bottom: 3px solid transparent;
}
.navbar a:hover,
.navbar a.active {
  color: var(--main-color);
  border-bottom: 3px solid var(--main-color);
}
#menu-icon {
  font-size: 3.6rem;
  color: var(--main-color);
  display: none;
}
section {
  min-height: 100vh;
  padding: 10rem 12% 10rem;
}
.home {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15rem;
}
.home-content {
  display: flex;
  flex-direction: column;
  align-items: baseline;
  text-align: left;
  justify-content: center;
  margin-top: 8rem;
}
span {
  color: var(--main-color);
}
.logo span {
  color: var(--main-color);
}
.home-content h3 {
  margin-bottom: 2rem;
  margin-top: 1rem;
  font-size: 3.5rem;
}
.home-content h1 {
  font-size: 7rem;
  font-weight: 7000;
  margin-top: 1.5rem;
  line-height: 1;
}
.home-img {
  border-radius: 50%;
}
.home-img img {
  position: relative;
  top: 3rem;
  width: 30vw;
  border-radius: 50%;
  box-shadow: 0 0 25px var(--main-color);
  cursor: pointer;
  transition: 0.4s ease-in-out;
}
.home-img img:hover {
  box-shadow: 0 0 25px var(--main-color), 0 0 50px var(--main-color),
    0 0 100px var(--main-color);
}
.home-content p {
  font-size: 1.5rem;
  font-weight: 500;
  line-height: 1.8;
  max-width: 1000px;
}
.social-icons a {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 4.5rem;
  height: 4.5rem;
  background: transparent;
  border: 2px solid var(--main-color);
  font-size: 2.5rem;
  border-radius: 50%;
  color: var(--main-color);
  margin: 3rem 1.5rem 3rem 0;
  transition: 0.3 ease-in-out;
}
.social-icons a:hover {
  color: var(--text-color);
  transform: scale(1.3) translateY(-5px);
  box-shadow: 0 0 25px var(--main-color);
  background-color: var(--main-color);
}
.btn {
  display: inline-block;
  padding: 1rem 2.8rem;
  background: var(--main-color);
  box-shadow: 0 0 25px var(--main-color);
  border-radius: 4rem;
  font-size: 1.6rem;
  color: black;
  border: 2px solid transparent;
  letter-spacing: 0.1rem;
  font-weight: 600;
  transition: 0.3s ease-in-out;
  cursor: pointer;
}
.btn:hover {
  transform: scale(1.05);
  box-shadow: 0 0 50px var(--main-color);
}
.btn-group {
  display: flex;
  align-items: center;
  gap: 1.5rem;
}
.btn-group a:nth-last-of-type(2) {
  background-color: black;
  color: var(--main-color);
  border: 2px solid var(--main-color);
  box-shadow: 0 0 25px transparent;
}
.btn-group a:nth-of-type(2):hover {
  box-shadow: 0 0 25px var(--main-color);
  background-color: var(--main-color);
  color: black;
}
.text-animation {
  font-size: 34px;
  font-weight: 600;
  min-width: 280px;
}
.text-animation span {
  position: relative;
}
.text-animation span::before {
  content: "Desenvolvedor Frontend";
  color: var(--main-color);
  animation: words 20s infinite;
}
.text-animation span::after {
  content: "";
  background-color: var(--bg-color);
  position: absolute;
  width: calc(100% + 8px);
  height: 100%;
  border-left: 3px solid var(--bg-color);
  right: -8px;
  animation: cursor 0.6s infinite, typing 20s steps(14) infinite;
}
@keyframes cursor {
  to {
    border-left: 2px solid var(--main-color);
  }
}
@keyframes words {
  0%,
  20% {
    content: "Full Stack Developer";
  }
  21%,
  40% {
    content: "Database Specialist";
  }
  41%,
  60% {
    content: "Systems Analyst";
  }
  61%,
  80% {
    content: "Software Tester";
  }
  81%,
  100% {
    content: "Software Developer";
  }
}
@keyframes typing {
  10%,
  15%,
  30%,
  35%,
  50%,
  55%,
  70%,
  75%,
  90%,
  95% {
    width: 0;
  }
  5%,
  20%,
  25%,
  40%,
  45%,
  60%,
  65%,
  80%,
  85% {
    width: calc(100% + 8px);
  }
}
.heading {
  font-size: 8rem;
  text-align: center;
  margin: 5rem 0;
}
.sobre-mim {
  padding: 100px 15px;
  background: var(--second-bg-color);
}
.sobre-mim h2 {
  margin-bottom: 5rem;
}
.timeline-items {
  max-width: 1200px;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  position: relative;
}
.timeline-items::before {
  content: "";
  position: absolute;
  width: 5px;
  height: 100%;
  background-color: var(--main-color);
  left: calc(50% - 1px);
}
.timeline-item {
  margin-bottom: 40px;
  width: 100%;
  position: relative;
}
.timeline-item:last-child {
  margin-bottom: 0;
}
.timeline-item:nth-child(odd) {
  padding-right: calc(50% + 30px);
  text-align: right;
}
.timeline-item:nth-child(even) {
  padding-left: calc(50% + 30px);
}
.timeline-dot {
  height: 21px;
  width: 21px;
  background-color: var(--main-color);
  box-shadow: 0 0 25px var(--main-color), 0 0 25px var(--main-color);
  position: absolute;
  left: calc(50% - 8px);
  border-radius: 50%;
  top: 10px;
}
.timeline-date {
  font-size: 20px;
  font-weight: 800;
  color: white;
  margin: 6px 0 15px;
}
.timeline-content {
  background-color: var(--bg-color);
  border: 3px solid var(--main-color);
  padding: 30px 50px;
  border-radius: 4rem;
  box-shadow: 0 0 10px var(--main-color);
  cursor: pointer;
  transition: 0.3s ease-in-out;
}
.timeline-content:hover {
  transform: scale(1.05);
  box-shadow: 0 0 25px var(--main-color);
}
.timeline-content h3 {
  font-size: 20px;
  color: white;
  margin: 0 0 10px;
  font-weight: 500;
}
.timeline-content p {
  color: white;
  font-size: 15px;
  font-weight: 300;
  line-height: 22px;
}
.contact {
  background-color: var(--bg-color);
}
.contact h2 {
  margin-bottom: 3rem;
  color: white;
}
.contact form {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 3rem;
  margin: 5rem auto;
  text-align: center;
}
.contact form .input-box {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.contact form .input-box input,
.contact form textarea {
  width: 100%;
  padding: 2.5rem;
  font-size: 1.8rem;
  color: var(--text-color);
  background: var(--second-bg-color);
  border-radius: 2rem;
  border: 2px solid var(--main-color);
  margin: 1.5rem 0;
  resize: none;
}
.contact form .btn {
  margin-top: 2rem;
}
.footer {
  position: relative;
  bottom: 0;
  width: 100%;
  padding: 40px 0;
  background-color: var(--second-bg-color);
}
.footer .social {
  text-align: center;
  padding-bottom: 25px;
  color: var(--main-color);
}
.footer .social a {
  font-size: 25px;
  color: var(--main-color);
  border: 2px solid var(--main-color);
  width: 42px;
  height: 42px;
  line-height: 42px;
  display: inline-block;
  text-align: center;
  border-radius: 50%;
  margin: 0 10px;
  transition: 0.3s ease-in-out;
}
.footer .social a:hover {
  transform: scale(1.2) translateY(-10px);
  background-color: var(--main-color);
  color: black;
  box-shadow: 0 0 25px var(--main-color);
}
.footer ul {
  margin-top: 0;
  padding: 0;
  font-size: 18px;
  line-height: 1.6;
  margin-bottom: 0;
  text-align: center;
}
.footer ul li a {
  color: white;
  border-bottom: 3px solid transparent;
  transition: 0.3s ease-in-out;
}
.footer ul li a:hover {
  border-bottom: 3px solid var(--main-color);
}
.footer ul li {
  display: inline-block;
  padding: 0 15px;
}
.footer .copyright {
  margin-top: 50px;
  text-align: center;
  font-size: 16px;
  color: white;
}
@media (max-width: 1285px) {
  html {
    font-size: 55%;
  }
  .services-container {
    padding-bottom: 7rem;
    grid-template-columns: repeat(2, 1fr);
    margin: 0 5rem;
  }
}
@media (max-width: 991px) {
  header {
    padding: 2rem 3%;
  }
  section {
    padding: 10rem 3% 2rem;
  }
  .timeline-items::before {
    left: 7px;
  }
  .timeline-item:nth-child(odd) {
    padding-right: 0;
    text-align: left;
  }
  .timeline-item:nth-child(odd),
  .timeline-item:nth-child(even) {
    padding-left: 37px;
  }
  .timeline-dot {
    left: 0;
  }
  .services {
    padding-bottom: 7rem;
  }
  .timemonials .wrapper {
    grid-template-columns: repeat(1, 1fr);
  }
  .contact form {
    flex-direction: column;
  }
  .footer {
    padding: 2rem 3%;
  }
}
@media (max-width: 895px) {
  #menu-icon {
    display: block;
  }
  .navbar {
    position: absolute;
    top: 100%;
    right: 0;
    width: 50%;
    padding: 1rem 3%;
    background: rgba(0, 0, 0, 0.8);
    backdrop-filter: blur(20px);
    border-bottom-left-radius: 2rem;
    border-left: 2px solid var(--main-color);
    border-bottom: 2px solid var(--main-color);
    display: none;
  }
  .navbar.active {
    display: block;
  }
  .navbar a {
    display: block;
    font-size: 2rem;
    margin: 3rem 0;
    color: white;
  }
  .home {
    flex-direction: column-reverse;
    margin: 5rem 4rem;
  }
  .home-content h3 {
    font-size: 2.6rem;
  }
  .home-content h1 {
    font-size: 8rem;
    margin-top: 3rem;
  }
  .home-content p {
    max-width: 600px;
    margin: 0 auto;
  }
  .home-img img {
    width: 56vw;
  }
}
.skills {
  background: var(--bg-color);
}
.skills .container {
  background: var(--second-bg-color);
  color: var(--text-color);
  border-radius: 1rem;
  padding: 2rem;
  width: auto;
  margin-top: 7rem;
}
.info img {
  width: 10rem;
}
.skills .container .row {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  flex-wrap: wrap;
  gap: 2rem;
}
.skills .container .bar {
  margin-bottom: 21px;
  padding: 20px;
  border-radius: 1rem;
  background: var(--bg-color);
  transition: 0.3s ease;
  cursor: pointer;
}
.skills .container .bar:hover {
  box-shadow: 0 4px 20px var(--main-color);
  transform: scale(1.03);
}
.skills .container .bar .info {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  margin-top: 1rem;
}
.skills .container .bar .info span {
  font-size: 2rem;
  font-weight: 500;
  margin-left: 0.5rem;
}
@media screen and (max-width: 600px) {
  .skills .container {
    margin: 0;
    padding: 0;
  }
  .skills .container .row {
    grid-template-columns: repeat(2, 1fr);
    margin: 1rem;
    padding: 2rem 0.2rem 2rem 0.2rem;
    gap: 1rem;
  }
  .skills .container {
    margin-top: 5px;
    width: 100%;
  }
}
.projects {
  background: var(--second-bg-color);
}
</style>
<header class="header">
      <a href="#home" class="logo">Gabriela <span>Guedes</span></a>
      <i class="bx bx-menu" id="menu-icon"></i>
      <nav class="navbar">
        <a href="#home" class="active">Início</a>
        <a href="#sobremim">Sobre Mim</a>
        <a href="#skills">Minhas Skills</a>
        <a href="#projects">Projetos</a>
        <a href="#contact">Contato</a>
      </nav>
    </header>
    <section class="home" id="home">
      <div class="home-content">
        <h1>Olá, Eu Sou <span>Gabriela Guedes</span></h1>
        <h3 class="text-animation">Eu Sou <span></span></h3>
        <p>
          Com Profunda Paixão por Tecnologia, Estou me Especializando em
          Desenvlvimento Fullstack, Focado no Backend. Tenho Conhecimento em:
          <b>Javascript; CSS; Python; PHP.</b>
          Focado em Entregar Soluções Visuais Inovadoras e Funcionais.
        </p>
        <div class="social-icons">
          <a href="https://www.linkedin.com/in/gabriela-guedes-512177236/"
            ><img
              src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAUJJREFUSEvtlc0qRlEUhp+HUkZkYqT8FANRMvJTBi5DbkAZKBMjc6Wk3IFchgykyFiS/I2MlAkDZbG1v6/jfKKcjwm7dp2zdvt91nrXPvvIDw9/WJ8GQET0A8/qVTPg7wARsQksZuF1dbkqpA6IiCHgtCTYq15XgXwF6KtqVdmiLWAhZ7yhLlXJPu39qMmDucnnVcUbABExCbRl4Uf1MD1HxBjQkeMP6tHrgegCpoERoBXYURuSKlt0C3RnoQt1IAP2gakcP3tlribBkgPPwIq6Vqz8O4A7oD3Pj1ycVXdrC98B1PYm0A0wCrQUSMmquaqAbXU+2zcD7BUAJ+pwVcCQmnrxNiIiVdKTX+/VzqqANvWpADgGxuuiWrf+sx5cquniSxkWT1EKtahRABwAE/+A2of2ly1qxu1Z1vj9n36zq3gBLPzRGctIENYAAAAASUVORK5CYII="
          /></a>
          <a href="https://github.com/gabrielaguedes12"
            ><img
              src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAm9JREFUSEvFlU2IjlEUx39/kQ1ZIMkS5XOKZKGmiBI2hmKkKBn5Sk0yPko0+WgojeQj7AglzIYdCwuUiHyWSRYWPposTApxPGe6z3TfO8/7zjOLydm87z33f+7/nnPP+T9ikE2DfD41CcxsGLAcWALMBCZDT8wH4DlwJ/PfkPS72kWrEpjZIuAsMKmfLN8DmyTdLcIVEpjZbuBouG2ZKv4F9kg6noL7EJhZC9BW5tQCTLOk9thfQWBmCwBP1f1e3w3AFmA/MAToBLzeUwG/9RHgDHAKWBl89ZIe5CS9BGY2HHgFTAybrZIO+H8z83f4LOl7WI8Axkt6F9b7gMMh7jVQJ+mPr2OC1cC1KL12Sc1lSmVmx4BdEXaZJK9ABcFlYG0EmifpYUmCuqydn0XnnZa0PSXw8kzL05Q0vczhOcbMngCzw/pxlsHclOALMDYAOiQ1DJDgCrAmxHRJGpMSfMoGa1wA3JO0cIAEt4GlIaZb0siU4CkwKwC8W0bXkoCYPEjKV2BU8L+V5K1c8cgXgI1RYJOki2WyMLMm4HyEvSRpXUrgNb8JfAO6vc99/F2PJP0oIjIzn4dtYeB8EHNblTXJ9ZTAZ8I7aQKwGNgMrAd+halulPTTg0JJbgXc0IT8DTBDkk96pVyb2QqX36xUH4E5YfDmhyy2JnW/CjQWZNYgqSP3F4ndSWCH64+kQ9XewMwOZsn0SElkJzI52Rk7qsm1i1srcD8TsRfAS0nnkgx833G5tZSS6xxtZvWAS69PZ5skf/BeMzNX0r3AI8Bl2n/7WH+fTN/3T2anJM8kJpjisi3JH7uq/d+Pfq2bld37B8MT0hliYf0NAAAAAElFTkSuQmCC"
          /></a>
        </div>
        <div class="btn-group">
          <a href="#contact" class="btn">Contratar</a>
          <a href="https://wa.me/5521991204173" class="btn">Contato</a>
        </div>
      </div>
      <div class="home-img">
        <img src="imagens/profile.webp" alt="Foto1 ia" />
      </div>
    </section>
    <section class="sobre-mim" id="sobremim">
      <h2 class="heading">Sobre Mim</h2>
      <div class="timeline-items">
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2019</div>
          <div class="timeline-content">
            <h3>Início do Sonho</h3>
            <p>
              Impulsionado pela minha paixão por tecnologia, iniciei minha
              jornada na programação, estudando
              <b>lógica de programação</b>. Foi nessa experiência que descobri
              minha vocação e paixão pela área de desenvolvimento de software.
            </p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2021</div>
          <div class="timeline-content">
            <h3>Conclusão Ensino Médio</h3>
            <p>
              Nesse período que minha decisão pela área da técnologa se
              consolidou. Já tendo conhecimento em <b>HTML e CSS</b>, inspirado
              em evoluir, pela possibilidade de criar, inovar e solucionar
              problemas.
            </p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2023</div>
          <div class="timeline-content">
            <h3>Início das Graduações</h3>
            <p>
              Comecei um bacharelado em <b>Sistemas de Informação</b> e um
              tecnólogo em <b>Análise e Desenvolvimento de Sistemas</b>,
              buscando especialização e aprofundamento no Desenvolvimento de
              Software.
            </p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2024</div>
          <div class="timeline-content">
            <h3>Especializando em Desenvolvimento Frontend</h3>
            <p>
              Me Identifiquei com <b>Desenvolvimento Frontend</b> e Atualmente
              estou me Especializando Em <b>Desenvolvimento Backend</b>.
              Continuamente Aprimorando Minhas Habilidades em
              <b>HTML, CSS, PHP, JAVASCRIPT e Banco de Dados.</b>
            </p>
          </div>
        </div>
      </div>
    </section>
    <section class="skills" id="skills">
      <h2 class="heading">Minhas <span>Skills</span></h2>
      <div class="container">
        <div class="row" id="skillsContainer">
          <div class="bar">
            <div class="info">
              <img src="imagens/js (1).png" alt="Javascript icons" />
              <span>javaScript</span>
            </div>
          </div>
          <div class="bar">
            <div class="info">
              <img src="imagens/python (1).png" alt="Python Icons " />
              <span>Python</span>
            </div>
          </div>
          <div class="bar">
            <div class="info">
              <img src="imagens/html (1).png" alt=" HTML Icons" />
              <span>HTML5</span>
            </div>
          </div>
          <div class="bar">
            <div class="info">
              <img src="imagens/social (1).png" alt=" CSS icons" />
              <span>CSS3</span>
            </div>
          </div>
          <div class="bar">
            <div class="info">
              <img src="imagens/figma (1).png" alt="Figma Icons " />
              <span>Figma</span>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="projects" id="projects">
      <h2 class="heading">Meus <span>Projetos</span></h2>
    </section>
    <section class="contact" id="contact">
      <h2 class="heading">Contate-<span>Me</span></h2>
      <form
        action="https://formsubmit.co/gabr1.profissional@gmail.com"
        method="POST"
      >
        <div class="input-group">
          <div class="input-box">
            <input type="text" name="name" placeholder="Nome Completo" />
            <input type="email" name="email" placeholder="Email" required />
          </div>
          <div class="input-box">
            <input type="number" name="number" placeholder="Número Celular" />
            <input type="text" name="assunt" placeholder="Assunto" />
          </div>
        </div>
        <div class="input-group-2">
          <textarea
            name="text"
            id=""
            cols="30"
            rows="10"
            placeholder="Sua Mensagem"
          ></textarea>
          <input type="submit" value="Enviar Mensagem" class="btn" />
        </div>
      </form>
    </section>
    <footer class="footer">
      <div class="social">
        <a href="https://www.linkedin.com/in/gabriela-guedes-512177236/"
          ><img
            src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAUJJREFUSEvtlc0qRlEUhp+HUkZkYqT8FANRMvJTBi5DbkAZKBMjc6Wk3IFchgykyFiS/I2MlAkDZbG1v6/jfKKcjwm7dp2zdvt91nrXPvvIDw9/WJ8GQET0A8/qVTPg7wARsQksZuF1dbkqpA6IiCHgtCTYq15XgXwF6KtqVdmiLWAhZ7yhLlXJPu39qMmDucnnVcUbABExCbRl4Uf1MD1HxBjQkeMP6tHrgegCpoERoBXYURuSKlt0C3RnoQt1IAP2gakcP3tlribBkgPPwIq6Vqz8O4A7oD3Pj1ycVXdrC98B1PYm0A0wCrQUSMmquaqAbXU+2zcD7BUAJ+pwVcCQmnrxNiIiVdKTX+/VzqqANvWpADgGxuuiWrf+sx5cquniSxkWT1EKtahRABwAE/+A2of2ly1qxu1Z1vj9n36zq3gBLPzRGctIENYAAAAASUVORK5CYII="
        /></a>
        <a href="https://github.com/gabrielaguedes12"
          ><img
            src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAm9JREFUSEvFlU2IjlEUx39/kQ1ZIMkS5XOKZKGmiBI2hmKkKBn5Sk0yPko0+WgojeQj7AglzIYdCwuUiHyWSRYWPposTApxPGe6z3TfO8/7zjOLydm87z33f+7/nnPP+T9ikE2DfD41CcxsGLAcWALMBCZDT8wH4DlwJ/PfkPS72kWrEpjZIuAsMKmfLN8DmyTdLcIVEpjZbuBouG2ZKv4F9kg6noL7EJhZC9BW5tQCTLOk9thfQWBmCwBP1f1e3w3AFmA/MAToBLzeUwG/9RHgDHAKWBl89ZIe5CS9BGY2HHgFTAybrZIO+H8z83f4LOl7WI8Axkt6F9b7gMMh7jVQJ+mPr2OC1cC1KL12Sc1lSmVmx4BdEXaZJK9ABcFlYG0EmifpYUmCuqydn0XnnZa0PSXw8kzL05Q0vczhOcbMngCzw/pxlsHclOALMDYAOiQ1DJDgCrAmxHRJGpMSfMoGa1wA3JO0cIAEt4GlIaZb0siU4CkwKwC8W0bXkoCYPEjKV2BU8L+V5K1c8cgXgI1RYJOki2WyMLMm4HyEvSRpXUrgNb8JfAO6vc99/F2PJP0oIjIzn4dtYeB8EHNblTXJ9ZTAZ8I7aQKwGNgMrAd+halulPTTg0JJbgXc0IT8DTBDkk96pVyb2QqX36xUH4E5YfDmhyy2JnW/CjQWZNYgqSP3F4ndSWCH64+kQ9XewMwOZsn0SElkJzI52Rk7qsm1i1srcD8TsRfAS0nnkgx833G5tZSS6xxtZvWAS69PZ5skf/BeMzNX0r3AI8Bl2n/7WH+fTN/3T2anJM8kJpjisi3JH7uq/d+Pfq2bld37B8MT0hliYf0NAAAAAElFTkSuQmCC"
        /></a>
      </div>
      <ul class="list">
        <li>
          <a href="#home">Início</a>
        </li>
        <li>
          <a href="#projects">Projetos</a>
        </li>
        <li>
          <a href="#sobremim">Sobre Mim</a>
        </li>
        <li>
          <a href="#skills">Skills</a>
        </li>
        <li>
          <a href="https://wa.me/5521991204173">Contato</a>
        </li>
      </ul>
      <p class="copyright">©Gabriela Guedes | All Rights Reserved</p>
    </footer>
    <script src="script.js"></script>
  </body>
</html>
