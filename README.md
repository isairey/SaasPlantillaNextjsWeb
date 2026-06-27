# 🚀 Next.js SaaS Starter

Una plantilla moderna para desarrollar aplicaciones **SaaS** utilizando **Next.js**, diseñada para acelerar el desarrollo de plataformas web con autenticación, gestión de usuarios, pagos mediante Stripe y un panel administrativo completamente funcional.

Ideal para crear productos SaaS escalables, seguros y listos para producción.

---

# ✨ Características

* 🌐 Landing Page moderna y responsive
* 💳 Integración con Stripe Checkout
* 👤 Registro e inicio de sesión de usuarios
* 🔐 Autenticación mediante JWT
* 🍪 Manejo seguro de sesiones mediante Cookies
* 📊 Dashboard privado para usuarios autenticados
* 👥 Gestión de usuarios y equipos
* 🛡️ Control de acceso basado en roles (RBAC)
* 📦 Gestión de suscripciones
* 💰 Portal de clientes de Stripe
* ⚡ Middleware global para proteger rutas privadas
* ✅ Validación de datos con Zod
* 📝 Sistema de registro de actividades (Logs)
* 🚀 Preparado para producción

---

# 🛠 Tecnologías Utilizadas

### Frontend

* Next.js
* React
* TypeScript
* shadcn/ui

### Backend

* Next.js API Routes
* Drizzle ORM
* PostgreSQL

### Servicios

* Stripe
* JWT Authentication
* Cookies
* Zod

---

# 📂 Estructura del Proyecto

```text
📦SaasPlantillaNextjsWeb
│
├── app/
│
├── components/
│
├── db/
│
├── lib/
│
├── middleware/
│
├── public/
│
├── styles/
│
├── drizzle/
│
└── README.md
```

---

# 🚀 Instalación

## 1. Clonar el repositorio

```bash
git clone https://github.com/isairey/SaasPlantillaNextjsWeb.git
```

---

## 2. Entrar al proyecto

```bash
cd SaasPlantillaNextjsWeb
```

---

## 3. Instalar dependencias

```bash
pnpm install
```

---

# ⚙ Configuración del Proyecto

## Configurar Stripe CLI

Instala Stripe CLI e inicia sesión:

```bash
stripe login
```

---

## Crear archivo de variables de entorno

```bash
pnpm db:setup
```

---

## Ejecutar migraciones

```bash
pnpm db:migrate
```

---

## Poblar la base de datos

```bash
pnpm db:seed
```

Se creará un usuario de prueba:

| Usuario                               | Contraseña |
| ------------------------------------- | ---------- |
| [test@test.com](mailto:test@test.com) | admin123   |

También puedes crear nuevos usuarios desde:

```
/sign-up
```

---

# ▶ Ejecutar el Proyecto

```bash
pnpm dev
```

La aplicación estará disponible en:

```
http://localhost:3000
```

---

# 💳 Integración con Stripe

El proyecto incorpora Stripe para gestionar pagos y suscripciones.

Incluye:

* Checkout
* Portal del Cliente
* Suscripciones
* Renovaciones
* Cancelaciones
* Webhooks

Para escuchar eventos de Stripe localmente:

```bash
stripe listen --forward-to localhost:3000/api/stripe/webhook
```

---

# 💳 Tarjeta de Prueba

Puedes utilizar la siguiente tarjeta para realizar pagos de prueba:

| Campo  | Valor                         |
| ------ | ----------------------------- |
| Número | 4242 4242 4242 4242           |
| Fecha  | Cualquier fecha futura        |
| CVC    | Cualquier número de 3 dígitos |

---

# 🔐 Sistema de Autenticación

La plataforma incorpora:

* Registro de usuarios
* Inicio de sesión
* JWT
* Cookies seguras
* Protección de rutas
* Middleware global
* Middleware para Server Actions
* Validación mediante Zod

---

# 👥 Gestión de Usuarios

Los usuarios pueden:

* Crear cuentas
* Iniciar sesión
* Editar información
* Crear equipos
* Gestionar miembros
* Administrar permisos

---

# 📊 Dashboard

Una vez autenticado, cada usuario tiene acceso a un panel privado con:

* Información de su cuenta
* Gestión de equipos
* CRUD de usuarios
* Estado de suscripciones
* Historial de actividades

---

# 🛡 Control de Acceso

El sistema implementa RBAC (Role Based Access Control).

Roles disponibles:

* 👑 Owner
* 👤 Member

Cada rol posee permisos específicos sobre la plataforma.

---

# 📋 Registro de Actividades

Todas las acciones importantes realizadas por los usuarios pueden almacenarse mediante un sistema de logs, facilitando el seguimiento y auditoría de eventos.

---

# 🚀 Despliegue

El proyecto está preparado para desplegarse fácilmente en plataformas como:

* Vercel
* Railway
* Render
* DigitalOcean
* VPS
* Docker

Antes de publicar en producción se recomienda:

* Configurar un Webhook de Stripe.
* Definir las variables de entorno de producción.
* Configurar PostgreSQL.
* Generar un `AUTH_SECRET` seguro.

---

# 📈 Escalabilidad

La arquitectura permite escalar fácilmente gracias a:

* Next.js App Router
* Middleware
* PostgreSQL
* Drizzle ORM
* Componentes reutilizables
* Separación entre lógica y presentación
* Integración con Stripe

---

# 👨‍💻 Desarrollado con

* Next.js
* React
* TypeScript
* PostgreSQL
* Drizzle ORM
* Stripe
* JWT
* Zod
* shadcn/ui

---

# 📄 Licencia

Este proyecto puede utilizarse como base para el desarrollo de aplicaciones SaaS modernas, permitiendo su personalización y ampliación según las necesidades de cada proyecto.
