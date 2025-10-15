
# Informe del Proyecto: Books Nest

## Introducción

El presente proyecto consiste en la creación de un **anuncio publicitario** para la editorial de libros **Books Nest**, una marca dedicada a publicar obras literarias y educativas con un enfoque cálido, profesional e inspirador.

La propuesta visual y conceptual busca reflejar la esencia de **Books Nest**: un lugar donde las historias encuentran su hogar y los sueños se publican “página a página”.

## Recursos usados (IA mencionadas)

Durante el desarrollo del proyecto se emplearon diversas herramientas de **inteligencia artificial** para asistir en el proceso creativo:

* **ChatGPT** → Creación del nombre de la marca, guion publicitario, diseño del logo y descripción de productos.
* **Copilot** → Generación de prompts para ChatGPT, eslogan de la marca y creación de imágenes de productos.

## Contenido:

### Vídeo:
Anuncio publicitario titulado *“Publicamos sueños, página a página”*.
Duración: 4–5 minutos.
Tono: Inspirador, cálido y profesional.
Estilo: Cinematográfico con paleta de tonos suaves (rosa, terracota, verde grisáceo, marrón oscuro).
Música: Piano suave y cuerdas cálidas.

**Estructura del guion publicitario:**

1. **Introducción – El poder de una historia**
   Muestra el origen de una idea y el valor de cada historia.
   Imágenes poéticas de escritura y lectura.
   Voz en off femenina con tono sereno y emotivo.

2. **El nacimiento de un libro**
   Refleja el proceso editorial desde la creación hasta la publicación.
   Participan autores, editores y diseñadores.

3. **Testimonios – Voces que cobran vida**
   Testimonios reales de autores y lectores que destacan la cercanía y confianza de Books Nest.

4. **La magia de leer y compartir**
   Escenas cotidianas de lectura que evocan emoción, aprendizaje y conexión humana.

5. **Cierre – Publicamos sueños**
   Logo de Books Nest acompañado del eslogan y la invitación a visitar su sitio web y redes sociales.

Puedes ver el guión completo en este enlace: [Guión publicitario](https://github.com/NuriaRodriguezPardo/IAVA/blob/main/Proyecto/Gui%C3%B3n%20Publicitario.pdf)

### Página web:
La página web de **Books Nest** presentará la marca, su catálogo editorial y su filosofía.
Incluirá el video publicitario, información sobre servicios de publicación, contacto y tienda en línea con productos inspirados en la lectura.

**Codigo:**
```html
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Books Nest</title>
    <style>
        body {
            margin: 0;
            font-family: 'Lato', sans-serif;
            background-color: #D7ACC4;
            color: #6A4641;
        }

        header {
            background-color: #8F4242;
            color: white;
            padding: 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        header img {
            height: 60px;
        }

        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }

        .section {
            padding: 40px 20px;
        }

        .section h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2em;
            margin-bottom: 20px;
            color: #6A4641;
        }

        .grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .card {
            background-color: #D6B1A5;
            border-radius: 8px;
            padding: 20px;
            width: 300px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .card img {
            width: 100%;
            height: auto;
            border-radius: 4px;
            margin-bottom: 10px;
        }

        footer {
            background-color: #738886;
            color: white;
            text-align: center;
            padding: 30px 20px;
        }
    </style>
</head>

<body>

    <header>
        <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Logo.png" alt="Books Nest Logo">
        <nav>
            <a href="#">Inicio</a>
            <a href="#productos">Productos</a>
            <a href="#libros">Libros</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <section class="section" id="productos">
        <h2>Productos destacados</h2>
        <div class="grid">
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Tazas.png" alt="Tazas literarias">
                <h3>Tazas literarias</h3>
                <p>Diseños inspirados en clásicos y frases de autores.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Termos.png" alt="Termos Books Nest">
                <h3>Termos grandes y pequeños</h3>
                <p>Perfectos para acompañar tus lecturas.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Bags.png" alt="Tote Bags">
                <h3>Tote Bags</h3>
                <p>Ilustraciones literarias y colores cálidos.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Cuadernos.png" alt="Cuadernos">
                <h3>Cuadernos</h3>
                <p>Para escribir tus ideas, sueños y relatos.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Pines.png" alt="Pines esmaltados">
                <h3>Pines esmaltados</h3>
                <p>Pequeñas joyas literarias para coleccionar.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Caja.png" alt="Cajas regalo">
                <h3>Cajas regalo</h3>
                <p>Libros, velas y detalles para lectores apasionados.</p>
            </div>
        </div>
    </section>

    <section class="section" id="libros">
        <h2>Libros que amamos</h2>
        <div class="grid">
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/OrgulloYPrejuicio.png" alt="Orgullo y prejuicio">
                <h3>Orgullo y prejuicio</h3>
                <p>Jane Austen</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/AliciaEnElPaisDeLasMaravillas.png" alt="Alicia en el país de las maravillas">
                <h3>Alicia en el país de las maravillas</h3>
                <p>Lewis Carroll</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Arturo.png" alt="Arturo">
                <h3>Arturo</h3>
                <p>La leyenda del Rey Arturo</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/ElJardinSecreto.png" alt="El jardín secreto">
                <h3>El jardín secreto</h3>
                <p>Frances Hodgson Burnett</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/CumbresBorrascosas.png" alt="Cumbres borrascosas">
                <h3>Cumbres borrascosas</h3>
                <p>Emily Brontë</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/LaIslaDelTesoro.png" alt="La isla del tesoro">
                <h3>La isla del tesoro</h3>
                <p>Robert Louis Stevenson</p>
            </div>
        </div>
    </section>

    <footer id="contacto">
        <p>Contacto: hola@booksnest.com</p>
        <p>Síguenos en redes sociales: @booksnest</p>
        <p><em>“Publicamos sueños, página a página”</em></p>
    </footer>

</body>

</html>
```


## Productos y Material Promocional

Diseñados con IA (ChatGPT y Copilot), los productos reflejan la estética cálida y literaria de Books Nest:

* Termos en tonos burdeos y verde grisáceo con el logo.
* Tazas con frases literarias.
* Tote bags ilustradas.
* Cuadernos para escritura creativa.
* Velas aromáticas con etiquetas personalizadas.
* Pins esmaltados con motivos de lectura.
* Postales y flyers con el eslogan **“Publicamos sueños, página a página.”**

Todos los elementos utilizan la **paleta de colores oficial**:

* Rosa suave (#D7ACC4)
* Terracota claro (#D6B1A5)
* Verde grisáceo (#738886)
* Rojo profundo (#8F4242)
* Marrón oscuro (#6A4641)

## Conclusión

El proyecto **Books Nest** combina creatividad, tecnología e inspiración para dar vida a una marca editorial que valora la emoción detrás de cada historia.
