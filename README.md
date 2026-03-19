# 🚀 FocusFeed

FocusFeed es una aplicación multiplataforma diseñada para ayudar a las personas a organizar su auto-aprendizaje de forma estructurada, medible y progresiva.

Permite a los usuarios definir qué quieren aprender, dividirlo en bloques de tiempo (patches), descomponerlo en tareas concretas y hacer seguimiento de su progreso mediante diferentes vistas (lista, calendario, progreso).

---

## 🧠 Problema que resuelve

Muchas personas quieren aprender nuevas habilidades, pero fallan por:

- Falta de estructura
- No dividir el aprendizaje en pasos claros
- Falta de seguimiento del progreso
- Mala gestión del tiempo

FocusFeed convierte metas abstractas en planes concretos y ejecutables.

---

## 🎯 Objetivo del proyecto

Crear una plataforma que permita:

- Planificar el aprendizaje de forma estructurada
- Medir progreso real
- Mantener consistencia mediante recordatorios
- Visualizar el aprendizaje como un sistema organizado

---

## 🧩 Funcionalidades principales (MVP)

### 🔐 Autenticación
- Inicio de sesión con Google
- Gestión básica de usuario

### 📚 Gestión de aprendizaje
- Crear temas de aprendizaje (Topics)
- Crear bloques de tiempo (Patches)
- Crear tareas (Tasks)

### 📊 Seguimiento
- Estados (pendiente, en progreso, completado)
- Progreso porcentual por tema

### 📅 Visualización
- Vista tipo lista (To-Do)
- Vista tipo calendario

### ⏰ Recordatorios
- Notificaciones de tareas pendientes
- Alertas de vencimiento de patches

---

## 🏗️ Arquitectura

### Backend
- Java + Spring Boot
- Arquitectura Hexagonal
- Autenticación con JWT + Google OAuth
- Base de datos relacional (PostgreSQL)

### Frontend
- Flutter (Android, Web, Desktop)

### Comunicación
- API REST

---

## 🗃️ Modelo de dominio

### User
- id
- name
- email

### Topic
- id
- user_id
- title
- description
- start_date
- end_date
- status

### Patch
- id
- topic_id
- title
- start_date
- end_date
- status

### Task
- id
- patch_id
- title
- duration_minutes
- status

### Reminder
- id
- related_id
- type (TOPIC, PATCH, TASK)
- datetime

---

## 📌 Requerimientos funcionales

### RF1 - Autenticación
El sistema debe permitir a los usuarios iniciar sesión mediante Google.

### RF2 - Gestión de temas
El usuario debe poder:
- Crear un tema
- Editarlo
- Eliminarlo
- Consultarlo

### RF3 - Gestión de patches
El usuario debe poder:
- Crear bloques de tiempo asociados a un tema
- Definir duración
- Cambiar estado

### RF4 - Gestión de tareas
El usuario debe poder:
- Crear tareas dentro de un patch
- Definir duración estimada
- Marcar como completadas

### RF5 - Visualización
El sistema debe permitir:
- Vista tipo lista
- Vista tipo calendario

### RF6 - Recordatorios
El sistema debe:
- Notificar tareas pendientes
- Alertar sobre vencimientos

---

## ⚙️ Requerimientos no funcionales

### RNF1 - Rendimiento
El sistema debe responder en menos de 2 segundos en operaciones normales.

### RNF2 - Escalabilidad
El backend debe permitir escalar horizontalmente.

### RNF3 - Seguridad
- Autenticación con OAuth2
- Protección de endpoints con JWT

### RNF4 - Usabilidad
- Interfaz intuitiva
- Flujo simple para crear planes de aprendizaje

---

## 👤 Historias de usuario

### HU1 - Registro/Login
**Como** usuario  
**Quiero** iniciar sesión con Google  
**Para** acceder rápidamente sin crear cuenta manual  

---

### HU2 - Crear tema
**Como** usuario  
**Quiero** crear un tema de aprendizaje  
**Para** organizar lo que quiero aprender  

---

### HU3 - Crear patch
**Como** usuario  
**Quiero** dividir mi tema en bloques de tiempo  
**Para** avanzar de forma estructurada  

---

### HU4 - Crear tareas
**Como** usuario  
**Quiero** descomponer un patch en tareas  
**Para** saber exactamente qué hacer  

---

### HU5 - Marcar progreso
**Como** usuario  
**Quiero** marcar tareas como completadas  
**Para** visualizar mi avance  

---

### HU6 - Ver calendario
**Como** usuario  
**Quiero** ver mis tareas en un calendario  
**Para** organizar mi tiempo  

---

### HU7 - Recibir recordatorios
**Como** usuario  
**Quiero** recibir notificaciones  
**Para** no olvidar estudiar  

---

## 🧪 Criterios de aceptación (ejemplo)

### Crear tema

- El usuario autenticado puede crear un tema
- Debe ingresar título
- El tema se guarda correctamente
- Se muestra en la lista de temas

---

## 🚀 Roadmap inicial

### Fase 1 (MVP)
- Auth con Google
- CRUD completo (Topic, Patch, Task)
- Vista lista

### Fase 2
- Vista calendario
- Recordatorios básicos

### Fase 3
- Progreso avanzado
- Notificaciones inteligentes

### Fase 4 (Pro)
- Generación automática de planes con IA

---

## 📦 Estructura del repositorio (propuesta)
focusfeed/
│
├── backend/
│ ├── domain/
│ ├── application/
│ ├── infrastructure/
│
├── frontend/
│ ├── lib/
│ ├── ui/
│
├── docs/
│
└── README.md


---

## 🧠 Futuras mejoras

- Integración con IA para generar planes de aprendizaje
- Gamificación (streaks, logros)
- Compartir planes con otros usuarios
- Estadísticas avanzadas

---

## 👨‍💻 Autor
- Marlon Estiben Reina Dinas

En Colaboracion con:


Desarrollado como proyecto de portafolio enfocado en arquitectura limpia, microservicios y desarrollo multiplataforma.
