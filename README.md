<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Toñitín La Estación del Corte - Agenda tu Cita</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: #000;
      color: #fff;
      margin: 0;
      padding: 0;
    }
    header {
      background: #ffbb00;
      padding: 20px;
      text-align: center;
      color: #111;
    }
    header img {
      max-width: 200px;
      margin-bottom: 10px;
    }
    main {
      padding: 20px;
    }
    form {
      background: #222;
      padding: 20px;
      border-radius: 10px;
      max-width: 500px;
      margin: auto;
    }
    label {
      display: block;
      margin-top: 15px;
    }
    input, select, textarea, button {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border-radius: 5px;
      border: none;
    }
    button {
      background: #ffbb00;
      color: #111;
      font-weight: bold;
      cursor: pointer;
      margin-top: 20px;
    }
    footer {
      text-align: center;
      margin-top: 40px;
      color: #666;
    }
  </style>
  <script>
    function enviarWhatsApp(event) {
      event.preventDefault();
      const nombre = document.querySelector('[name="nombre"]').value;
      const telefono = document.querySelector('[name="telefono"]').value;
      const fecha = document.querySelector('[name="fecha"]').value;
      const hora = document.querySelector('[name="hora"]').value;
      const servicio = document.querySelector('[name="servicio"]').value;
      const comentarios = document.querySelector('[name="comentarios"]').value;

      const mensaje = `Hola, quiero agendar una cita:%0A- Nombre: ${nombre}%0A- Teléfono: ${telefono}%0A- Fecha: ${fecha}%0A- Hora: ${hora}%0A- Servicio: ${servicio}%0A- Comentario: ${comentarios}`;

      const numero = '18093554572';
      window.open(`https://wa.me/${numero}?text=${mensaje}`, '_blank');
    }
  </script>
</head>
<body>
  <header>
    <img src="logo.png" alt="Logo de la barbería">
    <h1>Toñitín - La Estación del Corte</h1>
    <p>Más calidad, más confort ✂️</p>
  </header>
  <main>
    <h2>Reserva tu cita aquí</h2>
    <form onsubmit="enviarWhatsApp(event)">
      <label>Nombre completo:
        <input type="text" name="nombre" required>
      </label>
      <label>WhatsApp:
        <input type="tel" name="telefono" required>
      </label>
      <label>Fecha de la cita:
        <input type="date" name="fecha" required>
      </label>
      <label>Hora:
        <input type="time" name="hora" required>
      </label>
      <label>Servicio:
        <select name="servicio" required>
          <option value="Recorte normal">Recorte normal</option>
          <option value="Corte completo">Corte completo</option>
          <option value="Solo cerquillo">Solo cerquillo</option>
          <option value="Corte para niños">Corte para niños</option>
        </select>
      </label>
      <label>Comentarios:
        <textarea name="comentarios" rows="3"></textarea>
      </label>
      <button type="submit">Reservar cita por WhatsApp</button>
    </form>
  </main>
  <footer>
    <p>&copy; 2025 Toñitín - La Estación del Corte. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
