# 📱 Transportes

## Descripción General

**Transportes** es una aplicación web integral diseñada para la gestión y control de operadores de transporte en la empresa IMCO. La plataforma combina un sistema de chat en tiempo real, registro de tareo diario, reportes de operadores y visualización de planillas, todo integrado con Firebase Realtime Database y Google Sheets.

---

## 🚀 Características Principales

### 🔐 **Autenticación y Control de Acceso**
- Sistema de login con usuarios autorizados
- Roles diferenciados: **ADMINISTRADOR** y operadores
- El Administrador tiene acceso a funcionalidades exclusivas como la visualización de planillas
- Persistencia de sesión

### 💬 **Chat en Tiempo Real**
- Sala de chat general para comunicación entre operadores
- Indicador de escritura en tiempo real
- Notificaciones de nuevos mensajes
- Sonidos de entrada/salida de mensajes
- Visualización de usuarios conectados

### ⏰ **Sistema de Tareo Diario**
- Registro de asistencia y horarios de operadores
- Diferenciación entre horario **corrido** y **partido**
- Cálculo automático de horas trabajadas
- Filtrado por fecha
- Eliminación de registros (solo del propio usuario)

### 📋 **Reporte de Operadores**
- Formulario completo de registro diario que incluye:
  - Fecha de registro
  - Conductor (auto-seleccionado según usuario)
  - Tipo de vehículo (camión, bus, minivan, etc.)
  - Placa del vehículo
  - Capacidad
  - Horario (corrido/partido)
  - Horas de inicio y final (A y B si es partido)
  - Kilometraje inicial y final
- Historial de registros con opción de eliminar
- Previsualización e impresión de reportes
- Envío de reportes por WhatsApp (copia al portapapeles)

### 📊 **Planilla de Control (Solo Administrador)**
- Visualización de planilla de Google Sheets
- Filtrado automático por usuario
- Acceso restringido exclusivamente para el Administrador
- Función de recarga y apertura en nueva pestaña

### 🎨 **Personalización de Interfaz**
- Selector de **tamaño de fuente** (Peq, Med, Grd, XGrd, UGrd)
- Selector de **tipografía** (Default, Mono, Sans, Serif, Rounded)
- Selector de **tema de color** (Azul, Verde, Rojo, Morado, Naranja, Rosa, Gris)
- Persistencia de preferencias en localStorage

### 🔔 **Notificaciones y Sonidos**
- Notificaciones de nuevos mensajes
- Sonidos para mensajes enviados y recibidos
- Sonido especial para registros de tareo
- Indicador visual de sonido

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Descripción |
|------------|-------------|
| **HTML5** | Estructura de la aplicación |
| **CSS3** | Estilos y temas personalizables |
| **JavaScript (Vanilla)** | Lógica de la aplicación |
| **Firebase Realtime Database** | Almacenamiento de datos en tiempo real |
| **Google Sheets API** | Visualización de planillas |
| **Font Awesome** | Iconografía |
| **html2pdf.js** | Generación de PDF para reportes |

---

## 📁 Estructura de Firebase

```json
{
  "messages": {
    "general": { /* Mensajes del chat general */ },
    "tareo": {
      "USR-001": { /* Registros de tareo por usuario */ }
    },
    "reporte": { /* Registros para Google Sheets */ }
  },
  "presence": {
    "general": { /* Usuarios conectados */ }
  },
  "typing": {
    "general": { /* Indicadores de escritura */ }
  }
}
```

---

## 👥 Usuarios Autorizados

La aplicación cuenta con **27 usuarios** autorizados, incluyendo:

- **1 Administrador** (acceso a planillas)
- **26 Operadores** (acceso a chat, tareo y reportes)

---

## 📋 Lista de Usuarios

| # | Usuario |
|---|---------|

---

## 🚗 Lista de Placas

La aplicación incluye **32 placas** de vehículos predefinidas:

```

```

---

## 🔑 Claves de Acceso

| Usuario | Clave |
|---------|-------|
| ADMINISTRADOR |  |
| Operadores |  etc. (asignadas individualmente) |

---

## 📱 Capturas de Pantalla

### Pantalla de Login
- Selector de usuario con estado de conexión
- Selector de tamaño, tema y fuente
- Campo de clave de acceso

### Chat General
- Mensajes en tiempo real
- Indicador de escritura
- Usuarios conectados
- Notificaciones

### Tareo Diario
- Visualización de registros del usuario
- Checkboxes para seleccionar y eliminar
- Filtro por fecha

### Reporte IMCO
- Formulario completo de registro
- Historial de registros
- Previsualización e impresión
- Envío a WhatsApp

### Planilla (Solo Administrador)
- Visualización de Google Sheets
- Filtro por usuario
- Recarga y apertura externa

---

## ⚙️ Configuración

### Requisitos Previos
1. Cuenta de Firebase con Realtime Database habilitada
2. Google Sheets (para planillas)
3. Navegador moderno con soporte ES6+

### Variables de Entorno
```javascript
const firebaseConfig = {
  apiKey: "AIzaSyAUwQXsM6OrnlmmzfpRDM1MetOVKW-YMIk",
  authDomain: "transportes-chat.firebaseapp.com",
  databaseURL: "https://transportes-chat-default-rtdb.firebaseio.com",
  projectId: "transportes-chat",
  storageBucket: "transportes-chat.firebasestorage.app",
  messagingSenderId: "339529351494",
  appId: "1:339529351494:web:7ad1a202d48d3905966547"
};
```

### Reglas de Firebase
```json
{
  "rules": {
    "messages": { ".read": true, ".write": true },
    "presence": { ".read": true, ".write": true },
    "typing": { ".read": true, ".write": true }
  }
}
```

---

## 📱 Compatibilidad

- **Navegadores**: Chrome, Firefox, Safari, Edge (últimas versiones)
- **Dispositivos**: Desktop, Tablet, Mobile (responsive)
- **Sistema Operativo**: Windows, macOS, Linux, iOS, Android

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork del repositorio
2. Crear una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit de tus cambios (`git commit -m 'Agrega nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abrir un Pull Request

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Ver el archivo `LICENSE` para más detalles.

---

## 👨‍💻 Autor

**Paul Manrique**

---

## 📞 Contacto

Para soporte o consultas, contactar al área de **Paul Manrique**.

---

## 🔄 Versiones

| Versión | Fecha | Descripción |
|---------|-------|-------------|
| 1.0.0 | 2026 | Lanzamiento inicial |

---

## 🏆 Agradecimientos

- Equipo de Transportes por los requisitos y pruebas
- Comunidad de Firebase por la excelente documentación
- Colaboradores y usuarios que ayudaron a mejorar la aplicación
