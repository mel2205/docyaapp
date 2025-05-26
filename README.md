<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DocYa - Aplicación Médica</title>
  <style>
    /* Estilos básicos */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
    }

    header {
      background-color: #0078d4;
      color: white;
      text-align: center;
      padding: 1rem;
    }

    header h1 {
      font-size: 1.8rem;
      margin: 0;
    }

    nav {
      display: flex;
      justify-content: space-around;
      background-color: #004a99;
      padding: 0.75rem 0;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
      padding: 0.5rem 1rem;
      border-radius: 5px;
    }

    nav a:hover {
      background-color: #005bb5;
    }

    .page {
      display: none;
      padding: 1.5rem;
    }

    .page.active {
      display: block;
    }

    footer {
      background-color: #004a99;
      color: white;
      text-align: center;
      padding: 1rem;
      position: fixed;
      bottom: 0;
      width: 100%;
    }

    /* Estilos de accesibilidad */
    h2 {
      font-size: 1.6rem;
      color: #333;
    }

    p {
      font-size: 1.2rem;
      line-height: 1.5;
    }

    button {
      background-color: #0078d4;
      color: white;
      border: none;
      padding: 1rem 1.5rem;
      font-size: 1.2rem;
      border-radius: 8px;
      cursor: pointer;
    }

    button:hover {
      background-color: #005bb5;
    }

    input, select {
      width: 100%;
      padding: 0.8rem;
      font-size: 1.1rem;
      margin: 0.5rem 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    label {
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
      display: block;
    }
  </style>
</head>
<body>

  <!-- Encabezado -->
  <header>
    <h1>DocYa - Tu Salud en un Clic</h1>
  </header>

  <!-- Navegación -->
  <nav>
    <a href="#" onclick="showPage('inicio')">Inicio</a>
    <a href="#" onclick="showPage('registro')">Registro</a>
    <a href="#" onclick="showPage('agendamiento')">Agendar Cita</a>
    <a href="#" onclick="showPage('videollamada')">Videollamada</a>
    <a href="#" onclick="showPage('recordatorios')">Recordatorios</a>
  </nav>

  <!-- Páginas -->
  <div id="inicio" class="page active">
    <h2>Bienvenido a DocYa</h2>
    <p>DocYa es una aplicación diseñada para facilitar el acceso a consultas médicas y mejorar la calidad de vida de los adultos mayores. Usa el menú para navegar entre las secciones.</p>
    <button onclick="alert('Gracias por usar DocYa!')">Más Información</button>
  </div>

  <div id="registro" class="page">
    <h2>Registro de Usuario</h2>
    <p>Completa el siguiente formulario para registrarte en la aplicación.</p>
    <form onsubmit="handleRegister(event)">
      <label for="nombre">Nombre Completo:</label>
      <input type="text" id="nombre" name="nombre" required>
      <label for="email">Correo Electrónico:</label>
      <input type="email" id="email" name="email" required>
      <label for="password">Contraseña:</label>
      <input type="password" id="password" name="password" required>
      <button type="submit">Registrar</button>
    </form>
  </div>

  <div id="agendamiento" class="page">
    <h2>Agendar Cita Médica</h2>
    <p>Selecciona la fecha y hora para tu cita médica.</p>
    <form onsubmit="handleSchedule(event)">
      <label for="fecha">Fecha:</label>
      <input type="date" id="fecha" name="fecha" required>
      <label for="hora">Hora:</label>
      <input type="time" id="hora" name="hora" required>
      <button type="submit">Agendar</button>
    </form>
  </div>

  <div id="videollamada" class="page">
    <h2>Iniciar Videollamada</h2>
    <p>Haz clic en el botón para iniciar una videollamada con tu médico.</p>
    <button onclick="alert('Iniciando videollamada...')">Iniciar Videollamada</button>
  </div>

  <div id="recordatorios" class="page">
    <h2>Gestión de Recordatorios</h2>
    <p>Añade un recordatorio para tus medicamentos o citas.</p>
    <form onsubmit="handleReminder(event)">
      <label for="recordatorio">Escribe tu recordatorio:</label>
      <input type="text" id="recordatorio" name="recordatorio" required>
      <button type="submit">Guardar Recordatorio</button>
    </form>
  </div>

  <!-- Pie de página -->
  <footer>
    <p>DocYa - Tu Salud en un Clic © 2025</p>
  </footer>

  <!-- JavaScript -->
  <script>
    function showPage(pageId) {
      // Ocultar todas las páginas
      const pages = document.querySelectorAll('.page');
      pages.forEach(page => page.classList.remove('active'));

      // Mostrar la página seleccionada
      const selectedPage = document.getElementById(pageId);
      selectedPage.classList.add('active');
    }

    function handleRegister(event) {
      event.preventDefault();
      alert('¡Registro completado con éxito!');
    }

    function handleSchedule(event) {
      event.preventDefault();
      alert('¡Cita agendada correctamente!');
    }

    function handleReminder(event) {
      event.preventDefault();
      alert('¡Recordatorio guardado!');
    }
  </script>

</body>
</html>
 
