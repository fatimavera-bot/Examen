
# BAUHAUS DIGITAL: Sistema Visual Interactivo
**Autor:** Fatima Alexia Vera Navarrete            
**Profesora:** Sofía Suazo             
**Asignatura:** Pensamiento Computacional              
**Examen Final** - Escuela de Diseño UDP          

---

##  Enlaces del Proyecto
**Link público para ejecutar el proyecto**(https://editor.p5js.org/fatima.vera/full/ZBB3iKDFj)
**Link editable para revisar el código**(https://editor.p5js.org/fatima.vera/sketches/ZBB3iKDFj)

---

##  Descripción General

### Descripción Objetiva
**Bauhaus Digital** Es un sistema visual e interactivo desarrollado en p5.js. El usuario se encuentra inicialmente con una pantalla de bienvenida que introduce los comandos. Al interactuar con el teclado, puede acceder a dos escenas dinámicas: una grilla geométrica que reconfigura su cantidad de columnas y filas mediante el movimiento del mouse, y un estudio de color con círculos concéntricos y un triángulo interactivo. El sistema genera respuestas visuales en tiempo real y modula frecuencias de audio el cual cambia segun las acciones del usuario.

### Descripción Conceptual
* **Idea Central:** Traducir los principios de la escuela Bauhaus a un entorno digital algorítmico, donde las formas y los colores no son estáticos, sino variables controladas por lógica matemática e interactiva.
* **Corriente o Referente de Diseño:** La escuela **Bauhaus** (particularmente inspirada en los talleres de pintura abstracta y teoría del color de Vasili Kandinsky y Johannes Itten).
* **Principio de Diseño Explorado:** La síntesis geométrica, el uso de la paleta de colores primarios oficiales (rojo, azul, amarillo, blanco/crema y negro) y la relación entre forma, color y sonido (sinestesia).

---

##  Sistema Computacional

El proyecto se comporta como un sistema cerrado que procesa entradas para generar transformaciones en los estados visuales y sonoros:

* **Inputs:**
    * Posición del mouse en los ejes X e Y (mouseX, mouseY).
    * Eventos de teclado (Teclas A, S, E).
    * Click sostenido del mouse (mouseIsPressed).
* **Procesos:**
    * Mapeo continuo (map()) de la posición del mouse para calcular la densidad de filas/columnas y el tamaño de las figuras.
    * Cálculo de alternancia geométrica (operador residuo %) para intercalar cuadrados, círculos y colores.
    * Cálculo del desplazamiento vertical infinito basado en el frameCount.
    * Generación de desfases mediante random() al hacer click.
* **Estados del Sistema:**
    * Estado 0: Pantalla de inicio (Presentación del afiche estático e instrucciones).
    * Estado 1: Grilla Bauhaus (Composición modular interactiva en movimiento continuo).
    * Estado 2: Estudio de Color y Forma (Exploración geométrica concéntrica y sinestésica).
* **Eventos:**
    * Presionar A o a: Transiciona al Estado 1.
    * Presionar S o s: Transiciona al Estado 2.
    * Presionar E o e: Retorna al Estado 0.
    * Hacer click con el mouse: Activa el factor aleatorio en el Estado 2.
* **Outputs:**
    * **Visual:** Renderizado reactivo en el lienzo (canvas) de formas geométricas en movimiento y textos dinámicos.
    * **Sonoro:** Onda de audio sintetizada (tipo triángulo) cuya frecuencia e intensidad varían según la posición e interacción del cursor.

---

##  Diagrama de Flujo

A continuación se presenta el mapa lógico del sistema que describe las transiciones de los estados, procesos y decisiones del código:

![Diagrama de Flujo del Sistema](./diagrama_flujo.png) 
*(Nota: Asegúrate de subir tu imagen del diagrama en Figma con el nombre "diagrama_flujo.png" en la misma carpeta de GitHub para que se visualice aquí).*

---

##  Recursos Multimedia Utilizados

* **Tipo de recurso:** Audio Sintetizado (p5.Oscillator de tipo triangle).
* **Función dentro del proyecto:** Actúa como un puente sinestésico que reacciona a la interacción del usuario. No es un elemento decorativo; su frecuencia está directamente amarrada a la posición de las formas del sistema (`mouseX` y el tamaño del triángulo). En el Estado 0 permanece apagado para respetar la estructura de la interfaz, y se enciende en las experiencias interactivas.

---

##  Registro Visual y Proceso

### Bocetos e Ideas Iniciales
*Aquí puedes describir brevemente cómo pensaste la grilla o las formas en papel antes de pasarlas a código.*

### Capturas del Proceso
*(Inserta capturas de pantalla de tus estados aquí)*
* **Pantalla de Inicio:** ¡Interfaz limpia inspirada en los afiches de Weimar!
* **Grilla Interactiva:** Demostración del cambio en la matriz geométrica.

---

##  Reflexión Final

* **Principales decisiones tomadas:** Decidi implementar un control de estados estricto mediante el teclado para permitir una navegación fluida. También se opte por un oscilador de onda triangular a volumen muy bajo (0.01) En el estado 1 y un volumen de (0.03) en el estado 2 para generar una atmósfera sonora interactiva pero sutil en la que, del estado 1 al estado 2 haya una subida del volumen, queriendo evidenciar la transición tambien de manera auditiva.
* **Dificultades encontradas:** Lograr que los elementos de la grilla bajaran y subieran de manera infinita sin salirse del margen del afiche inferior requirió calibrar correctamente el operador matemático de residuo con el `height`.
* **Aprendizajes obtenidos:**Entendí mejor la programación orientada a estados en p5.js, comprendi cómo un mismo software puede cambiar radicalmente su comportamiento y su lógica de interacción en base a variables globales de control.
