# 🏛️ Sistema de Gestión Administrativa - DIF Negrete

[![React](https://img.shields.io/badge/React-19.2-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-6.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![NestJS](https://img.shields.io/badge/NestJS-11.0-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)](https://nestjs.com/)
[![Prisma](https://img.shields.io/badge/Prisma-7.7-2D3748?style=for-the-badge&logo=prisma&logoColor=white)](https://www.prisma.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.2-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-8.0-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)

> **Nota:** Este es un proyecto privado desarrollado para el **DIF Municipal de Negrete, Veracruz**. Esta documentación tiene fines de exhibición profesional.

Una solución integral para la digitalización de procesos administrativos gubernamentales, reemplazando el flujo de trabajo basado en hojas de cálculo con una plataforma web moderna, segura y escalable.

---

## 🌟 Características Principales

*   **🔐 Autenticación Robusta:** Sistema multi-rol (ADMIN, PADRON) con JWT y seguridad avanzada.
*   **📋 Gestión de Alumnos:** Registro centralizado mediante CURP para evitar duplicados y detectar reingresos automáticamente.
*   **🎨 Talleres Comunitarios:** Catálogo dinámico categorizado por Cultura, Deporte, Oficio, etc.
*   **👨‍🏫 Control de Instructores:** Gestión de maestros internos y externos con vinculación a grupos.
*   **👥 Organización de Grupos:** Control de cupos, horarios, periodos y asignación de aulas.
*   **💳 Sistema de Inscripciones:** Proceso atómico que vincula alumno-grupo, gestiona pagos y genera folios únicos.
*   **📅 Registro de Asistencia:** Control diario digital con histórico consultable.
*   **📊 Dashboard Estadístico:** Visualización de datos en tiempo real mediante gráficas interactivas.

---

## 🛠️ Stack Tecnológico

### Frontend
- **Framework:** React 19 (Vite)
- **Lenguaje:** TypeScript
- **Estilos:** Tailwind CSS (Arquitectura de diseño responsivo)
- **Gestión de Estado:** Zustand & React Query (TanStack)
- **Formularios:** React Hook Form + Zod (Validación estricta)
- **Gráficas:** Recharts

### Backend
- **Framework:** NestJS 11 (Arquitectura Modular & Clean Architecture)
- **ORM:** Prisma 7 (PostgreSQL)
- **Seguridad:** Passport.js (JWT), Bcrypt, Throttler
- **Validación:** Class-validator & Class-transformer

### Infraestructura & DevOps
- **Backend:** Railway (CI/CD)
- **Frontend:** Vercel
- **Base de Datos:** Supabase (PostgreSQL)

---

## 🏗️ Arquitectura del Sistema

El sistema sigue una arquitectura de **microservicios lógicos** dentro de un monorepo, asegurando la escalabilidad y mantenibilidad.

```
.
├── backend/          # NestJS API & Prisma Schema
│   ├── src/
│   │   ├── auth/     # Autenticación & Guards
│   │   ├── users/    # Gestión de usuarios del sistema
│   │   └── padron/   # Lógica de negocio (Core)
└── frontend/         # React SPA
    └── src/
        ├── api/      # Clientes Axios & Hooks
        ├── components/ # UI Atómica
        └── pages/     # Vistas de la aplicación
```

---

## 📸 Showcase

> *Se recomienda añadir capturas de pantalla de alta resolución para demostrar la interfaz.*

| Login | Dashboard |
|:---:|:---:|
| ![Login](/login.png) | ![Dashboard](/dashboard.png) |

| Inscripción | Listado de Grupos |
|:---:|:---:|
| ![Inscripción](/inscripcion.png) | ![Grupos](/grupos.png) |

---

## 🛡️ Seguridad

El sistema implementa múltiples capas de seguridad:
- ✅ **JWT HttpOnly Cookies:** Para mitigar ataques XSS.
- ✅ **Rate Limiting:** Protección contra fuerza bruta en login.
- ✅ **Validación de Esquemas:** Zod y Class-validator para saneamiento de entradas.
- ✅ **Roles y Permisos:** Control de acceso granular a nivel de endpoint y UI.
- ✅ **Parcheado:** Vulnerabilidades conocidas de dependencias han sido mitigadas.

---

## ✒️ Autor

**Arturo Baez Solano** - *Fullstack Developer & Product Owner*

---
© 2026 Velantex
