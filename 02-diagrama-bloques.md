# Diagrama de Bloques de la Solución

## Diagrama General del Sistema

```markdown
## Diagrama General del Sistema

```mermaid
graph TD
    A[CLIENTE - Usuario Final] --> B[CAPA DE ENTRADA: QR, WhatsApp, Instagram]
    B --> C[CAPA DE PROCESO: Google Forms y WhatsApp API]
    C --> D[CAPA DE DATOS: Google Sheets con Graficas]
    D --> E[COACH EMPRESARIAL: Dueno de Suscuni]
    
    style A fill:#f9f,stroke:#333
    style E fill:#bbf,stroke:#333
┌─────────────────────────────────────────────────────────────────┐
│ CLIENTE │
│ (Usuario Final) │
└─────────────────────────────────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────┐
│ CAPA DE ENTRADA │
│ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ │
│ │ QR en │ │ Instagram │ │ WhatsApp │ │
│ │ Mesas │ │ Channel │ │ Business │ │
│ └──────────────┘ └──────────────┘ └──────────────┘ │
└─────────────────────────────────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────┐
│ CAPA DE PROCESO │
│ ┌──────────────────────────────────────────────────┐ │
│ │ GOOGLE FORMS / JOTFORM │ │
│ │ - Formulario visual con imágenes de bebidas │ │
│ │ - Calificación 1-5 estrellas │ │
│ │ - Captura de datos (nombre, WhatsApp) │ │
│ │ - Campo de comentarios │ │
│ └──────────────────────────────────────────────────┘ │
│ │ │
│ ▼ │
│ ┌──────────────────────────────────────────────────┐ │
│ │ WHATSAPP BUSINESS API │ │
│ │ - Nombre de usuario (@suscuni) │ │
│ │ - Mensaje de bienvenida automático │ │
│ │ - Mensaje de ausencia (fuera de horario) │ │
│ │ - Respuestas rápidas (/horario, /ubicacion) │ │
│ └──────────────────────────────────────────────────┘ │
─────────────────────────────────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────┐
│ CAPA DE DATOS │
│ ┌──────────────────────────────────────────────────┐ │
│ │ GOOGLE SHEETS │ │
│ │ - Base de datos de feedback │ │
│ │ - Base de datos de clientes frecuentes │ │
│ │ - Registro de cumpleaños │ │
│ │ - Vista de Resumen con gráficas automáticas │ │
│ └──────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────┐
│ CAPA DE SALIDA │
│ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ │
│ │ Dashboard │ │ Reportes │ │ Notif. │ │
│ │ Gráficas │ │ Semanales │ │ Cumpleaños │ │
│ └──────────────┘ └──────────────┘ └──────────────┘ │
└─────────────────────────────────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────┐
│ COACH EMPRESARIAL │
│ (Dueño de Suscuni) │
│ - Visualiza gráficas automáticas │
│ - Toma decisiones basadas en datos │
│ - Envía anuncios por Instagram Channel │
│ - Gestiona clientes frecuentes │
└─────────────────────────────────────────────────────────────────┘ ```
*Actualizado en branch de desarrollo*
