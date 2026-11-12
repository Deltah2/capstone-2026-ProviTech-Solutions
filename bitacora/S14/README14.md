
# S14 - Bitácora: Validación de Prototipo, Planificación de Stand y Prueba de Impacto (Egg Drop)

**Equipo:** ProviTech Solutions  
**Proyecto:** Sistema integrado para la gestión de reservas y uso de espacios (Hub Providencia)  
**Integrantes:** Luckas Asencio, Felipe Barrios, José Bernal  
**Responsable del registro:** Luckas Ariel Asencio Vargas  

---

## 1. Resumen de la Sesión

Durante la Semana 14 el trabajo se dividió en dos frentes prácticos orientados a la validación empírica (pasar *"De la Propuesta a la Evidencia"*):
1. **Actividad Práctica de Ingeniería (Desafío de Caída del Huevo / *Egg Drop*):** Diseño, construcción y prueba real de un prototipo físico de absorción de impacto lanzado desde el segundo piso del campus.
2. **Revisión de Avance por Equipo (Prototipo Web y Feria Capstone):** Evaluación de los resultados concretos del MVP de **ProviTech Solutions**, pruebas de validación, definición de roles para la demostración y diseño operativo del stand.

---

## 2. Actividad Práctica: Desafío de Caída del Huevo (Segundo Piso)

Como entrenamiento práctico de prototipado, gestión de riesgos y validación en condiciones reales, el equipo construyó una estructura protectora con materiales limitados cuyo objetivo único era lograr que un huevo crudo sobreviviera intacto a una caída libre desde el segundo piso del edificio.

### Aprendizajes Conectados al Proyecto Capstone:
* **La prueba real es el único validador:** En ingeniería, un diseño teórico parece perfecto hasta que se somete al impacto real (el lanzamiento desde el segundo piso). De igual forma, nuestro software de reservas debe probarse con flujos de usuarios reales e intentos de error antes de llegar al Hub Providencia.
* **Tolerancia a fallos (Plan de amortiguación):** Así como la estructura física necesitó zonas de deformación y absorción de energía para proteger el núcleo (el huevo), nuestra plataforma web incorpora validadores de entrada y un sistema local autónomo (Plan B) para que el sistema no colapse durante la demostración en la Feria Capstone.

### Evidencias del Lanzamiento (Egg Drop):
<details>
<summary><b>Haz clic aquí para ver las fotos de la construcción y lanzamiento desde el 2° piso</b></summary>
<br>
<!-- Reemplaza las rutas con los nombres de tus fotos en GitHub -->
<p align="center">
  <img src="../../imagenes/S14/huevo_1.jpeg?raw=true" alt="Construcción del prototipo protector del huevo" width="75%">
  <br><br>
  <img src="../../imagenes/S14/huevo_2.jpeg?raw=true" alt="Prueba de caída desde el segundo piso" width="75%">
</p>
</details>

---

## 3. Reporte de Avance del Equipo: ProviTech Solutions

A continuación, se documentan las respuestas formales a los 4 ejes de evaluación de avance rumbo a la Feria Capstone:

### 01. ¿Qué hicieron? ¿Cómo van? (Resultados concretos de la última semana)
Pasamos del diseño conceptual al desarrollo concreto de nuestro **Producto Mínimo Viable (MVP) Web Interactivo**, logrando:
* **Integración de los 4 módulos en una Single-Page Application funcional:**
  1. *Módulo de Identidad Única:* Formulario con validador de formato RUT chileno y generación automática de credencial digital QR.
  2. *Catálogo y Agenda Inteligente:* Grilla horaria interactiva programada con las reglas reales del Hub (*Impresión 3D* por cupos, *Corte Láser* en bloques de 30 min, *Salas 1 y 4* y *Cowork*).
  3. *Tótem de Recepción (Check-in Presencial):* Interfaz tipo Kiosco con temporizador de tolerancia de 15 minutos para erradicar las "reservas fantasma".
  4. *Dashboard Municipal y Visor NoSQL:* Panel con gráficos dinámicos de ocupación e inspector en vivo de documentos JSON.

### 02. ¿Cómo lo comprobaron? (Pruebas, indicadores, registros y fallas)
* **Protocolo de prueba:** Se ejecutaron pruebas funcionales internas simulando el ciclo completo de 15 reservas en distintos espacios del Hub.
* **Indicadores y resultados medidos:**
  * **Tiempo de reserva:** Reducción del flujo de solicitud a menos de **45 segundos** desde el catálogo web (frente a días de espera por correo electrónico).
  * **Liberación automática (Anti-Fantasmas):** El **100% de las reservas simuladas sin check-in** tras el vencimiento del temporizador (15 min) cambiaron su estado a `liberada_inasistencia`, habilitando el cupo en el calendario inmediatamente.
* **Principales fallas detectadas y corregidas:**
  * *Falla 1 (Entrada de datos):* El campo de RUT permitía ingresar texto sin formato estandarizado. **Solución:** Se implementó una función validadora y formateadora automática de RUT (`XX.XXX.XXX-X`).
  * *Falla 2 (Sincronización de vistas):* Al cancelar una reserva en el perfil del usuario, el gráfico del Dashboard administrativo no se actualizaba hasta recargar la vista. **Solución:** Se centralizó el estado en un único objeto reactivo que refresca los KPIs y el documento JSON en tiempo real.

### 03. ¿Quién hará qué? (Roles claros para el Pitch y la Demostración)

| Integrante | Rol en Competencia de Pitch | Rol en Demostración (Stand Feria Capstone) |
| :--- | :--- | :--- |
| **Luckas Ariel Asencio** | **Expositor Oficial Pitch:** Viabilidad técnica, arquitectura *Open Source* ($0 licencias), modelo NoSQL, puesta en marcha y cierre de impacto. | **Demostrador Backend & Datos:** Muestra a la comisión cómo cada reserva impacta en vivo la estructura documental NoSQL y explica el plan piloto de 2 semanas. |
| **Felipe Andrés Barrios** | **Expositor Oficial Pitch:** Presentación de la solución, flujo de experiencia de usuario (UX) y mecanismo de Check-in presencial de 15 minutos. | **Guía de Interacción (Frontend):** Invita a los visitantes a usar la tablet/tótem para hacer *check-in* con QR/RUT y reservar un laboratorio en vivo. |
| **José Ignacio Bernal** | **Soporte Estratégico y Q&A:** Apoyo en preparación de métricas y respuesta a preguntas de gestión y procesos ante la comisión. | **Anfitrión y Analista de KPIs:** Recibe a los visitantes en el stand, contextualiza los dolores del Hub Providencia y explica los gráficos del Dashboard Municipal. |

### 04. ¿Cómo será el stand? (Prototipo, soporte visual, interacción y Plan B)
* **Prototipo e Interacción con el Visitante:**
  * **Estación 1 - Tótem de Recepción (Tablet / iPad):** Dispuesta en el borde frontal del stand para que cualquier visitante o evaluador pueda digitar un RUT o usar una tarjeta QR de prueba, experimentando en 5 segundos cómo se valida el ingreso o cómo se libera un laboratorio por inasistencia.
  * **Estación 2 - Monitor Principal (Laptop):** Pantalla dividida mostrando el Catálogo de Reservas de Laboratorios y el Dashboard Administrativo de la Municipalidad actualizándose en tiempo real según lo que el visitante haga en la Estación 1.
* **Soporte Visual:**
  * Diagrama visual comparativo ("Flujo Manual Actual por Correo vs. Flujo Automatizado ProviTech").
  * Credenciales físicas impresas con códigos QR de prueba ("Vecino Emprendedor", "Estudiante Impresión 3D") para entregar en mano al jurado e invitarlos a interactuar.
* **Plan B (Contingencia Técnica):**
  * **Ejecución 100% Offline (Local):** El prototipo web y sus librerías estarán descargados y ejecutándose de manera local, eliminando cualquier dependencia de la red Wi-Fi de la universidad.
  * **Respaldo de Hardware y Video:** Contaremos con dos laptops configurados con el mismo entorno (MacBook Air M1 y Lenovo Legion) más un iPad de apoyo. En caso de corte eléctrico o fallo crítico, dispondremos de un video MP4 pregrabado con el recorrido funcional completo y capturas en alta resolución.

---

### Evidencias de la Sesión y del Prototipo:
<details>
<summary><b>Haz clic aquí para ver la diapositiva de trabajo y capturas del avance</b></summary>
<br>
<p align="center">
  <img src="../../imagenes/S14/avance_equipo_s14.jpeg?raw=true" alt="Pauta de Avance por Equipo S14" width="80%">
</p>
</details>
