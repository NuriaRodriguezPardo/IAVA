
# Informe del Proyecto: Books Nest

## Links
- [Página web](https://nuriarodriguezpardo.github.io/IAVA/)
- [Vídeo](https://www.youtube.com/watch?v=yDePbmAqFKg)

## Introducción

El presente proyecto consiste en la creación de un **anuncio publicitario** para la editorial de libros **Books Nest**, una marca dedicada a publicar obras literarias y educativas con un enfoque cálido, profesional e inspirador.

La propuesta visual y conceptual busca reflejar la esencia de **Books Nest**: un lugar donde las historias encuentran su hogar y los sueños se publican “página a página”.

## Recursos usados (IA mencionadas)

Este proyecto se basa en el **diseño de *prompts*** como habilidad clave. El *workflow* ha incorporado un *stack* de herramientas de IA para cubrir todo el proceso creativo:

* **Generación de prompts:**
   * **ChatGPT** → Creación del nombre de la marca, guion publicitario, diseño del logo y descripción de productos.
   * **Copilot** → Generación de prompts para ChatGPT, eslogan de la marca y creación de imágenes de productos.

* **Generación de Imagen (Activos Estáticos):**
    * **Reve:** Herramienta principal para la generación de la mayoria de las **fotos**.
    * **Copilot**

* **Generación de Video (Activos en Movimiento):**
    * **Pipit:** Utilizado para crear las escenas dinámicas del anuncio (ej. editores conversando, pareja en el café).
    * **Flow:** Empleado para la animación de *assets* estáticos, como el *unboxing* del producto y la animación final del logo.
    * **DeeVid AI**
    * **HeyGen** Empleado para la animación de avatares.

* **Generación de Audio**
    * **Suno:** Utilizado para componer la **pieza musical** instrumental de 2:30, siguiendo el *prompt* de estilo "acogedor, calmado, discreto, piano suave y cuerdas cálidas".
    * **Google AI Studio:** Utilizado para la creación de la **voz en off** (Texto-a-Voz) para el anuncio.
   
* **Post-Producción y Edición:**
    * **Google Vids:** Herramienta clave para ensamblar todas las escenas de vídeo de Pipit y Flow, sincronizar la música de Suno y la voz en off de AI Studio, y producir el anuncio final.

### Logotipo
El logotipo (referenciado en los archivos de imagen) combina elementos clásicos (un libro abierto) con un toque orgánico o artesanal (una pluma, un arco o elementos botánicos), estableciendo un tono profesional pero cercano.

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

* **Estética:** La web mantiene de forma estricta la paleta de colores corporativa y utiliza las imágenes de producto generadas por IA (libros, *merchandising*) para crear un ambiente *acogedor* y elegante.
* **Funcionalidad Clave (Interactividad):** La sección de "Colecciones" es interactiva. Al navegar por las cubiertas de las ediciones especiales, **el usuario puede hacer clic en la portada de cualquier libro. Al hacerlo, se despliega una ventana modal (pop-up) que muestra la sinopsis del libro**, una breve biografía del autor y detalles de la edición (textura de la tapa, detalles dorados, etc.). Esta interacción invita a la exploración y profundiza en la experiencia de "descubrir" un nuevo libro.


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

        /* Nuevo Trozo: Estilos para la ventana modal (emergente) */
        .modal {
            display: none;
            /* Oculto por defecto */
            position: fixed;
            /* Posición fija en la pantalla */
            z-index: 1;
            /* Por encima de todo */
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.6);
            /* Fondo semi-transparente oscuro */
        }

        .modal-content {
            background-color: #D7ACC4;
            /* Color de fondo de la web */
            margin: 10% auto;
            /* 10% desde arriba y centrado */
            padding: 30px;
            border: 3px solid #8F4242;
            /* Borde con el color del header */
            width: 80%;
            max-width: 600px;
            border-radius: 10px;
            position: relative;
            color: #6A4641;
            /* Color de texto principal de la web */
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .modal-content h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8em;
            color: #8F4242;
            /* Color del header */
            border-bottom: 2px solid #6A4641;
            padding-bottom: 10px;
            margin-top: 0;
        }

        .close-button {
            color: #8F4242;
            float: right;
            font-size: 35px;
            font-weight: bold;
            line-height: 20px;
        }

        .close-button:hover,
        .close-button:focus {
            color: #6A4641;
            text-decoration: none;
            cursor: pointer;
        }

        /* Fin del Nuevo Trozo de Estilos */
    </style>
</head>

<body>

    <header>
        <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Logo.png"
            alt="Books Nest Logo">
        <nav>
            <a href="#">Inicio</a>
            <a href="#productos">Productos</a>
            <a href="#libros">Libros</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <section class="section" id="video">
        <h2>Vídeo Destacado</h2>
        <div style="text-align: center; margin-bottom: 20px;">
            <iframe width="560" height="315" src="https://www.youtube.com/embed/yDePbmAqFKg"
                title="YouTube video player" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                allowfullscreen></iframe>
        </div>
        <p style="text-align: center;">Encuentra más sobre nuestros clásicos aquí: <a
                href="https://www.youtube.com/watch?v=yDePbmAqFKg" target="_blank"
                style="color: #8F4242; text-decoration: none; font-weight: bold;">Ver en YouTube</a></p>
    </section>

    <section class="section" id="productos">
        <h2>Productos destacados</h2>
        <div class="grid">
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Tazas.png"
                    alt="Tazas literarias">
                <h3>Tazas literarias</h3>
                <p>Diseños inspirados en clásicos y frases de autores.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Termos.png"
                    alt="Termos Books Nest">
                <h3>Termos grandes y pequeños</h3>
                <p>Perfectos para acompañar tus lecturas.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Bags.png"
                    alt="Tote Bags">
                <h3>Tote Bags</h3>
                <p>Ilustraciones literarias y colores cálidos.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Cuadernos.png"
                    alt="Cuadernos">
                <h3>Cuadernos</h3>
                <p>Para escribir tus ideas, sueños y relatos.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Pines.png"
                    alt="Pines esmaltados">
                <h3>Pines esmaltados</h3>
                <p>Pequeñas joyas literarias para coleccionar.</p>
            </div>
            <div class="card">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Caja.png"
                    alt="Cajas regalo">
                <h3>Cajas regalo</h3>
                <p>Libros, velas y detalles para lectores apasionados.</p>
            </div>
        </div>
    </section>

    <section class="section" id="libros">
        <h2>Libros que amamos</h2>
        <div class="grid">

            <div class="card" onclick="openModal('modalOrgullo')">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/OrgulloYPrejuicio.png"
                    alt="Orgullo y Prejuicio">
                <h3>Orgullo y Prejuicio</h3>
                <p>Jane Austen</p>
            </div>

            <div class="card" onclick="openModal('modalAlicia')">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/AliciaEnElPaisDeLasMaravillas.png"
                    alt="Alicia">
                <h3>Alicia en el País de las Maravillas</h3>
                <p>Lewis Carroll</p>
            </div>

            <div class="card" onclick="openModal('modalArturo')">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/Arturo.png"
                    alt="Arturo">
                <h3>Arturo</h3>
                <p>La leyenda del Rey Arturo</p>
            </div>

            <div class="card" onclick="openModal('modalJardin')">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/ElJardinSecreto.png"
                    alt="El jardín secreto">
                <h3>El jardín secreto</h3>
                <p>Frances Hodgson Burnett</p>
            </div>

            <div class="card" onclick="openModal('modalCumbres')">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/CumbresBorrascosas.png"
                    alt="Cumbres borrascosas">
                <h3>Cumbres borrascosas</h3>
                <p>Emily Brontë</p>
            </div>

            <div class="card" onclick="openModal('modalIsla')">
                <img src="https://raw.githubusercontent.com/NuriaRodriguezPardo/IAVA/refs/heads/main/Proyecto/Fotos/LaIslaDelTesoro.png"
                    alt="La isla del tesoro">
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

    <div id="modalAlicia" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3>Alicia en el País de las Maravillas</h3>
            <p id="sinopsisAlicia">
                Comienza con Alicia, una joven soñadora y curiosa, sentada aburrida junto a su hermana a la orilla de un
                río. De repente, su atención es capturada por un apurado Conejo Blanco que pasa corriendo, vestido con
                chaleco, consultando un reloj de bolsillo y lamentándose: "¡Dios mío! ¡Voy a llegar tarde!".
                Impulsada por la curiosidad, Alicia sigue al Conejo Blanco hasta una madriguera, en la que cae de forma
                inesperada. Tras una larguísima caída, aterriza en una sala con muchas puertas. Encuentra una pequeña
                llave dorada y, tras beber el contenido de una botella etiquetada como "BÉBEME" y comer un pastelito que
                dice "CÓMEME", experimenta una serie de transformaciones de tamaño. Sus cambios de estatura, que van
                desde gigante hasta minúscula, la llevan a derramar un charco de lágrimas tan grande que casi se ahoga
                en él.
                En el charco, Alicia se encuentra con un Ratón y otras criaturas empapadas, incluyendo un Dodo, un Loro
                y un Águila. Para secarse, el Dodo organiza una "Carrera Loca", sin reglas ni principio ni fin, donde
                todos ganan.
                Sus aventuras la llevan luego a la casa del Conejo Blanco, donde vuelve a crecer peligrosamente,
                quedando atascada hasta que logra encogerse de nuevo y escapar. Después de deambular por el bosque, se
                topa con una Oruga azul fumando narguile sobre una seta. La Oruga la desafía a reflexionar sobre su
                identidad y le muestra cómo usar el hongo (comiendo de un lado para crecer y del otro para encoger) para
                controlar su tamaño.
                Alicia usa el hongo para alcanzar una estatura normal y entra en una casa donde conoce a la Duquesa, una
                mujer que maltrata a su bebé y cocina una sopa con demasiada pimienta, y al famoso Gato de Cheshire, una
                criatura sonriente que puede desaparecer dejando solo su sonrisa en el aire. El Gato le aconseja sobre
                la gente de Wonderland y la dirige hacia el Sombrerero Loco.
                Llega al jardín donde se está celebrando la infame Merienda de Locos, un encuentro eterno y sin sentido
                con el Sombrerero Loco, la Liebre de Marzo y el Lirón dormido, donde el tiempo se ha detenido y los
                participantes se dedican a acertijos sin respuesta y a cambiar de sitio sin cesar.
                Harta de la locura de la fiesta, Alicia entra en un hermoso jardín que resulta ser el dominio de la
                tiránica Reina de Corazones. La Reina es una figura temible que grita "¡Que le corten la cabeza!" ante
                la menor ofensa. Alicia presencia un surrealista juego de cróquet, donde los mazos son flamencos, las
                pelotas son erizos y los arcos son naipes que se doblan.
                La Reina la presenta a la Falsa Tortuga y al Grifo, quienes le cuentan historias de una educación
                extravagante y le enseñan el "Baile de la Langosta".
                Finalmente, Alicia es arrastrada a un juicio ridículo e injusto. La Sota de Corazones es acusada de
                robar las tartas de la Reina, pero el juicio se lleva a cabo sin ninguna lógica. El Sombrerero Loco y la
                Duquesa son llamados como testigos, ofreciendo testimonios absurdos. Alicia, que ha vuelto a crecer
                hasta su tamaño normal, ya no soporta más la falta de sentido. Cuando la Reina, en medio de la confusión
                de las "pruebas", ordena: "¡Sentencia primero, veredicto después!", Alicia se rebela y la desafía,
                gritando que no son más que un mazo de cartas.
                Al instante, todas las cartas se elevan y se abalanzan sobre ella. Alicia despierta de golpe, dándose
                cuenta de que está de vuelta junto a su hermana, que suavemente le sacude las hojas de la cara. El País
                de las Maravillas no era más que un largo y vívido sueño, y la historia concluye con la hermana de
                Alicia imaginando cómo Alicia, en el futuro, conservará la sencillez y el entusiasmo de su niñez al
                contar a otros niños sus fantásticas aventuras.
            </p>
        </div>
    </div>

    <div id="modalOrgullo" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3>Orgullo y Prejuicio</h3>
            <p id="sinopsisOrgullo">
                Orgullo y Prejuicio, de Jane Austen, se desarrolla en la campiña inglesa de principios del siglo XIX y
                se centra en la vida de la familia Bennet, con sus cinco hijas casaderas: la hermosa y dulce Jane, la
                ingeniosa y vivaz Elizabeth (Lizzy), la estudiosa Mary, y las frívolas Kitty y Lydia. La señora Bennet,
                una mujer cuyo único propósito en la vida es casar a sus hijas, ve una oportunidad de oro con la llegada
                de Charles Bingley, un joven, rico y apuesto soltero que alquila la mansión vecina de Netherfield Park.
                La primera gran reunión social, un baile, establece el eje central de la trama. Bingley se siente
                inmediatamente atraído por la belleza y el carácter de Jane Bennet. Con Bingley llega su íntimo amigo,
                Fitzwilliam Darcy, un hombre aún más rico, de porte aristocrático, pero con un semblante de superioridad
                y una reserva que lo hacen parecer orgulloso y arrogante. Darcy menosprecia a la sociedad rural
                circundante e insulta directamente a Elizabeth al negarse a bailar con ella, declarando que "no está
                mal, aunque no es lo bastante guapa como para tentarme". Este incidente siembra la prevención
                (prejuicio) en Elizabeth contra Darcy, convencida de que es el hombre más desagradable del mundo.
                La tensión aumenta con la llegada del carismático y encantador oficial George Wickham, quien rápidamente
                se gana la simpatía de Elizabeth. Wickham le cuenta a Elizabeth una historia de infortunio, alegando que
                Darcy lo despojó de una herencia prometida por el padre de Darcy. Elizabeth, ya predispuesta contra
                Darcy, cree ciegamente esta versión, reforzando su prejuicio.
                La felicidad de Jane y Bingley se ve truncada cuando, de repente, Bingley y sus hermanas (que
                desaprueban a la familia Bennet) abandonan Netherfield sin previo aviso. Elizabeth está convencida de
                que Darcy y la hermana de Bingley, Caroline, han conspirado para separarlos.
                Posteriormente, Elizabeth recibe una sorprendente propuesta de matrimonio de Darcy. Elizabeth rechaza la
                propuesta con vehemencia, acusándolo de haber arruinado la felicidad de Jane al separarla de Bingley y
                de haber tratado cruelmente a Wickham.
                Al día siguiente, Darcy le entrega a Elizabeth una carta crucial. En ella, explica dos verdades que
                sacuden el mundo de Elizabeth. En primer lugar, confirma su intervención para separar a Jane y Bingley,
                pero lo justifica por creer sinceramente que el afecto de Jane no era lo suficientemente fuerte para el
                de su amigo, y a causa del comportamiento impropio de la familia Bennet. En segundo lugar, revela que
                Wickham es un libertino sin escrúpulos. Wickham, lejos de ser la víctima, intentó huir con Georgiana, la
                hermana menor de Darcy, para robar su fortuna. Elizabeth se da cuenta de que ha juzgado a Darcy
                (orgullo) y a Wickham (prejuicio) de forma totalmente errónea.
                El viaje de Elizabeth a la gran propiedad de Darcy en Derbyshire, Pemberley, marca el inicio de su
                cambio de opinión. Allí, el trato amable de Darcy hacia su familia y la lealtad de sus sirvientes le
                muestran una cara totalmente distinta del hombre. Este proceso se interrumpe con la noticia del
                escándalo: Lydia, la hermana menor e irresponsable, se ha fugado con Wickham, sin intención de casarse.
                Esto supone la ruina social y económica para toda la familia Bennet.
                Elizabeth descubre con asombro que Darcy fue quien encontró a la pareja en Londres, pagó las deudas de
                Wickham y lo sobornó para que se casara con Lydia, salvando así el honor de la familia Bennet. Darcy
                hizo todo esto en secreto, movido por el amor hacia Elizabeth y el sentimiento de culpa por no haber
                expuesto antes la vileza de Wickham.
                Finalmente, la llegada de Lady Catherine de Bourgh, la orgullosa tía de Darcy, a Longbourn para exigirle
                a Elizabeth que rechace a su sobrino y prometa no casarse con él, sella el destino de la pareja.
                Elizabeth se niega rotundamente a someterse al dictado de Lady Catherine. Su firmeza da esperanzas a
                Darcy, quien malinterpretó la anterior negativa de Elizabeth. Bingley y Jane se han reconciliado y se
                comprometen.
                Darcy vuelve a proponerle matrimonio a Elizabeth, esta vez con humildad, habiendo superado su orgullo
                social. Elizabeth, habiendo superado su prejuicio inicial y entendiendo el verdadero noble carácter de
                Darcy, acepta su propuesta. La novela concluye con el matrimonio de ambas parejas, un final feliz que
                representa el triunfo del verdadero amor sobre la presunción, el orgullo de clase y el juicio
                apresurado.
            </p>
        </div>
    </div>

    <div id="modalArturo" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3>El Rey Arturo y los Caballeros de la Mesa Redonda</h3>
            <p id="sinopsisArturo">
                El libro narra la historia del Rey Arturo y el origen de su legendario reino, comenzando con sus padres.
                La historia se inicia con el Rey Uther Pendragon, que se enamora perdidamente de Igraine, la esposa del
                poderoso Duque de Cornualles. Ante el temor de ser deshonrada, Igraine y su esposo huyen secretamente.
                Airado, Uther les declara la guerra y sitia el castillo de Terrabil.
                Enfermo de amor y rabia, Uther es asistido por Merlín, quien accede a usar magia para que el rey pueda
                yacer con Igraine, con la condición de que el niño nacido sea entregado a Merlín para su crianza. Merlín
                transforma a Uther para que tenga la apariencia del Duque y, esa misma noche, Uther engendra a Arturo.
                Merlín, cumpliendo la promesa, se lleva al bebé y lo entrega a Sir Héctor, un noble fiel, para que su
                esposa lo críe. El niño es bautizado con el nombre de Arturo.
                Dos años después, el Rey Uther cae gravemente enfermo, y en su lecho de muerte, gracias a Merlín,
                declara que su hijo Arturo deberá ser el legítimo rey de Inglaterra.
                Tras la muerte de Uther, el reino cae en desorden, pues muchos nobles quieren la corona. Merlín aconseja
                al Arzobispo de Canterbury que reúna a todos los nobles en Londres en Navidad, para que Dios revelase al
                verdadero rey mediante un milagro. En el patio de la iglesia aparece una gran piedra de mármol con un
                yunque de acero incrustado, del cual sobresale una espada. La inscripción declara que quien saque la
                espada es el rey legítimo de toda Inglaterra. Ninguno de los nobles logra mover la espada.
                Durante un torneo, el joven Arturo, que fue criado como el hijo de Sir Héctor y hermano de leche de Sir
                Kay, saca la espada fácilmente de la piedra, al ir a buscar una espada para su hermano. Sir Kay intenta
                mentir diciendo que él la sacó, pero la verdad se revela. Sir Héctor confiesa a Arturo que él no es su
                verdadero padre, sino que fue encomendado a él por Merlín. Arturo se entristece, pero promete a Sir Kay
                que lo nombrará senescal.
                La prueba de la espada es aplazada hasta Pentecostés debido a que muchos nobles se enfurecen al ser
                gobernados por un joven de origen incierto. Finalmente, en Pentecostés, cuando nadie más puede sacarla
                excepto Arturo, el pueblo clama que acepte el trono, pues ven la voluntad de Dios en el milagro. Arturo
                es coronado rey, jura mantener la justicia y comienza a restaurar el orden y las tierras a sus dueños
                legítimos. Nombra a Sir Kay senescal y a otros caballeros leales en altos cargos.
                El reinado de Arturo comienza con una guerra contra once reyes rebeldes, como el Rey Lot y el Rey
                Uriens, que se niegan a reconocerlo. Aconsejado por Merlín, Arturo busca la alianza del Rey Ban de
                Benwick y el Rey Bors de Gaula (Francia), dos reyes poderosos que luchan contra el Rey Claudas. Arturo
                promete ayudarles en sus guerras si ellos le asisten a él. Unidos, Arturo y sus aliados se enfrentan a
                los once reyes en una dura batalla.
                Más adelante en la historia, Arturo obtiene la espada Excalibur y su vaina, que tiene propiedades
                curativas. El rey Arturo se casa con Ginebra, hija del Rey Leodegrance de Camelerd. Como regalo de
                bodas, Leodegrance le entrega la famosa Tabla Redonda, que tiene capacidad para ciento cincuenta
                caballeros. El libro relata cómo, gracias al consejo de Merlín y a la proeza de sus caballeros, Arturo
                se consolida como rey y se enfrenta a amenazas externas, como los mensajeros que le exigen tributo en
                nombre del emperador Lucio de Roma. La narración continúa con las hazañas de sus caballeros, como Sir
                Lanzarote del Lago, que se convierte en el caballero de mayor renombre en el mundo.
            </p>
        </div>
    </div>

    <div id="modalJardin" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3>El Jardín Secreto</h3>
            <p id="sinopsisJardin">
                La novela comienza en la India con Mary Lennox, una niña de nueve años, descrita como desagradable,
                delgada y pálida, fruto de unos padres negligentes que la dejaron al cuidado de sirvientes. Después de
                que una epidemia de cólera mate a sus padres y a su aya, y que el resto de sirvientes huya, Mary queda
                completamente sola y olvidada en la casa.
                Mary es enviada a Inglaterra para vivir con su único pariente vivo, su tío Archibald Craven, en la
                inmensa y desolada mansión de Misselthwaite Manor en Yorkshire. Su tío es un hombre jorobado,
                melancólico, que vive recluido en un ala de la casa y pasa la mayor parte del tiempo viajando, incapaz
                de superar la muerte de su amada esposa, diez años atrás.
                La señora Medlock, el ama de llaves, informa a Mary de que la casa tiene casi cien habitaciones, la
                mayoría cerradas, y le advierte que debe jugar sola y que no debe deambular por la casa. Mary se siente
                más sola que nunca, explorando el gran parque que rodea la casa. Allí conoce a la amable doncella Martha
                Sowerby, quien le habla sobre su hermano Dickon, un muchacho dulce que convive en armonía con los
                animales del páramo.
                A través de Martha y el jardinero Ben Weatherstaff, Mary se entera de la existencia de un jardín
                especial, amado por la señora Craven, que fue cerrado con llave por su tío y cuya llave fue enterrada
                tras la muerte de su esposa hace diez años. Nadie ha entrado en él desde entonces. Este misterio
                obsesiona a Mary.
                Un día, con la ayuda de un petirrojo, Mary encuentra la llave del jardín secreto y, poco después,
                descubre la puerta oculta bajo una cortina de hiedra. Al entrar, encuentra un lugar encantador y
                misterioso, lleno de rosas, pero descuidado y salvaje.
                Poco después, Mary conoce a Dickon, el hermano de Martha, quien la ayuda con los preparativos para que
                el jardín reviva, plantando y cuidando los bulbos y las rosas. El trabajo físico y el aire fresco de
                Yorkshire transforman a Mary, que deja de ser la niña enfermiza y desagradable de la India.
                Una noche, Mary escucha un llanto que le parece venir de alguien perdido. Siguiendo el sonido, descubre
                al fin al misterioso Colin Craven, su primo, en una habitación del ala oeste. Colin es un niño postrado
                en cama, con la creencia de que es un inválido con una protuberancia en la espalda y que morirá pronto.
                Es caprichoso, tiránico y ha mantenido a todos en la casa a su merced con sus rabietas.
                Mary, sin temor, le habla con franqueza y le revela la existencia del jardín secreto, atrayendo su
                enorme curiosidad. Los dos niños se hacen amigos, y Mary, convencida de que el aire y la "magia" del
                jardín pueden curarlo, y de que su presunta enfermedad es en gran parte psicosomática, planea la visita.
                Finalmente, Mary y Dickon llevan a Colin en secreto al jardín. Al experimentar por primera vez la
                primavera, el sol, los animales y el trabajo en la naturaleza, Colin siente un poder vivificante y se
                pone de pie, descubriendo que no tiene ninguna joroba y que no está enfermo. Colin decide guardar su
                recuperación en secreto de todos, especialmente de su padre, para sorprenderlo con un "descubrimiento
                científico".
                Meses después, el señor Craven, que ha estado viajando, siente un impulso irresistible que lo lleva de
                vuelta a Misselthwaite Manor y al muro cubierto de hiedra. Mientras camina cerca, escucha el sonido de
                voces y pasos rápidos. De repente, la puerta del jardín se abre y ve a Colin, sano y radiante, corriendo
                a su encuentro.
                El libro concluye con el señor Craven y su hijo caminando juntos hacia la casa. La curación de Colin y
                la reactivación del jardín secreto simbolizan la sanación emocional y física de toda la familia y la
                mansión, que pasa del luto y la desolación a la alegría y la vida.
            </p>
        </div>
    </div>

    <div id="modalCumbres" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3>Cumbres Borrascosas</h3>
            <p id="sinopsisCumbres">
                La novela, narrada principalmente a través de la perspectiva del ama de llaves Ellen "Nelly" Dean al
                señor Lockwood, el nuevo inquilino de la Granja de los Tordos, es un relato gótico y apasionado sobre el
                amor destructivo y la venganza.
                La historia se centra en dos propiedades vecinas en los páramos de Yorkshire: la casa señorial, pero
                austera, de Cumbres Borrascosas (Wuthering Heights) y la más civilizada y cómoda Granja de los Tordos
                (Thrushcross Grange).
                La tragedia comienza cuando el señor Earnshaw, dueño de Cumbres Borrascosas, trae a casa a un niño
                gitano huérfano y harapiento de las calles de Liverpool, al que llama Heathcliff. El niño es aceptado
                por la joven Catherine Earnshaw, pero es recibido con resentimiento por su hermano mayor, Hindley.
                A medida que crecen, Heathcliff y Catherine desarrollan un vínculo amoroso salvaje, profundo y
                simbiótico, que trasciende la simple pasión y se convierte en la esencia misma de sus vidas. Corren
                libres por el páramo, ajenos a las restricciones sociales de la casa. Sin embargo, su relación se ve
                alterada cuando Hindley, tras la muerte de su padre, hereda la propiedad y, cegado por los celos y el
                alcohol, degrada a Heathcliff a la posición de sirviente, negándole educación.
                Catherine sufre un accidente cerca de la Granja de los Tordos y pasa cinco semanas convaleciente con los
                refinados hermanos Edgar e Isabella Linton. Al regresar, su naturaleza se ha dividido: está fascinada
                por la civilización y el estatus que ofrecen los Linton, pero su corazón sigue unido a Heathcliff.
                En una escena crucial, Catherine confiesa a Nelly Dean que, aunque ama a Heathcliff con todo su ser ("Yo
                soy Heathcliff"), no puede casarse con él porque sería degradante desde el punto de vista social.
                Heathcliff escucha esta confesión de forma parcial y, humillado, huye de Cumbres Borrascosas en una
                noche de tormenta, sin escuchar la parte en la que Catherine afirma que su amor es incondicional y
                eterno.
                Tres años después, Catherine se casa con Edgar Linton. Poco después, Heathcliff regresa, ahora rico,
                educado y con una apariencia imponente, pero lleno de un amargo deseo de venganza.
                Heathcliff ejecuta un plan frío y metódico para destruir a quienes considera responsables de su
                sufrimiento. Primero, toma venganza sobre Hindley, que se ha hundido en el vicio tras la muerte de su
                esposa, ganándole sus deudas de juego y, en última instancia, apoderándose de Cumbres Borrascosas.
                Luego, se casa con la ingenua Isabella Linton solo para atormentarla y deshonrar a Edgar, su cuñado.
                La tensión entre Catherine, Edgar y Heathcliff alcanza un punto insostenible. El amor incontrolable de
                Catherine por Heathcliff y su incapacidad para conciliar su pasión con su estatus social la llevan a un
                colapso. Muere al dar a luz a su hija, Cathy Linton. La muerte de Catherine destroza a Heathcliff, que
                suplica a su espíritu que lo atormente por el resto de su vida y que no lo deje solo.
                La segunda mitad de la novela se centra en la siguiente generación. Heathcliff obliga a su hijo
                enfermizo, Linton Heathcliff (hijo de Isabella y él), a casarse con su prima Cathy Linton (hija de
                Catherine y Edgar) para asegurarse de heredar la Granja de los Tordos. Tras la muerte de los dos Linton
                y del joven Linton Heathcliff, Heathcliff posee ambas propiedades.
                El círculo de la venganza parece completo. Sin embargo, Hareton Earnshaw (el hijo de Hindley), a quien
                Heathcliff ha degradado y mantenido en la ignorancia como venganza contra su padre, y Cathy Linton, se
                enamoran gradualmente a pesar de sus diferencias.
                El agotado y obsesivo Heathcliff, al ver la profunda semejanza entre la joven Cathy y la Catherine que
                amó, pierde finalmente su deseo de vivir y de vengarse. Su única meta es reunirse con el fantasma de
                Catherine, y su salud se deteriora hasta que es encontrado muerto en la cama de su amada.
                La novela concluye con el matrimonio planificado de Cathy Linton y Hareton Earnshaw, que simboliza la
                curación y la restauración de la paz en las casas, y con Lockwood visitando las tumbas de Catherine,
                Heathcliff y Edgar, y preguntándose cómo alguien podría imaginarlos "inquietos" en ese páramo sereno y
                apacible.
            </p>
        </div>
    </div>

    <div id="modalIsla" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <h3>La Isla del Tesoro</h3>
            <p id="sinopsisIsla">
                La historia, narrada por el joven Jim Hawkins, comienza en la hostería "Almirante Benbow" en la costa de
                Inglaterra, propiedad de los padres de Jim. La tranquilidad se rompe con la llegada de un viejo y
                siniestro marinero llamado Billy Bones, que se instala allí para beber ron y esperar la llegada de otros
                piratas. Billy Bones, un antiguo primer oficial del famoso Capitán Flint, posee un misterioso mapa.
                La presencia de Bones atrae a otros piratas, como el tullido "Perro Negro" y el ciego y amenazante
                "Pew". Tras la muerte repentina de Billy Bones, a causa de un ataque de apoplejía (provocado por un
                shock tras recibir la "Mancha Negra", la citación pirata a juicio), Jim y su madre huyen con el
                contenido del cofre de Bones, que incluye dinero, un diario y el codiciado mapa del tesoro del Capitán
                Flint.
                Jim lleva el mapa a los caballeros locales: el doctor Livesey y el terrateniente Squire Trelawney. Al
                ver el mapa que marca la ubicación del inmenso tesoro de Flint en una isla remota, deciden organizar una
                expedición. Trelawney se encarga de equipar un barco, la goleta Hispaniola, y de contratar una
                tripulación en Bristol.
                Trelawney comete un error fatal al confiar demasiado en un cocinero de un solo pie llamado Long John
                Silver, que se presenta como un hombre honrado. Sin el conocimiento de los caballeros, Silver es el
                antiguo contramaestre de Flint y ha reunido en secreto a una gran parte de la tripulación con el
                propósito de amotinarse y robar el tesoro.
                Jim se embarca en la Hispaniola como grumete. Poco antes de llegar a su destino, y escondido en un
                barril de manzanas, Jim escucha una conversación entre Silver y varios marineros, en la que revelan su
                plan de motín, que consiste en esperar a que los caballeros encuentren el tesoro para luego asesinarlos
                y huir con la fortuna.
                Jim advierte inmediatamente a Livesey, Trelawney y al Capitán Smollett. Deciden mantener la calma y
                simular ignorancia hasta que sea el momento oportuno. Al llegar a la isla, el Capitán Smollett logra
                enviar al grupo de traidores a tierra bajo un pretexto, dejando a Jim y a sus aliados en una posición
                ventajosa.
                El motín estalla. Jim, al desembarcar, se separa del grupo principal y es testigo del asesinato de un
                marinero leal. Huyendo por el bosque, Jim se encuentra con un náufrago: Ben Gunn, un exmiembro de la
                tripulación de Flint, abandonado en la isla tres años atrás y que vive casi enloquecido por la soledad.
                Gunn se ofrece a ayudar a Jim a cambio de un pasaje de vuelta a casa y una parte del tesoro.
                Mientras tanto, el grupo leal se atrinchera en un fuerte de madera en la isla. Se libra una breve pero
                violenta batalla. Jim, en un acto de valentía impulsiva, regresa al barco y lo lleva a un escondite
                seguro, dejando a los piratas varados en la orilla. Incluso se enfrenta y derrota al timonel Israel
                Hands.
                Cuando Jim regresa al fuerte, descubre que el doctor Livesey ha cedido el mapa a Long John Silver a
                cambio de un acuerdo para que la tripulación leal pueda abandonar la isla. Los piratas, con Silver a la
                cabeza, se adentran en la isla siguiendo el mapa, llevándose a Jim como rehén.
                El clímax ocurre cuando llegan al lugar marcado, solo para encontrar que el tesoro ha sido desenterrado
                y robado. Los piratas se vuelven contra Silver, pero son emboscados y dispersados por el doctor Livesey,
                Ben Gunn y el Capitán Smollett. En un giro sorprendente, se revela que Ben Gunn había encontrado el
                tesoro de Flint y lo había trasladado a su cueva.
                Con el tesoro a salvo, los supervivientes se reúnen. Cargan el oro y la plata en el Hispaniola. Long
                John Silver, a pesar de sus crímenes, demuestra habilidad al ayudar en el viaje de vuelta, escapando
                finalmente con una pequeña parte del tesoro en una escala en América, con la connivencia de Jim.
                La historia termina con Jim, Trelawney, Livesey y Smollett regresando a Inglaterra, ricos y victoriosos,
                aunque con la promesa de Jim de que nunca volverá a la isla. El tesoro restante de Flint sigue
                enterrado.
            </p>
        </div>
    </div>

</body>

</html>

<script>
    // Función para abrir el modal
    function openModal(modalId) {
        document.getElementById(modalId).style.display = "block";
    }

    // Obtener todos los botones de cierre
    var closeButtons = document.querySelectorAll(".close-button");

    // Recorrer los botones y añadir el evento para cerrar el modal
    closeButtons.forEach(function (button) {
        button.onclick = function () {
            var modal = button.closest('.modal');
            modal.style.display = "none";
        }
    });

    // Cerrar el modal si el usuario hace clic fuera de él
    window.onclick = function (event) {
        if (event.target.classList.contains('modal')) {
            event.target.style.display = "none";
        }
    }
</script>
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

| Color | Hex | Descripción |
| :--- | :--- | :--- |
| Rosa suave | `#D7ACC4` | Aporta calidez, delicadeza y un toque romántico. |
| Terracota claro | `#D6B1A5` | Tono tierra, natural, artesanal y acogedor. |
| Verde grisáceo | `#738886` | Aporta seriedad, elegancia y un toque orgánico/natural. |
| Rojo profundo | `#8F4242` | Color de la pasión, el drama y la literatura clásica (como tapas de libros antiguos). |
| Marrón oscuro | `#6A4641` | Aporta profundidad, estabilidad y una sensación de madera o cuero. |

## Conclusión

El proyecto **Books Nest** combina creatividad, tecnología e inspiración para dar vida a una marca editorial que valora la emoción detrás de cada historia.
