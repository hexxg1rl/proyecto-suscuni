
---

### **CRITERIO 3: REQUERIMIENTOS **



```markdown
# Requerimientos del Sistema

## 1. Requerimientos Funcionales

### RF-001: Registro de Feedback de Bebidas
**Descripción:** El sistema debe permitir a los clientes calificar bebidas de temporada mediante un formulario digital.

**Componentes:**
- Formulario con imágenes de bebidas
- Sistema de calificación de 1 a 5 estrellas
- Campo de texto para comentarios opcionales
- Campo de nombre (opcional)
- Campo de WhatsApp (opcional)

**Prioridad:** ALTA  
**Dependencia:** Ninguna

---

### RF-002: Generación Automática de Gráficas
**Descripción:** El sistema debe generar automáticamente gráficas de pastel y barras que muestren:
- Promedio de calificación por bebida
- Número de respuestas por semana
- Bebidas más populares
- Distribución de calificaciones

**Componentes:**
- Google Sheets con vista de "Resumen"
- Fórmulas automáticas (AVERAGE, COUNT, FILTER)
- Actualización en tiempo real

**Prioridad:** ALTA  
**Dependencia:** RF-001

---

### RF-003: Registro de Clientes Frecuentes
**Descripción:** El sistema debe permitir el registro opcional de clientes para programa de fidelización.

**Componentes:**
- Formulario de registro ligero (solo nombre y WhatsApp)
- Campo de fecha de cumpleaños (opcional)
- Campo de bebida favorita (opcional)
- Sistema de puntos (5 visitas = 1 bebida gratis)

**Prioridad:** MEDIA  
**Dependencia:** RF-001

---

### RF-004: Automatización de WhatsApp Business
**Descripción:** El sistema debe configurar mensajes automáticos en WhatsApp Business.

**Componentes:**
- Mensaje de bienvenida (se envía la primera vez que un cliente escribe)
- Mensaje de ausencia (se envía fuera del horario de 8:00 AM - 8:00 PM)
- Respuestas rápidas con atajos:
  - /horario → "Nuestro horario es de Lunes a Domingo de 8:00 AM a 8:00 PM"
  - /ubicacion → "Estamos en [dirección completa]"
  - /menu → "Puedes ver nuestro menú en [link]"

**Prioridad:** MEDIA  
**Dependencia:** Ninguna

---

### RF-005: Canal de Difusión en Instagram
**Descripción:** El sistema debe permitir la creación y gestión de un Canal de Difusión en Instagram.

**Componentes:**
- Creación de canal "Suscuni - Novedades"
- Publicación de anuncios de bebidas de temporada
- Mención del canal en QR de feedback

**Prioridad:** BAJA  
**Dependencia:** Ninguna

---

### RF-006: Sistema de Fidelización con QR
**Descripción:** El sistema debe permitir el control de visitas mediante QR o código.

**Componentes:**
- Generación de código único por cliente
- Registro de visitas en Google Sheets
- Contador automático de puntos
- Notificación al alcanzar 5 visitas

**Prioridad:** MEDIA  
**Dependencia:** RF-003

---

## 2. Requerimientos de Interfaz Externa

### RIE-001: Compatibilidad con Smartphones
**Descripción:** El formulario debe ser accesible desde cualquier smartphone con cámara y navegador web.

**Especificaciones:**
- Compatible con iOS (Safari) y Android (Chrome)
- Diseño responsive (adaptable a diferentes tamaños de pantalla)
- Tiempo de carga < 3 segundos

---

### RIE-002: Integración con Google Workspace
**Descripción:** El sistema debe integrarse con herramientas de Google.

**Especificaciones:**
- Google Forms para captura de datos
- Google Sheets para almacenamiento y visualización
- Acceso mediante cuenta de Google gratuita

---

### RIE-003: Integración con WhatsApp Business API
**Descripción:** El sistema debe utilizar la API gratuita de WhatsApp Business.

**Especificaciones:**
- Versión gratuita de WhatsApp Business
- Configuración de nombre de usuario (@suscuni)
- Enlaces directos wa.me/suscuni

---

### RIE-004: Integración con Instagram
**Descripción:** El sistema debe integrarse con Instagram para canal de difusión.

**Especificaciones:**
- Cuenta de Instagram Business o Creator
- Función de "Broadcast Channel" habilitada
- Link en bio del perfil

---

## 3. Requerimientos de Diseño

### RD-001: Estética Visual
**Descripción:** El diseño debe reflejar la identidad de marca de Suscuni.

**Especificaciones:**
- Paleta de colores: Café (#6F4E37), Beige (#F5F5DC), Crema (#FFFDD0)
- Tipografía: Sans-serif moderna (Montserrat o similar)
- Imágenes de alta calidad de las bebidas
- QR con diseño personalizado (no solo código negro)

---

### RD-002: Experiencia de Usuario (UX)
**Descripción:** El formulario debe ser intuitivo y rápido de completar.

**Especificaciones:**
- Máximo 4-5 preguntas
- Tiempo de llenado < 30 segundos
- Instrucciones claras y visibles
- Botones grandes y fáciles de tocar

---

### RD-003: Diseño "Silencioso"
**Descripción:** Los QR físicos no deben interrumpir la estética del café.

**Especificaciones:**
- Tamaño: 5cm x 5cm (aproximadamente)
- Material: Acrílico o papel laminado de calidad
- Texto minimalista: "¿Cómo estuvo tu bebida? Escanea aquí "
- Colores que combinen con la decoración del local

---

## 4. Requerimientos de Atributos de Calidad

### RAC-001: Usabilidad
**Descripción:** El sistema debe ser fácil de usar tanto para clientes como para el dueño.

**Métricas:**
- Cliente: Completar formulario en < 30 segundos
- Dueño: Ver gráficas con 1 clic (sin necesidad de Excel)
- Tasa de error: < 5% de formularios incompletos

---

### RAC-002: Disponibilidad
**Descripción:** El sistema debe estar disponible 24/7.

**Métricas:**
- Google Forms/Sheets: 99.9% uptime (garantizado por Google)
- WhatsApp Business: Disponible mientras el celular tenga batería
- Instagram Channel: Disponible 24/7

---

### RAC-003: Escalabilidad
**Descripción:** El sistema debe soportar crecimiento en el número de usuarios.

**Métricas:**
- Google Forms: Ilimitado (hasta 10 millones de respuestas)
- Google Sheets: Hasta 10 millones de celdas
- WhatsApp Business: Hasta 1,000 contactos en lista de difusión

---

### RAC-004: Mantenibilidad
**Descripción:** El sistema debe ser fácil de mantener y actualizar.

**Especificaciones:**
- Documentación clara en GitHub
- Manual de usuario de 1 página
- Videos tutoriales (opcional)
- Soporte del estudiante durante 13 semanas

---

## 5. Requerimientos de Seguridad

### RS-001: Privacidad de Datos del Cliente
**Descripción:** Los datos personales de los clientes deben protegerse.

**Especificaciones:**
- Campos de nombre y WhatsApp son OPCIONALES
- Los datos se almacenan en Google Sheets con acceso restringido (solo el dueño)
- No se comparten datos con terceros
- Cumplimiento con Ley Federal de Protección de Datos Personales (México)

---

### RS-002: Privacidad del Número Telefónico del Dueño
**Descripción:** El número personal del dueño no debe ser expuesto.

**Especificaciones:**
- Uso de nombre de usuario en WhatsApp Business (@suscuni)
- Enlaces wa.me/suscuni (no muestran el número)
- Los clientes solo ven el nombre del negocio, no el número

---

### RS-003: Control de Acceso
**Descripción:** Solo el dueño debe tener acceso a la base de datos completa.

**Especificaciones:**
- Google Sheets: Compartir solo con el correo del dueño
- Contraseña protegida (autenticación de Google)
- No permitir acceso público a la hoja de cálculo

---

### RS-004: Integridad de Datos
**Descripción:** Los datos no deben ser modificados accidentalmente.

**Especificaciones:**
- Google Forms: Los clientes solo pueden enviar, no editar respuestas de otros
- Google Sheets: Historial de versiones activado (permite restaurar si se borra algo)
- Copia de seguridad automática (Google Drive)

---

## 6. Otros Requerimientos

### OR-001: Cero Costo
**Descripción:** La implementación no debe tener costo económico para Suscuni.

**Especificaciones:**
- Google Forms: Gratuito
- Google Sheets: Gratuito
- WhatsApp Business: Gratuito
- Instagram Channel: Gratuito
- Canva (diseño de QR): Versión gratuita
- Única inversión: Impresión de QRs (~$50-100 MXN en imprenta local)

---

### OR-002: Sin Conocimientos Técnicos Requeridos
**Descripción:** El dueño no debe requerir conocimientos de programación o Excel.

**Especificaciones:**
- Interfaz visual de Google Sheets (sin fórmulas complejas)
- Vista de "Resumen" con gráficas automáticas
- Capacitación de 15 minutos suficiente
- Manual de usuario impreso de 1 página

---

### OR-003: Implementación en 13 Semanas
**Descripción:** El proyecto debe completarse dentro del período académico.

**Cronograma:**
- Semanas 1-2: Diagnóstico y levantamiento de requerimientos
- Semanas 3-6: Diseño y desarrollo
- Semanas 7-10: Implementación y monitoreo
- Semanas 11-13: Evaluación y cierre

---

### OR-004: Consentimiento para Código Abierto
**Descripción:** El dueño debe autorizar la publicación del proyecto en GitHub.

**Especificaciones:**
- Consentimiento verbal o escrito del dueño
- Publicación en repositorio público de GitHub
- Documentación completa en español
- Licencia MIT o Creative Commons