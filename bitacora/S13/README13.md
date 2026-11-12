
# S13 - Bitácora: Presentación de Pitch y Prototipado Rápido (Desafío del Marshmallow)

**Equipo:** ProviTech Solutions  
**Proyecto:** Sistema integrado para la gestión de reservas y uso de espacios (Hub Providencia)  
**Integrantes:** Luckas Asencio, Felipe Barrios, José Bernal  
**Responsable del registro:** Luckas Ariel Asencio Vargas  

---

## 1. Resumen de la Sesión

Durante la Semana 13 se llevaron a cabo dos hitos prácticos fundamentales en el curso:
1. **Diseño y Presentación del Pitch de Solución:** Exposición formal de la propuesta tecnológica para el desafío *"Edificios Inteligentes: Sistema integrado de reserva y uso de espacios"* del Hub Providencia.
2. **Taller de Prototipado Rápido (Desafío del Marshmallow):** Dinámica grupal de ingeniería y colaboración para construir una estructura autoportante con fideos y cinta adhesiva, poniendo a prueba la iteración temprana y el aprendizaje a partir del error.

---

## 2. Creación y Presentación del Pitch: ProviTech Solutions

El equipo estructuró y presentó la propuesta de valor, la arquitectura de software y el plan de puesta en marcha de la plataforma web para el Hub Providencia, abarcando 6 ejes clave:

### A. Diagnóstico y Evaluación de Alternativas
* **El Problema Validado en Terreno:** Coordinación manual por correo electrónico que tarda días, espacios gratuitos bloqueados por "reservas fantasma", llenado repetitivo de formularios manuales con errores en cada visita y ceguera de datos para la Municipalidad.
* **Selección de Alternativa:** Se descartó el uso de planillas con formularios (por mantener datos sucios) y el software comercial (por el alto costo mensual de licencias), seleccionando el desarrollo de la **plataforma a medida ProviTech Solutions** con costo cero en licencias.

### B. La Solución y Control Anti-Fantasmas
* **Identidad Única:** Registro por única vez validando el RUT del usuario, eliminando los formularios diarios en la entrada.
* **Agenda Inteligente:** Disponibilidad en tiempo real adaptada a las reglas de cada espacio (*Impresión 3D* por cupos flexibles, *Corte Láser* en bloques rígidos de 30 minutos, y *Cowork/Videojuegos* mediante pase diario), junto con cancelación en un solo clic.
* **Check-in Presencial (15 min de tolerancia):** Al llegar al Hub, el usuario escanea su QR o digita su RUT en la tablet de recepción. Si no valida su asistencia dentro de los primeros 15 minutos, el sistema anula la reserva automáticamente y libera el laboratorio en vivo para otro vecino.

### C. Puesta en Marcha e Indicadores (Dashboard)
* **Viabilidad y Costo ($0 en licencias):** Arquitectura 100% *Open Source* con base de datos NoSQL en servidores municipales, reutilizando la tablet de recepción existente.
* **Operación y Piloto:** Capacitación práctica de 45 minutos para que el equipo del Hub pase de responder correos a supervisar el sistema, iniciando con un **plan piloto de 2 semanas** enfocado en Impresión 3D y Corte Láser.
* **Métricas en Vivo:** Reducción a 0 correos de coordinación, medición del porcentaje de bloques recuperados a los 15 minutos y reportes en tiempo real de ocupación y horas punta.

### Evidencias de la Presentación (Pitch):
<details>
<summary><b>Haz clic aquí para ver las diapositivas y fotos de la presentación del Pitch</b></summary>
<br>
<!-- Reemplaza las rutas con los enlaces o nombres de tus imágenes en GitHub -->
<p align="center">
  <img src="../../imagenes/S13/pitch_1.png?raw=true" alt="Presentación Pitch ProviTech 1" width="80%">
  <br><br>
  <img src="../../imagenes/S13/pitch_2.png?raw=true" alt="Presentación Pitch ProviTech 2" width="80%">
</p>
</details>

---

## 3. Actividad Práctica: Desafío del Marshmallow (Torre de Fideos)

Como ejercicio práctico de diseño, colaboración bajo presión y prototipado rápido, el equipo participó en la construcción de la torre autoportante más alta capaz de sostener un malvavisco (*marshmallow*) completo en la cúspide.

### Parámetros y Materiales del Desafío:
* **Materiales asignados por equipo:** 18 espaguetis crudos, 1 metro de cinta adhesiva (*scotch*) y 1 malvavisco.
* **Tiempo límite:** 30 minutos para diseñar, construir y probar la estructura.
* **Regla crítica:** La torre debía mantenerse en pie por sí sola soportando el peso del malvavisco en la punta sin colapsar.

### Aprendizajes Conectados al Proyecto Capstone:
1. **Iteración temprana vs. planificación excesiva:** Al igual que en el desarrollo de software, dejar la prueba de carga (colocar el malvavisco) para el último minuto aumenta el riesgo de colapso estructural. Validar el prototipo desde el inicio permite corregir fallas de base a tiempo.
2. **Distribución de esfuerzos y estabilidad:** Se reforzó la importancia de construir una base sólida (como nuestra arquitectura de base de datos y reglas de negocio) antes de escalar en altura (interfaz y funciones secundarias).
3. **Trabajo colaborativo:** Coordinación de roles en tiempo real para cortar cinta, ensamblar nodos estructurales y controlar el tiempo.

### Evidencias del Desafío del Marshmallow:
<details>
<summary><b>Haz clic aquí para ver las fotografías de la construcción de la torre de fideos</b></summary>
<br>
<!-- Reemplaza las rutas con los enlaces o nombres de tus fotos de la actividad -->
<p align="center">
  <img src="../../imagenes/S13/fideos_1.jpeg?raw=true" alt="Construcción torre de espaguetis 1" width="75%">
  <br><br>
  <img src="../../imagenes/S13/fideos_2.jpeg?raw=true" alt="Resultado final desafío del malvavisco" width="75%">
</p>
</details>
