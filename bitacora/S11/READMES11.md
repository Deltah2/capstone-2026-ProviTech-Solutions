
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
