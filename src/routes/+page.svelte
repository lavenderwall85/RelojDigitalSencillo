<script>
    let horaActual = new Date();
  
    // Actualizar la hora cada segundo
    setInterval(() => {
      horaActual = new Date();
    }, 1000);
  
    // Formatear la hora para mostrarla correctamente
    function formatearHora(hora) {
      let horas = String(hora.getHours()).padStart(2, '0');
      let minutos = String(hora.getMinutes()).padStart(2, '0');
      let segundos = String(hora.getSeconds()).padStart(2, '0');
      return `${horas}:${minutos}:${segundos}`;
    }
  </script>
  
  <main>
    <h1>Reloj Digital</h1>
    <div class="reloj">{formatearHora(horaActual)}</div>
  </main>
  
  <style>
    main {
      text-align: center;
      margin-top: 50px;
      font-family: Arial, sans-serif;
    }
  
    h1 {
      font-size: 24px;
      margin-bottom: 20px;
    }
  
    .reloj {
      font-size: 48px;
      font-weight: bold;
      color: #4CAF50;
      padding: 20px;
      border: 2px solid #4CAF50;
      display: inline-block;
      border-radius: 10px;
    }
  </style>
  