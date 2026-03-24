# U2-Proyecto-Integrador

DOCUMENTACIÓN DEL PROYECTO DE ANIMACIÓN: KIRBY EN ESTRELLA

#INDÍCE
1. Introducción
2. Guia de poses y construcción
   * 2.1 Anatomía y Proporciones
   * 2.2 Poses clave
3. paleta de colores
4. Proceso de animación en blender
    * 4.1 Configuración del Escenario
    * 4.2 Importar la imagen de referencia
    * 4.3 Configurar la línea de tiempo
    * 4.4 Animación (Frames)
5. Resultados.
6. conclusión.


# 1. Introducción
Este proyecto consiste en la creación de una animación 2D tradicional (frame X frame) de un personaje icónic se escojio un dibujo de Kirby con una entrella para realizarlo.El objetivo es simular un movimiento de "walk cycle" (ciclo de caminata) pero con un enfoque en el rebote y la rotación, como si Kirby fuera una pelota de goma rodando sobre la estrella.
# 2. Guía de Poses y Construcción
Para garantizar la consistencia visual del personaje en cada fotograma, se ha establecido la siguiente guía de poses y construcción:
 ## 2.1 Anatomía y Proporciones:
   * Cuerpo: Esfera perfecta (círculo).
   * Estrella: Proporcionalmente más ancha que el cuerpo, con puntas redondeadas.
   * Ojos: Óvalos alargados que ocupan el tercio superior del rostro.
 ## 2.2 Poses Clave:
   * Pose A (Contacto): Kirby y la estrella tocan el suelo con la estrella nivelada.
   * Pose B (Down/Squash): Punto más bajo del movimiento, Kirby se comprime ligeramente contra la estrella por efecto de la gravedad.
   * Pose C (Passing): Kirby inicia el ascenso, un pie se levanta para impulsarse.
   * Pose D (Up/Stretch): Punto más alto del rebote, Kirby y la estrella se estiran ligeramente hacia arriba.
 * Squash & Stretch (Compresión y Estiramiento):
   * En el impacto (Suelo): Compresión en el eje vertical (Z) y expansión en el horizontal (X) para simular el rebote (ej. Z: 0.9, X: 1.1).
   * En el aire (Salto): Estiramiento en el eje vertical (Z) y compresión en el horizontal (X) para simular el impulso (ej. Z: 1.1, X: 0.9).

   ![Imagen de referencia](imagenes/referencia.png)
     
# 3. Paleta de Colores
Se ha seleccionado una paleta de colores específicos para reproducir fielmente la estética de Kirby:
 * Piel (Cuerpo): Hex #FEAFC9, RGB (254, 175, 201)
 * Pies/Zapatos: Hex #D70C57, RGB (215, 12, 87)
 * Ojos: Hex #3272AE, RGB (50, 114, 174)
 * Mejillas: Hex #FE7BB4, RGB (254, 123, 180)
 * Estrella (Cuerpo): Hex #FFF04B, RGB (255, 240, 75)
 * Bordes: Hex #000000, RGB (0, 0, 0)

   ![colores](images/paletadecolores.png)
   
# 4. Proceso de Animación en Blender (How To)
El flujo de trabajo para la animación frame X frame en Blender con Grease Pencil es el siguiente:
 ## 4.1 Configuración del Escenario:
   * Crear una escena 2D en Blender.
Se elimina el trazo predeterminado y se agrega un nuevo Grease Pencil en blanco.
Se configuran materiales específicos para trazos y rellenos de colores para utilizar durante la animación.

 ![pencil](images/pencil.png)

   ## 4.2 Importar la imagen de referencia como fondo.
Se importa una imagen de referencia, se ajusta su tamaño y se reduce su opacidad para facilitar el calcado.
   ## 4.3 Configurar la línea de tiempo (Timeline) con el número de fotogramas deseado para el ciclo de caminata.
Se dibujan los 7 fotogramas clave de la secuencia, dibujando primero los trazos (usando arcos y curvas) y luego los rellenos en cada pose.
 * Boceto (Draft):
   * En una capa de Grease Pencil para bocetos, dibujar las esferas base de Kirby y la forma general de la estrella para marcar el ritmo del movimiento en los fotogramas clave.
  
      ![Tiempo](images/tiempo.png)
     
 ## 4.4 Animación (Frames):
   * En una capa de Grease Pencil para animación, dibujar los fotogramas clave (Keyframes) basándose en la guía de poses (A, B, C, D).
Ajuste y Sincronización: Se organizan los fotogramas clave en la línea de tiempo (cada 3 fotogramas) y se ajusta la posición de cada dibujo para lograr una animación fluida.
 * En una capa de Grease Pencil para entintado, trazar las líneas definitivas del personaje con un pincel de grosor constante para obtener un estilo limpio y profesional.
 * Color (Materials):
   * Crear materiales en Blender con los colores hexadecimales definidos en la paleta para cada parte del personaje (Piel, Pies, Ojos, Mejillas, Estrella, Bordes).
   * Aplicar los colores a las áreas correspondientes utilizando la herramienta de pintando directamente en la capa de Grease Pencil.
   * Aseguramos que los colores sean consistentes en todos los fotogramas.
 * Revisión y Ajustes:
   * Reproducir la animación para verificar la fluidez del movimiento de "walk cycle".
   * Ajustar los tiempos de los fotogramas clave y la interpolación si es necesario para mejorar la sincronización del movimiento.
   * Verificar que la compresión y estiramiento se apliquen correctamente para lograr el efecto de rebote deseado.
Efectos Finales: Se añaden efectos de sombra y luz (ribete) para dar profundidad y se configura el color de fondo.
 
# 5. Resultados.

![Kyrby](images/kyrby.png)

# 6. Conclusión
Este proyecto de animación 2D en Blender ha permitido explorar la creación de un ciclo de caminata único para un personaje icónico como Kirby. Al seguir la guía de poses y la paleta de colores establecidas, y aplicar las técnicas de "Squash & Stretch" y la interpolación en Blender, se ha logrado recrear el movimiento de rebote y rotación característico de Kirby sobre su estrella.
