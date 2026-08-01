# Matriz de Dependencias y Prioridades

## Tabla de Funcionalidades

| ID | Funcionalidad | Prioridad | Dependencia | Elemento Agrupador |
|----|--------------|-----------|-------------|-------------------|
| RF-001 | Registro de Feedback de Bebidas | ALTA | Ninguna | Módulo de Feedback |
| RF-002 | Generación Automática de Gráficas | ALTA | RF-001 | Módulo de Feedback |
| RF-003 | Registro de Clientes Frecuentes | MEDIA | RF-001 | Módulo de Fidelización |
| RF-004 | Automatización de WhatsApp | MEDIA | Ninguna | Módulo de Comunicación |
| RF-005 | Canal de Difusión Instagram | BAJA | Ninguna | Módulo de Comunidad |
| RF-006 | Sistema de Fidelización con QR | MEDIA | RF-003 | Módulo de Fidelización |
| RIE-001 | Compatibilidad Smartphones | ALTA | RF-001 | Infraestructura |
| RIE-002 | Integración Google Workspace | ALTA | RF-001, RF-002 | Infraestructura |
| RIE-003 | Integración WhatsApp Business | MEDIA | RF-004 | Infraestructura |
| RIE-004 | Integración Instagram | BAJA | RF-005 | Infraestructura |
| RD-001 | Estética Visual | ALTA | RF-001 | Diseño |
| RD-002 | Experiencia de Usuario | ALTA | RF-001 | Diseño |
| RD-003 | Diseño "Silencioso" | MEDIA | RF-001 | Diseño |
| RAC-001 | Usabilidad | ALTA | RD-002 | Calidad |
| RAC-002 | Disponibilidad | ALTA | RIE-002 | Calidad |
| RAC-003 | Escalabilidad | MEDIA | RIE-002 | Calidad |
| RAC-004 | Mantenibilidad | ALTA | OR-002 | Calidad |
| RS-001 | Privacidad Datos Cliente | ALTA | Ninguna | Seguridad |
| RS-002 | Privacidad Número Dueño | ALTA | RF-004 | Seguridad |
| RS-003 | Control de Acceso | ALTA | RIE-002 | Seguridad |
| RS-004 | Integridad de Datos | MEDIA | RIE-002 | Seguridad |
| OR-001 | Cero Costo | ALTA | Ninguna | Restricciones |
| OR-002 | Sin Conocimientos Técnicos | ALTA | OR-001 | Restricciones |
| OR-003 | Implementación 13 Semanas | ALTA | Ninguna | Restricciones |
| OR-004 | Consentimiento GitHub | ALTA | Ninguna | Restricciones |

## Diagrama de Dependencias
                ┌─────────────┐
                │   INICIO    │
                └─────────────┘
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
    ┌─────────┐  ┌─────────┐  ┌─────────┐
    │ RF-001  │  │ RF-004  │  │ RF-005  │
    │Feedback │  │WhatsApp │  │Instagram│
    └─────────┘  └─────────┘  └─────────┘
          │            │            │
          ▼            │            │
    ┌─────────┐        │            │
    │ RF-002  │        │            │
    │Gráficas │        │            │
    └─────────┘        │            │
          │            │            │
          ▼            ▼            ▼
    ┌─────────┐  ┌─────────┐  ┌─────────┐
    │ RF-003  │  │ RS-002  │  │ RIE-004 │
    │Clientes │  │Priv.    │  │Int.     │
    │Frec.    │  │Número   │  │Instagram│
    └─────────┘  └─────────┘  └─────────┘
          │
          ▼
    ┌─────────┐
    │ RF-006  │
    │Fideliz. │
    └─────────┘

## Justificación de Prioridades

### PRIORIDAD ALTA (Debe implementarse primero):
- **RF-001, RF-002:** Son el núcleo del proyecto. Sin feedback y gráficas, no hay valor para el dueño.
- **RIE-001, RIE-002:** Sin compatibilidad con smartphones e integración con Google, el sistema no funciona.
- **RD-001, RD-002:** La estética y UX son críticas para la adopción por parte de los clientes.
- **RAC-001, RAC-002, RAC-004:** Usabilidad, disponibilidad y mantenibilidad son esenciales para el éxito.
- **RS-001, RS-002, RS-003:** La privacidad es un requerimiento legal y ético no negociable.
- **OR-001, OR-002, OR-003, OR-004:** Son restricciones del proyecto que deben cumplirse obligatoriamente.

### PRIORIDAD MEDIA (Importante pero puede esperar):
- **RF-003, RF-006:** La fidelización es valiosa pero no crítica en las primeras semanas.
- **RF-004:** WhatsApp Business es útil pero el dueño puede atender manualmente al inicio.
- **RIE-003:** La integración con WhatsApp es importante pero no urgente.
- **RD-003:** El diseño "silencioso" de los QR es deseable pero se puede ajustar después.
- **RAC-003:** La escalabilidad es importante a largo plazo, pero el café es pequeño.
- **RS-004:** La integridad de datos es importante pero Google Sheets ya lo garantiza.

### PRIORIDAD BAJA (Nice to have):
- **RF-005:** El canal de Instagram es complementario, no esencial.
- **RIE-004:** La integración con Instagram puede hacerse al final del proyecto.

## Agrupación por Elemento

### Módulo de Feedback (ALTA)
- RF-001: Registro de Feedback
- RF-002: Generación de Gráficas
- RIE-001: Compatibilidad Smartphones
- RIE-002: Integración Google Workspace
- RD-001: Estética Visual
- RD-002: Experiencia de Usuario
- RAC-001: Usabilidad
- RAC-002: Disponibilidad

### Módulo de Fidelización (MEDIA)
- RF-003: Registro de Clientes
- RF-006: Sistema de Puntos
- RD-003: Diseño Silencioso
- RAC-003: Escalabilidad

### Módulo de Comunicación (MEDIA)
- RF-004: Automatización WhatsApp
- RIE-003: Integración WhatsApp
- RS-002: Privacidad Número

### Módulo de Comunidad (BAJA)
- RF-005: Canal Instagram
- RIE-004: Integración Instagram

### Infraestructura y Calidad (ALTA)
- RAC-004: Mantenibilidad
- RS-001: Privacidad Datos
- RS-003: Control de Acceso
- RS-004: Integridad Datos

### Restricciones del Proyecto (ALTA)
- OR-001: Cero Costo
- OR-002: Sin Conocimientos Técnicos
- OR-003: 13 Semanas
- OR-004: Consentimiento GitHub