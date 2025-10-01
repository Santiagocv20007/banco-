<!DOCTYPE html>
<html lang="es">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Banco a la U</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background: linear-gradient(135deg, #0a0a0a, #1a001f);
      color: #eee;
      line-height: 1.6;
      scroll-behavior: smooth;
    }
    /* Banner con imagen */
    .hero {
      background: url('https://images.unsplash.com/photo-1556740738-b6a63e27c4df') no-repeat center center/cover;
      height: 60vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: white;
      position: relative;
    }
    .hero::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.6); /* oscurece para resaltar el texto */
    }
    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 800px;
    }
    .hero-content h1 {
      font-size: 2.8em;
      margin-bottom: 15px;
      color: #c084fc;
      text-shadow: 2px 2px 8px rgba(0,0,0,0.8);
    }
    .hero-content p {
      font-size: 1.3em;
      margin-bottom: 20px;
    }
    .hero-content a {
      display: inline-block;
      padding: 14px 24px;
      background: linear-gradient(90deg, #5a2a82, #c084fc);
      color: white;
      border-radius: 10px;
      font-weight: bold;
      text-decoration: none;
      transition: all 0.3s;
    }
    .hero-content a:hover {
      background: linear-gradient(90deg, #c084fc, #5a2a82);
      transform: scale(1.05);
    }
    nav {
      background: #111;
      padding: 12px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    nav a {
      color: #c084fc;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s, transform 0.2s;
    }
    nav a:hover {
      color: #fff;
      transform: scale(1.1);
    }
    .container {
      width: 90%;
      max-width: 1100px;
      margin: auto;
      padding: 30px 0;
    }
    section {
      margin-bottom: 60px;
      opacity: 0;
      transform: translateY(40px);
      transition: opacity 1s ease, transform 1s ease;
    }
    section.visible {
      opacity: 1;
      transform: translateY(0);
    }
    section h2 {
      color: #c084fc;
      margin-bottom: 20px;
      text-align: center;
    }
    .casillas {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }
    .card {
      background: rgba(30, 0, 40, 0.9);
      border: 1px solid rgba(255,255,255,0.1);
      padding: 20px;
      border-radius: 14px;
      text-align: center;
      box-shadow: 0px 6px 20px rgba(0,0,0,0.7);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: scale(1.05);
      background: rgba(90,42,130,0.6);
      box-shadow: 0px 8px 25px rgba(0,0,0,0.9);
    }
    form {
      background: rgba(30, 0, 40, 0.9);
      padding: 25px;
      border-radius: 16px;
      box-shadow: 0px 6px 20px rgba(0,0,0,0.8);
    }
    label {
      font-weight: bold;
      display: block;
      margin: 10px 0 5px;
      color: #c084fc;
    }
    input, select, textarea {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 8px;
      margin-bottom: 15px;
      background: #1e1e2e;
      color: white;
      font-size: 1em;
      outline: none;
      transition: border 0.3s, background 0.3s;
    }
    input:focus, select:focus, textarea:focus {
      border: 1px solid #c084fc;
      background: #2a2a3d;
    }
    button {
      width: 100%;
      padding: 14px;
      background: linear-gradient(90deg, #5a2a82, #c084fc);
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 1.1em;
      cursor: pointer;
      font-weight: bold;
      transition: all 0.3s;
    }
    button:hover {
      background: linear-gradient(90deg, #c084fc, #5a2a82);
      transform: scale(1.05);
    }
    footer {
      text-align: center;
      padding: 20px;
      background: #111;
      margin-top: 20px;
      font-size: 0.9em;
      color: #aaa;
    }
  </style>
</head>
<body>

  <!-- Hero con imagen -->
  <div class="hero">
    <div class="hero-content">
      <h1>Bienvenido a Banco a la U</h1>
      <p>Tu banco digital para estudiantes y profesionales jóvenes</p>
      <a href="#formulario">Abre tu cuenta ahora</a>
    </div>
  </div>

  <nav>
    <a href="#quienes">Quiénes Somos</a>
    <a href="#beneficios">Beneficios</a>
    <a href="#servicios">Servicios</a>
    <a href="#testimonios">Testimonios</a>
    <a href="#formulario">Abrir Cuenta</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <div class="container">
    <section id="quienes">
      <h2>Quiénes Somos</h2>
      <p>
        En <strong>Banco a la U</strong> Somos una entidad financiera 
        que busca garantizar una oportunidad 
        para aquellos que quieran triunfar
        , nos centramos en los estudiantes de bachiller
        , universitarios y profesores.
      </p>
    </section>

    <section id="beneficios">
      <h2>Beneficios de ser parte de Banco a la U</h2>
      <div class="casillas">
        <div class="card">
          <h3>✔️ Sin costos ocultos</h3>
          <p>Transparencia total en nuestras tarifas y operaciones.</p>
        </div>
        <div class="card">
          <h3>💳 Tarjeta Universitaria</h3>
          <p>Obtén una tarjeta con beneficios exclusivos para estudiantes.</p>
        </div>
        <div class="card">
          <h3>📲 100% Digital</h3>
          <p>Accede a tu cuenta y haz transacciones desde tu celular.</p>
        </div>
        <div class="card">
          <h3>🎓 Créditos Educativos</h3>
          <p>Financia tus estudios con tasas preferenciales.</p>
        </div>
      </div>
    </section>

    <section id="servicios">
      <h2>Nuestros Servicios</h2>
      <div class="casillas">
        <div class="card">
          <h3>Cuentas de Ahorro</h3>
          <p>En esta cuenta los estudiantes
             podrán depositar el dinero que en un futuro
             será destinado a su carrera universitaria o
             otros gastos dentro del estudio.</p>
        </div>
        <div class="card">
          <h3>Préstamos Estudiantiles</h3>
          <p>Financia tu carrera universitaria de manera fácil y rápida.</p>
        </div>
        <div class="card">
          <h3>Billetera Digital</h3>
          <p>en esta cuenta los estudiantes
            podrán depositar el dinero que en un futuro
             será destinado a su carrera universitaria o
             otros gastos dentro del estudio.</p>
        </div>
        <div class="card">
          <h3>Seguros Universitarios</h3>
          <p>Protección y respaldo para ti y tus estudios.</p>
        </div>
      </div>
    </section>

    <section id="testimonios">
      <h2>Lo que dicen nuestros clientes</h2>
      <div class="casillas">
        <div class="card">
          <p>"Gracias a Banco a la U pude financiar mis estudios de posgrado sin preocupaciones."</p>
          <strong>- Laura, estudiante de Derecho</strong>
        </div>
        <div class="card">
          <p>"La aplicación móvil es muy práctica, hago todas mis transacciones desde el celular."</p>
          <strong>- Andrés, estudiante de Ingeniería</strong>
        </div>
      </div>
    </section>

    <section id="formulario">
      <h2>Solicita tu cuenta</h2>
      <form action="https://formspree.io/f/tu_codigo" method="POST">
        <label for="nombre">Nombre completo</label>
        <input type="text" name="nombre" required>

        <label for="email">Correo electrónico</label>
        <input type="email" name="email" required>

        <label for="telefono">Teléfono</label>
        <input type="tel" name="telefono" required>

        <label for="tipoCuenta">Tipo de cuenta</label>
        <select name="tipoCuenta">
          <option value="ahorros">Cuenta de ahorros</option>
          <option value="corriente">Cuenta corriente</option>
          <option value="universitaria">Cuenta universitaria</option>
        </select>

        <label for="mensaje">Mensaje adicional</label>
        <textarea name="mensaje" rows="4"></textarea>

        <button type="submit">Enviar solicitud</button>
      </form>
    </section>

    <section id="contacto">
      <h2>Contáctanos</h2>
      <p>Email: contacto@bancoalau.com</p>
      <p>Teléfono: +57 310 123 4567</p>
      <p>Dirección: Calle 123 #45-67, Bogotá, Colombia</p>
    </section>
  </div>

  <footer>
    © 2025 Banco a la U - Todos los derechos reservados
  </footer>

  <script>
    // Animaciones con Intersection Observer
    const secciones = document.querySelectorAll("section");
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        }
      });
    }, { threshold: 0.2 });

    secciones.forEach(sec => observer.observe(sec));

  </script>
</body>
</html>
