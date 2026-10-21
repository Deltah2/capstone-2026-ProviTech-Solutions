
# S11 - Definición del MVP y Preparación del Pitch de Solución

**Equipo:** Provitech Solutions  
**Proyecto:** Sistema integrado para la gestión de reservas y uso de espacios (Hub Providencia)  
**Fecha:** Noviembre de 2026  

---

## 1. Diagnóstico Consolidado del Problema

El desafío **"Edificios Inteligentes: Sistema integrado de reserva y uso de espacios"** para la Municipalidad de Providencia surge porque el proceso actual es 100% manual y descentralizado:

*   **Atención y coordinación por correo:** Las reservas de laboratorios (Impresión 3D, Corte Láser, Videojuegos) y salas de reuniones (Salas 1 y 4) se gestionan enviando correos al equipo administrativo, generando cuellos de botella e ineficiencia operativa.
*   **El problema de las "Reservas Fantasma":** Al tratarse de un servicio gratuito, las personas reservan con anticipación y luego no asisten. Al no existir costo de oportunidad ni confirmación automatizada, los espacios quedan bloqueados y se pierde disponibilidad para otros vecinos o emprendedores.
*   **Fricción en el registro y datos "sucios":** Quienes acuden al cowork o a los laboratorios deben escanear un código QR e ingresar manualmente sus datos (RUT, nombre, ocupación) cada vez que entran. Esto frustra al usuario recurrente y genera errores tipográficos que la administración debe limpiar a mano en planillas.
*   **Falta de trazabilidad e indicadores:** No existe un historial consolidado ni métricas claras sobre la demanda real, horas punta o tasa de ocupación de los espacios.

---

## 2. Definición del Prototipo (MVP - Producto Mínimo Viable)

De acuerdo con los requerimientos del desafío y los hallazgos técnicos levantados en terreno:
1.  **Uso estricto de herramientas Open Source** (cero costo de licencias para la municipalidad).
2.  **Arquitectura orientada a Bases de Datos No Relacionales (NoSQL)**, alineada a la migración tecnológica de la institución.

### Arquitectura Funcional (4 Módulos Clave)

```text
 ┌─────────────────────────────────────────────────────────┐
 │                   SISTEMA HUB RESERVAS                  │
 └────────────────────────────┬────────────────────────────┘
                              │
     ┌────────────────────────┼────────────────────────┐
     ▼                        ▼                        ▼
┌──────────────┐      ┌──────────────┐        ┌──────────────┐
│  Módulo 1:   │      │  Módulo 2:   │        │  Módulo 3:   │
│ Identidad    │      │ Catálogo y   │        │ Validación   │
│ Única        │      │ Reserva      │        │ / Check-in   │
│ (Perfil)     │      │ (Calendario) │        │ (QR / RUT)   │
└──────────────┘      └──────────────┘        └──────────────┘
                                                       │
                                                       ▼
                                              ┌──────────────┐
                                              │  Módulo 4:   │
                                              │ Panel Admin  │
                                              │ (KPIs / Uso) │
                                              └──────────────┘
---
```

#### Módulo 1: Identidad Única de Usuario (Registro Único)
*   Permite que el usuario se registre una sola vez en la plataforma (cumpliendo con el consentimiento de datos).
*   En visitas posteriores, solo necesita acreditarse mediante su RUT o código QR personal, eliminando el llenado repetitivo de formularios diarios.

#### Módulo 2: Catálogo y Agenda de Disponibilidad (Laboratorios y Salas)
*   Vista interactiva en tiempo real para consultar la disponibilidad de los Laboratorios (reglas por cupos en Impresión 3D, bloques de tiempo en Corte Láser y pase diario en Videojuegos) y de las Salas 1 y 4.
*   Elimina por completo la coordinación vía correo electrónico.

#### Módulo 3: Mecanismo de Check-in / Validación de Asistencia
*   Confirmación presencial rápida al llegar al Hub Providencia.
*   **Regla anti-ausentismo:** Si el usuario no realiza el check-in dentro de la ventana de tolerancia (ej. primeros 15 minutos), la reserva se libera automáticamente para combatir las "reservas fantasma".

#### Módulo 4: Panel de Indicadores para Administración (Dashboard)
*   Visualización consolidada para la toma de decisiones municipales:
    *   Tasa de ocupación efectiva por laboratorio y sala.
    *   Porcentaje de inasistencias (*no-shows*).
    *   Trazabilidad de horarios y días de mayor demanda.

---

## 3. Plan de Acción y Roles del Equipo

| Integrante | Rol | Entregable para el MVP |
| :--- | :--- | :--- |
| **Felipe Andrés Barrios** | Frontend | Construcción de la interfaz web (wireframes y maquetación) para el catálogo de espacios, selección de horarios y pantalla de check-in. |
| **Luckas Ariel Asencio** | Backend / BD | Diseño del modelo de datos (NoSQL) para gestionar usuarios, espacios, reglas de negocio de laboratorios, estados de reserva e historial. |
| **José Ignacio Bernal** | Procesos & KPIs | Diseño funcional del panel de administración con los indicadores clave de uso, ocupación e inasistencia. |
