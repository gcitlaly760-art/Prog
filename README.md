<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi página web</title>
  <link rel="stylesheet" href="styles.css">
</head>
  <style>
:root {
  --azul:silver;
  --azul-oscuro: #1e3a8a;
  --texto: #1e293b;
  --fondo: #f8fafc;
  --lateral: #dbe7fb;
  --borde: #93b4ee;
  --amarillo: #fde68a;
  --pie: #1e293b;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 15px;
  line-height: 1.5;
  color: var(--texto);
  background: var(--fondo);
}

a { color: var(azul); }


.encabezado {
  background: var(--azul);
  color:black;
  padding: 28px 6% 16px;
}
.encabezado h1 { margin: 0 0 14px; font-size: 1.8rem; }

.menu { display: flex; flex-wrap: wrap; gap: 6px 22px; }
.menu a { color:yellow; text-decoration: none; font-size: .95rem; }
.menu a:hover { text-decoration: underline; }

.contenedor {
  display:lavender;
  grid-template-columns: 1fr 260px;
  align-items: stretch;
  gap: 0 20px;
  padding: 0 6% 20px;
}
main {
  padding-top: 18px;
  display: flex;
  flex-direction: column;
  gap: 14px;
}


.tarjeta {
  border: 1.5px dashed var(--borde);
  border-radius: 4px;
  padding: 12px 14px;
}
.tarjeta h2 {
  margin: 0 0 8px;
  font-size: 1rem;
  color: var(--azul-oscuro);
}
.tarjeta p { margin: 0; }

mark { background: var(--amarillo); padding: 0 3px; }

blockquote {
  margin: 10px 0 0;
  padding: 6px 12px;
  border-left: 4px solid var(--borde);
  background:yellowgreen;
  font-style: italic;
}
blockquote cite { display: block; font-size: .85rem; opacity: .8; }

.en-linea {
  display: flex;
  flex-wrap: wrap;
  gap: 4px 24px;
  margin: 0 0 6px;
  padding-left: 18px;
}
.en-linea li { padding-left: 2px; }
dl { margin: 0; }
dt { display: inline; font-weight: 700; }
dd { display: inline; margin: 0; }


table { width: 100%; border-collapse: collapse; }
th, td { padding: 3px 8px; border: 1px solid var(--borde); border-left: none; border-right: none; text-align: left}
th { background: var(--azul); color:black; }


.multimedia { display: flex; flex-wrap: wrap; align-items: flex-start; gap: 18px; }
figure { margin: 0; }
figure img { width: 140px; height: 105px; object-fit: cover; display: block; }
figcaption { font-size: .8rem; font-style: italic; margin-top: 3px; }
.multimedia video { width: 240px; height: 105px; background:pink; object-fit: cover; }
.campo {
  display: grid;
  grid-template-columns: 170px minmax(0, 1fr);
  align-items: center;
  gap: 8px;
  max-width: 460px;
  margin-bottom: 8px;
  font-size: .9rem;
}
.campo small { font-size: .85em; }
input, select {
  padding: 4px 6px;
  border: 1px solid var(--borde);
  border-radius: 2px;
  font: inherit;
  background:pink;
  color: var(--texto);
}
input:focus, select:focus { outline: 2px solid var(--azul); }
input:user-invalid, select:user-invalid { border-color: #dc2626; }

.btn {
  background: var(--azul);
  color: #fff;
  border: 0;
  padding: 7px 22px;
  border-radius: 6px;
  font-weight: 700;
  cursor: pointer;
}
.btn:hover { background: var(--azul-oscuro); }

.barra-lateral {
  background: var(--lateral);
  padding: 18px 14px;
}
.barra-lateral h2 { margin: 0 0 2px; font-size: 1.05rem; color: var(--azul-oscuro); }
.barra-lateral > p { margin: 0 0 12px; font-size: .85rem; }
details {
  border: 1.5px dashed var(--borde);
  background: #fff;
  border-radius: 3px;
  padding: 8px 10px;
}
summary { cursor: pointer; font-weight: 700; font-size: .9rem; color: var(--azul-oscuro); }
details p { margin: 4px 0 0; font-size: .85rem; }

.pie { background: var(--pie); color: #e2e8f0; text-align: center; padding: 18px; }
.pie p { margin: 0; font-size: .85rem; }

@media (max-width: 800px) {
  .contenedor { grid-template-columns: 1fr; }
  .barra-lateral { margin-bottom: 14px; }
  .campo { grid-template-columns: 1fr; }
}
 </style>
</head>
<body>
<header class="encabezado">
    <h1>Mi página web</h1>
    <nav class="menu" aria-label="Navegación principal">
      <a href="#texto">Texto</a>
      <a href="#listas">Listas</a>
      <a href="#tabla">Tabla</a>
      <a href="#multimedia">Multimedia</a>
      <a href="#formulario">Formulario</a>
      <a href="#contacto">Contacto</a>
    </nav>
    </style>
  </header>

  <div class="contenedor">

    <main>

      
      <section id="texto" class="tarjeta">
        <h2>Elementos de texto</h2>
        <p>
          Párrafo con <strong>negrita</strong>,<em>cursiva</em> y <mark>resaltado</mark>
          <q>Cita destacada.</q>
          <a href="https://developer.mozilla.org/es/" target="_blank" rel="noopener">Enlace externo</a>.
        </p>
        <blockquote>
          La programación es un mundo fascinante y lleno de posibilidades. Ya sea que estés creando la lógica detrás de una aplicación web, conectando bases de datos, diseñando interfaces responsivas o automatizando tareas, siempre hay algo nuevo por aprender y construir.
         
        </blockquote>
      </section>

      <section id="listas" class="tarjeta">
        <h2>Listas</h2>
        <ul class="en-linea">
          <li>HTML</li>
          <li>CSS</li>
          <li>JavaScript</li>
        </ul>
        <ol class="en-linea">
          <li>Crear</li>
          <li>Escribir</li>
          <li>Publicar</li>
        </ol>
        <dl>
          <dt>Lista de definiciones:</dt>
          <dd>término y descripción</dd>
        </dl>
      </section>

      
      <section id="tabla" class="tarjeta">
        <h2>Tabla</h2>
        <table>
          <thead>
            <tr><th scope="col">Tecnología</th><th scope="col">Función</th></tr>
          </thead>
          <tbody>
            <tr><td>HTML</td><td>Estructura</td></tr>
            <tr><td>CSS</td><td>Diseño</td></tr>
            <tr><td>JavaScript</td><td>Interactividad</td></tr>
          </tbody>
        </table>
      </section>

  
      <section id="multimedia" class="tarjeta">
        <h2>Multimedia</h2>
        <div class="multimedia">
          <figure>
            <img src="pro.jpg">
          </figure>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/as1opL254NA" title="video de ejemplo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
      </section>

    
      <section id="formulario" class="tarjeta">
        <h2>Formulario</h2>
        <form action="mailto:correo@ejemplo.com" method="post" enctype="text/plain">
          <div class="campo">
            <label for="nombre">Nombre</label>
            <input type="text" id="nombre" name="nombre" required>
          </div>
          <div class="campo">
            <label for="correo">Correo</label>
            <input type="email" id="correo" name="correo" required>
          </div>
          <div class="campo">
            <label for="pais">País </label>
            <select id="pais" name="pais" required>
              <option value="">Selecciona...</option>
              <option>Guatemala</option>
              <option>México</option>
              <option>Colombia</option>
              <option>España</option>
              <option>Argentina</option>
              <option>Otro</option>
            </select>
          </div>
          <button type="submit" class="btn">Enviar</button>
        </form>
      </section>

    </main>

    <aside class="barra-lateral" id="contacto">
      <h2>Barra lateral</h2>
      <p>Contenido relacionado</p>
      <details>
        <summary>Desplegable</summary>
        <p>Ver más contenido</p>
      </details>
    </aside>

  </div>

  
</body>
</html>
