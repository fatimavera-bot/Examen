# BAUHAUS DIGITAL: Sistema Visual Interactivo

**Autora:** Fatima Alexia Vera Navarrete                   
**Profesora:** Sofía Suazo                 
**Asignatura:** Pensamiento Computacional             
**Examen Final:** Escuela de Diseño UDP                 

---

## Enlaces del Proyecto

**Proyecto en pantalla completa** https://editor.p5js.org/fatima.vera/full/ZBB3iKDFj         
**Código en p5.js** ]https://editor.p5js.org/fatima.vera/sketches/ZBB3iKDFj

---

## Información del Proyecto

* **Nombre del proyecto:** BAUHAUS DIGITAL: Sistema Visual Interactivo
* **Autora:** Fatima Alexia Vera Navarrete
* **Descripción general:** Sistema visual e interactivo desarrollado en p5.js que traduce los lenguajes artísticos de la vanguardia Bauhaus a un entorno algorítmico y reactivo. El sistema transita por una pantalla informativa y dos experiencias dinámicas donde el color, la geometría y la síntesis sonora interactúan directamente con las acciones del usuario mediante teclado y mouse.

---

## Descripción Objetiva

* **Qué es el proyecto:** Es un software de arte generativo y diseño interactivo programado sobre la biblioteca p5.js.
* **Qué se ve en pantalla:** Una interfaz gráfica modular variable que transita por tres vistas o estados de interacción diferenciados por el uso del color de fondo y la densidad geométrica.
* **Qué elementos visuales aparecen:** Rectángulos, líneas de corte vertical, textos tipográficos de estilo afiche, una matriz de celdas móviles independientes que alternan cuadrados y círculos, círculos expansivos y un triángulo central con transparencias.
* **Qué inputs utiliza:** Coordenadas de posición del cursor en los ejes horizontal y vertical, clicks continuos del mouse y pulsaciones de teclas específicas (*A*, *S*, *E*).
* **Qué outputs genera:** Renderizado gráfico reactivo bidimensional en un lienzo digital de 400x600 píxeles y una onda de audio sintetizada cuya frecuencia y volumen se transforman dinámicamente en tiempo real.

---

## Descripción Conceptual

* **Idea central:** Traducir los principios de la escuela Bauhaus a un entorno digital algorítmico, donde las formas y los colores no son estáticos, sino variables fluidas controladas por lógica matemática e interactiva.
* **Corriente o referente de diseño:** La escuela Bauhaus, me inspire en los talleres de pintura abstracta, las composiciones modulares y las teorías del color desarrolladas por Vasili Kandinsky y Johannes Itten.
* **Referentes visuales, históricos o teóricos:** Los afiches tipográficos y composiciones de la etapa de Weimar. Se retoma el concepto histórico de la sinestesia (asociar directamente un tono cromático o una forma geométrica a una frecuencia sonora específica), explorado activamente en los tratados teóricos de Kandinsky.
* **Principio de diseño explorado:** La síntesis geométrica, la modulación espacial a través de grillas constructivas y el uso de la paleta de colores primarios y neutros de la escuela.

---

## Sistema Computacional

El proyecto se comporta como un sistema cerrado que procesa entradas de datos directas para generar transformaciones en los estados visuales y sonoros:

 Componente | Detalle y Variables Asociadas 

 **Inputs** Posición del cursor (mouseX, mouseY), eventos de teclado (key), click del mouse sostenido (mouseIsPressed). 
 **Procesos**  Mapeo continuo (map()) para calcular filas, columnas y tamaños; cálculo de alternancia geométrica y cromática con el operador residuo (%); desfases aleatorios por interacción (random()); desplazamiento vertical infinito basado en el conteo de cuadros (frameCount). 
 **Estados**  **Estado 0:** Pantalla de inicio estática con instrucciones.<br>**Estado 1:** Grilla interactiva modular en movimiento continuo.<br>**Estado 2:** Estudio concéntrico de color y forma sinestésica.
 **Eventos**  Presión de tecla A/a (cambio a Estado 1); presión de tecla S/s (cambio a Estado 2); presión de tecla E/e (retorno a Estado 0); click sostenido (activación de factor de ruido aleatorio en formas). 
 **Outputs**  Actualización visual en el canvas (formas en movimiento, textos de interfaz) y generación de audio sintético variable mediante oscilador triangular. 

---

## Explicación de la Interacción

* **Qué datos entran al sistema:** Entran las coordenadas numéricas de posición del mouse y los códigos de caracteres de las teclas presionadas por el usuario.
* **Cómo se procesan:** Los datos numéricos del cursor se normalizan y re-escalan a rangos útiles mediante funciones matemáticas de mapeo. Las pulsaciones de teclas pasan por una estructura condicional de control para redefinir el valor de la variable de estado general.
* **Cómo se transforman:** La posición horizontal modifica directamente la cantidad de columnas visibles en la grilla o el ancho de la base del triángulo principal; simultáneamente cambia el valor en hercios de la frecuencia sonora. La posición vertical altera el número de filas o el diámetro oscilante de los círculos.
* **Qué respuestas producen:** El sistema redibuja el lienzo a 60 cuadros por segundo mostrando cambios instantáneos de escala y posición geométrica, al mismo tiempo que el sintetizador de audio eleva o disminuye su tono y altera su volumen de salida para evidenciar auditivamente las transiciones del espacio.

---

## Recursos Multimedia Utilizados

* **Tipo de recurso utilizado:** Audio Sintetizado digitalmente en tiempo real a través del componente p5.Oscillator configurado con una onda de tipo triangular (triangle).
* **Función que cumple dentro del proyecto:** Actúa como un puente que reacciona a la interacción directa del usuario. No se utiliza como un elemento decorativo de fondo; su frecuencia está amarrada a las propiedades espaciales del sistema (posición horizontal y tamaño del triángulo). En el Estado 0 permanece completamente apagado para respetar la estructura limpia de la interfaz de presentación, y se enciende en las experiencias interactivas modificando sutilmente su volumen entre el Estado 1 (0.01) y el Estado 2 (0.03) para acentuar el paso entre atmósferas.

---

## Diagrama de Flujo

<img width="1380" height="752" alt="diagrama flujo final" src="https://github.com/user-attachments/assets/0e5ade95-6b7e-4194-aab3-e9ab0e2247ac" />





---

## Registro Visual

### Referentes
<img width="350" height="350" alt="wassily-kandinsky" src="https://github.com/user-attachments/assets/6f96f8e8-67fa-4fec-8e32-f25f324d40bf" />
<img width="440" height="454" alt="images" src="https://github.com/user-attachments/assets/aaefcac0-c0ef-42f9-b8ab-96ba557d613f" />







### Iteraciones y Capturas del Proceso

#### Pantalla de Inicio
![Captura de la interfaz de inicio](imagenes/captura_inicio.png)
*Descripción: Interfaz gráfica limpia inspirada en la composición y balance de los afiches tipográficos de la escuela Bauhaus en Weimar.*

#### Grilla Interactiva
![Captura de la grilla dinámica](imagenes/captura_grilla.png)
*Descripción: Demostración del comportamiento de la matriz geométrica activa, variando su densidad modular de acuerdo al movimiento del mouse.*

---

## Reflexión Final

* **Principales decisiones tomadas:** Se decidió implementar un control de estados estricto y centralizado mediante eventos de teclado para garantizar una navegación de usuario fluida y libre de interrupciones. Asimismo, se optó por un oscilador de onda triangular calibrado a volúmenes muy sutiles (0.01 en el Estado 1 y 0.03 en el Estado 2); esta sutil diferencia permite evidenciar la transición de la experiencia no solo de manera gráfica, sino también a través de una progresión atmosférica de carácter auditivo.
* **Dificultades encontradas:** El mayor desafío técnico consistió en lograr que los elementos de la grilla se desplazaran de forma vertical infinita en sentidos opuestos sin salirse de los márgenes inferiores diseñados para el afiche. Esto requirió calibrar y sincronizar minuciosamente el operador matemático de residuo (%) en relación con el parámetro del lienzo (height - 80).
* **Aprendizajes obtenidos:** El proyecto permitió consolidar la comprensión práctica sobre la programación orientada a estados en entornos de diseño interactivo. Se comprendió con claridad de qué manera un mismo software puede modificar radicalmente su comportamiento visual, sus ecuaciones y su lógica de interacción global con el usuario basándose simplemente en la gestión de variables de control global.
