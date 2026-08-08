# Arquitectura de la Solución - Suscuni

## Diagrama de Componentes

```mermaid
graph TB
    subgraph "CAPA DE PRESENTACIÓN"
        A[Cliente - Smartphone]
        B[Dueño - Laptop/Celular]
    end
    
    subgraph "CAPA DE ENTRADA"
        C[QR en Mesas]
        D[WhatsApp Business]
        E[Instagram Channel]
    end
    
    subgraph "CAPA DE APLICACIÓN - GOOGLE"
        F[Google Forms<br/>Formulario Visual]
        G[Google Sheets<br/>Base de Datos]
        H[Google Apps Script<br/>Automatización]
    end
    
    subgraph "CAPA DE COMUNICACIÓN"
        I[WhatsApp Business API<br/>Mensajes Automáticos]
        J[Instagram API<br/>Canal de Difusión]
    end
    
    subgraph "CAPA DE DATOS"
        K[Google Drive<br/>Almacenamiento]
        L[GitHub<br/>Repositorio y Docs]
    end
    
    subgraph "CAPA DE PRESENTACIÓN - SALIDA"
        M[Dashboard Google Sheets<br/>Gráficas Automáticas]
        N[Reportes PDF<br/>KPIs y Métricas]
    end
    
    A --> C
    C --> F
    D --> I
    E --> J
    F --> G
    G --> H
    H --> M
    I --> G
    J --> E
    G --> K
    L --> B
    M --> B
    N --> B
    
    style A fill:#f9f,stroke:#333
    style B fill:#bbf,stroke:#333
    style M fill:#bfb,stroke:#333
```
## Descripción de Componentes

### 1. Servidores de Aplicación
- **Google Forms:** Servidor de formularios en la nube
- **Google Sheets:** Servidor de base de datos y cálculo
- **WhatsApp Business API:** Servidor de mensajería
- **GitHub:** Servidor de repositorio y control de versiones

### 2. Servidores Web
- **Google Drive:** Almacenamiento de archivos
- **Instagram:** Plataforma de redes sociales
- **Travis-CI:** Servidor de integración continua

### 3. Repositorios
- **GitHub:** `github.com/[tu-usuario]/proyecto-suscuni`
  - Branches: main, develop, master
  - Issues: Gestión de requerimientos
  - Projects: Tablero Kanban
  - Wiki: Documentación técnica

### 4. Clientes
- **Cliente Final:** Smartphone con cámara y navegador
- **Coach Empresarial:** Laptop o smartphone para ver dashboards
- **Estudiante:** Laptop para desarrollo y gestión

## Flujo de Datos

1. Cliente escanea QR → Google Forms
2. Google Forms → Google Sheets (automático)
3. Google Sheets → Gráficas automáticas
4. Dueño consulta Google Sheets → Toma decisiones
5. Dueño publica en Instagram → Clientes reciben
6. Cliente escribe WhatsApp → Respuesta automática
7. Todo documentado en GitHub → Trazabilidad

## Tecnologías Utilizadas

| Capa | Tecnología | Función |
|------|------------|---------|
| Frontend | Google Forms | Captura de datos |
| Backend | Google Sheets | Procesamiento y almacenamiento |
| Automatización | Google Apps Script | Scripts automáticos |
| Comunicación | WhatsApp Business | Mensajería automatizada |
| Difusión | Instagram Channel | Anuncios |
| Documentación | GitHub | Repositorio y control |
| CI/CD | Travis-CI | Integración continua |

## Seguridad

- **Autenticación:** Cuentas de Google del dueño
- **Autorización:** Acceso restringido a Google Sheets
- **Encriptación:** HTTPS en todas las plataformas
- **Privacidad:** Datos de clientes opcionales
- **Respaldo:** Google Drive (automático)
