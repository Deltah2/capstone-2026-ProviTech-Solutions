Bitácora - Semana 7

Equipo: Provitech Solutions
Proyecto: Sistema integrado para la gestión de reservas y uso de espacios (Hub Providencia)
Fecha: 29 de octubre de 2026

![Foto del equipo Provitech Solutions](https://github.com/Deltah2/capstone-2026-ProviTech-Solutions/blob/dbb7ffa9e46852e7f1d204524abfd25f38886d74/Imagenes%20/S07/IMG_2980.jpeg)

1. Resumen de Actividades

Durante la Semana 7, el equipo realizó una salida a terreno al Hub Providencia para llevar a cabo la fase de empatía y observación directa. Se realizó una entrevista y levantamiento de requerimientos con la administración del recinto para comprender en profundidad los flujos de trabajo actuales, las limitantes tecnológicas y las reglas de negocio de los espacios físicos.

![Foto del equipo Provitech Solutions](https://github.com/Deltah2/capstone-2026-ProviTech-Solutions/blob/dbb7ffa9e46852e7f1d204524abfd25f38886d74/Imagenes%20/S07/IMG_2969.jpeg)

2. Hallazgos del Levantamiento en Terreno

A partir de la conversación con el equipo del Hub, se definieron los siguientes puntos críticos que guiarán el desarrollo técnico (Backend y Frontend):

A. El Proceso Actual y Experiencia de Usuario (UX)

Falta de visibilidad: Los usuarios no tienen cómo ver la disponibilidad (calendario) antes de llegar al recinto. Muchas reservas se solicitan de forma presencial y "a ciegas".

Fricción en el registro: El mayor problema actual de experiencia de usuario es que las personas deben llenar manualmente un formulario (mediante un código QR) cada vez que ingresan, entregando datos como nombre, RUT y ocupación repetidas veces.

Trabajo manual: La administración pierde horas valiosas limpiando los datos ingresados en el formulario debido a faltas de ortografía o inconsistencias.

B. Reglas de Negocio (Lógica para el Sistema)

Restricción de agenda: No se permite programar reservas con mucha anticipación ni de forma repetitiva para evitar las "reservas fantasma", ya que al ser un espacio gratuito, la gente suele faltar si no hay costo de oportunidad.

Laboratorio de Impresión 3D: Se maneja por "cupos" de tiempo (ej. de 1-2 horas, 3-5 horas, etc.). El usuario solo requiere estar presencialmente 30-45 minutos; luego puede retirarse y volver a buscar la pieza.

Corte Láser: Funciona por bloques exactos de tiempo agendado (ej. 30 minutos). Terminado el bloque, el usuario debe ceder el espacio.

Laboratorio de Videojuegos: Opera bajo una lógica de "pase diario" o uso libre, similar al área de cowork, sin límite estricto de tiempo por ahora debido a la demanda actual.

C. Requerimientos Técnicos y Arquitectura

Bases de Datos: La municipalidad e institución están en proceso de migrar su estructura hacia Bases de Datos No Relacionales. Nuestro desarrollo deberá alinearse a este estándar.

Sistema de Identidad Única: El "sueño" administrativo es tener un sistema similar a la Clave Única, donde el usuario se registre solo una vez en una base centralizada y, en sus visitas posteriores, solo valide su ingreso de forma rápida.

Métricas (KPIs): Actualmente no tienen forma de medir la ocupación real del espacio ni de trazar los horarios "punta", un requerimiento fundamental que nuestra plataforma deberá solucionar.

![Foto del equipo Provitech Solutions](https://github.com/Deltah2/capstone-2026-ProviTech-Solutions/blob/dbb7ffa9e46852e7f1d204524abfd25f38886d74/Imagenes%20/S07/IMG_2971.jpeg)
