# 📋 AgendaGPT Mobile

> Agenda móvil de asuntos pendientes derivados de oficios, circulares y documentos administrativos — **Ciclo escolar 2026-2027**.

[![Estado](https://img.shields.io/badge/estado-activo-brightgreen)]()
[![Versión](https://img.shields.io/badge/versión-v3-blue)]()
[![PWA](https://img.shields.io/badge/PWA-instalable-1F4E79)]()
[![Licencia](https://img.shields.io/badge/licencia-uso%20interno-lightgrey)]()

---

## 🚀 Acceso rápido

**Aplicación en línea:**  
👉 https://pcantivirus2020-png.github.io/agendagpt-mobile/AgendaGPT_Mobile.html

**Instalación como app:**
- **Android (Chrome):** menú ⋮ → *Instalar aplicación*
- **iPhone (Safari):** botón Compartir → *Añadir a pantalla de inicio*

---

## 📖 Descripción

**AgendaGPT Mobile** es una aplicación web progresiva (PWA) diseñada para el personal administrativo y docente que necesita dar seguimiento a asuntos derivados de oficios y circulares oficiales.

Permite **cargar un PDF** de una circular, extraer automáticamente la información relevante (número de oficio, fechas, asunto y acciones a realizar) y agregarla a una agenda digital con cálculo automático de prioridades.

Todo el procesamiento se realiza **localmente en el dispositivo**. Ningún documento se sube a servidores externos.

---

## ✨ Características principales

### 📋 Gestión de asuntos
- ➕ Crear, ✏️ editar y 🗑️ eliminar asuntos
- 🔄 Cambiar estado (Pendiente → En proceso → Concluido)
- 📝 Campo de notas internas por asunto
- 🔗 Campo de liga / información adicional

### 🎯 Prioridad automática
| Condición | Prioridad |
|---|---|
| Estado = Concluido | 🟢 Concluida |
| Sin fecha límite | 🟡 Media |
| Vence hoy o vencido | 🔴 Crítica |
| Vence en 1–3 días | 🟠 Alta |
| Vence en 4+ días | 🟡 Media |

### 📄 Importación desde PDF
- Extracción de texto real con **PDF.js**
- **OCR en español** con Tesseract.js (para PDFs escaneados)
- Detección automática de:
  - 📄 Número de oficio / circular (incluye detección de "S/N")
  - 📅 Fecha del oficio (ubicada en el encabezado)
  - 📆 Fecha límite (con análisis de contexto)
  - 📌 Asunto / actividad
  - ✅ Acción a realizar
- Sistema de **confianza por campo** (badges de color)
- Limpieza inteligente del texto OCR

### 🔍 Búsqueda y filtros
- 🔎 Búsqueda por oficio, asunto, acción o notas
- Filtro por prioridad (Crítica / Alta / Media)
- Filtro por estado (Pendiente / En proceso / Concluido)
- Ordenamiento por urgencia, fecha, oficio o más recientes

### 📊 Exportación
- 📊 **Excel** (`.xls`) con todas las columnas
- 📄 **Word** (`.doc`) con formato tabular
- 🖨️ **Imprimir / PDF** desde el navegador

### 💾 Persistencia
- Guardado automático en `localStorage` del navegador
- Funciona **sin conexión** después de instalada
- Los datos permanecen entre sesiones

---

## 🛠️ Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| **HTML5 + CSS3** | Interfaz responsiva mobile-first |
| **JavaScript (ES2022+)** | Lógica de la aplicación |
| **PDF.js** (v4.4.168) | Extracción de texto de PDFs |
| **Tesseract.js** (v5.1.0) | OCR en español para PDFs escaneados |
| **Service Worker** | Funcionamiento offline (PWA) |
| **localStorage** | Persistencia local de asuntos |
| **GitHub Pages** | Hosting HTTPS gratuito |

Sin frameworks. Sin build step. Un solo archivo HTML autosuficiente + Service Worker.

---

## 📁 Estructura del proyecto
