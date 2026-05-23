# Bauhaus en movimiento

## 1. Información del Proyecto

* **Nombre del proyecto:** Bauhaus en movimiento
* **Autora:** Fatima Alexia Vera Navarrete

### Descripción objetiva

**Qué es el proyecto:**
El proyecto es un afiche interactivo y dinámico programado en p5.js que rinde homenaje a la estética de la escuela Bauhaus. Transforma la rigidez del diseño editorial clásico en un sistema visual generativo donde la geometría cobra vida a través del código.

**Qué se ve en pantalla:**
Se observa una composición vertical con un fondo de tono crema. Sobre este, se despliega una grilla estructurada por potentes diagonales negras en perspectiva que conviven con una serie de círculos y cuadrados de colores primarios que se desplazan de forma continua y fluida por el lienzo. En la parte inferior, una franja negra sólida corona el afiche con la inscripción centradamente tipográfica "Bauhaus inspiracion".

**Qué elementos visuales aparecen:**
* Cuadriláteros negros estirados (`quad`) que forman un patrón diagonal de fondo.
* Cuadrados (`rect`) que oscilan en tamaño y descienden continuamente.
* Círculos (`ellipse`) que ascienden de manera infinita por la pantalla.
* Paleta cromática oficial Bauhaus: Crema de fondo, negro carbón, rojo vibrante, azul profundo y amarillo cadmio.

**Qué inputs utiliza:**
* **Posición continua del mouse (`mouseX`, `mouseY`):** Utilizada como controlador dinámico para reconfigurar la densidad de la grilla del afiche.

**Qué outputs genera:**
* **Alteración de la matriz geométrica:** El cambio en tiempo real del número de columnas y filas que componen la estructura.
* **Animación e interpolación cinética:** Desplazamientos verticales autónomos infinitos gracias al uso de `frameCount` combinados con la función matemática de oscilación `sin()`.

---

## 2. Descripción Conceptual

### Idea central del proyecto
El proyecto explora la tensión entre el orden estricto de la Bauhaus y las infinitas posibilidades del arte generativo interactivo. Busca que un afiche histórico deje de ser una pieza estática de museo para convertirse en un organismo visual interactivo que se mueve según la interacción del espectador.

### Corriente o referente de diseño con el que dialoga
Dialoga directamente con el **Diseño Gráfico de la Bauhaus** (especialmente su época de consolidación geométrica en 1923) y las vertientes del **Arte Cinético digital**.

### Listado y breve descripción de referentes visuales
1. **Afiche de la Exposición de la Bauhaus de 1923 (Joost Schmidt):** De aquí se extrae la rigurosa retícula ortogonal, la potente sombra diagonal negra que genera relieve tridimensional y el uso estricto de colores primarios.
2. **Abstracción Geométrica Dinámica:** Influencia directa de las composiciones oblicuas y fluidas, donde los círculos rompen la estructura cuadriculada y adquieren una dirección libre, simulando una lluvia o estela de elementos puros en movimiento.

### Principio de diseño explorado
El principio de **Ritmo, Repetición y Contrapunto**. El algoritmo no replica una captura fija, sino que traduce las leyes de composición en un bucle matemático estructurado. Mientras las diagonales negras ofrecen un ritmo estático y predecible, las figuras de colores actúan como un contrapunto dinámico que altera la percepción espacial del lienzo.

---

## 3. Input / Output y Sistema


* **Regla de Densidad Dinámica:** La cantidad de columnas de la grilla se calcula dividiendo el ancho del lienzo entre un rango de 5 a 10 según la posición horizontal (`mouseX`) del cursor. Las filas se calculan entre 6 y 12 según la posición vertical ('mouseY').
* **Regla de Distribución Cromática:** Mediante una operación de residuo matemático (`(x + y) % 3`), el sistema garantiza un orden perfectamente equitativo para alternar los tres colores primarios (azul, rojo, amarillo) celda por celda sin amontonamientos.
* **Regla Cinética Inversa:** Los círculos ascienden a una velocidad constante basada en `frameCount * 1.5`, mientras que los cuadrados descienden de manera autónoma a `frameCount * 1.2`.
* **Regla de Escala Orgánica:** Los cuadrados alteran su tamaño de forma armónica utilizando la función trigonométrica `sin()`, simulando una respiración visual continua dentro de la rigidez geométrica.

### Explicación del sistema de interactividad
* **¿Qué datos entran?** Las coordenadas numéricas del cursor `mouseX` y `mouseY` actualizadas de forma continua frame por frame.
* **¿Cómo se procesan y transforman?** A través de la función `map()`, los pixeles brutos de la pantalla se normalizan y escalan a números enteros discretos que el sistema utiliza para definir el número de filas y columnas de la grilla.
* **¿Qué respuesta visual producen?** Al mover el cursor, la estructura del afiche se comprime o se expande armónicamente, modificando instantáneamente el tamaño de las celdas, redistribuyendo las figuras y transformando la escala tridimensional de todo el afiche.

---

## 4. Imágenes Referentes

<img width="236" height="334" alt="e29b96ad1f4ce795b45d7ef4c764dcbe" src="https://github.com/user-attachments/assets/287992bc-1699-49e5-a022-ae6f78bc41ec" />
<img width="564" height="564" alt="br-11134201-7qukw-ljyvjyxl13m258" src="https://github.com/user-attachments/assets/e63fb935-7f1c-4a3f-89a1-05726ddfe472" />



## 5. Ejecución del Proyecto

https://editor.p5js.org/fatima.vera/sketches/T5p9bVLgj
