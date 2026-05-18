# Sistema InePro

> *Belleza con propósito · Gestión integral de ventas*

![status](https://img.shields.io/badge/status-en%20desarrollo-9A3F08?style=flat-square)
![licencia](https://img.shields.io/badge/licencia-MIT-27ae60?style=flat-square)
![node](https://img.shields.io/badge/node.js-%E2%89%A5%2020.0-27ae60?style=flat-square)
![sena](https://img.shields.io/badge/SENA-ADSO%203282766-FFB400?style=flat-square)

Sistema web de gestión de ventas para empresa de cosméticos. Proyecto formativo del programa **Tecnólogo en Análisis y Desarrollo de Software** del SENA, Centro de Gestión y Desarrollo Sostenible Surcolombiano, Pitalito, Huila.

---

## 📋 Descripción

InePro permite administrar de manera centralizada toda la operación comercial de una empresa de cosméticos: catálogo de productos, base de clientes, pedidos con sus diferentes estados, reportes de ventas mensuales y configuración general del negocio.

El sistema acompaña la marca *"Belleza con propósito"* y busca darle a la empresa una herramienta digital robusta para crecer en orden, sin depender de hojas de cálculo dispersas ni de procesos manuales.

## 🛠️ Stack tecnológico

| Capa | Tecnología |
|---|---|
| **Front-end** | HTML5, CSS3, JavaScript (ES6+) |
| **Back-end** | Node.js + Express.js |
| **Base de datos** | MySQL 8 |
| **Despliegue** | Netlify (front) + Render (back) |
| **Librerías clave** | Chart.js · JWT · bcrypt |

## 👥 Equipo de desarrollo

| Integrante | Rol |
|---|---|
| **Angélica Saraith Herrera Osorio** | Líder técnica · Front-end |
| **Martha Leonor Osorio Gómez** | Back-end · Documentación |

**Instructor:** Jhon Faiber Cerquera Sánchez  
**Ficha:** 3282766

## 🚀 Cómo correr el proyecto localmente

> ⚠️ El back-end se encuentra en desarrollo activo. Por ahora solo el front-end está funcional.

```bash
# 1. Clonar el repositorio
git clone https://github.com/angelicasaraith13-glitch/sistema-inepro.git
cd sistema-inepro

# 2. Instalar dependencias (cuando el back-end esté listo)
npm install

# 3. Configurar variables de entorno
cp .env.example .env
# editar .env con los datos de tu MySQL local

# 4. Correr en modo desarrollo
npm run dev
```

## 🌿 Flujo de versionamiento

El equipo trabaja bajo el modelo **GitHub Flow + develop**:

- `main` → producción estable (despliegue automático)
- `develop` → integración del equipo
- `feature/*` → nuevas funcionalidades
- `fix/*` → correcciones
- `docs/*` → cambios de documentación

Para más detalles consulta [CONTRIBUTING.md](./CONTRIBUTING.md) o el informe completo *GA7-220501096-AA1-EV01: Plan de Versionamiento*.

## 📝 Convención de commits

Seguimos [**Conventional Commits 1.0.0**](https://www.conventionalcommits.org/es/v1.0.0/):

```
feat(pedidos): agrega filtro por rango de fechas
fix(login): corrige redireccion tras autenticar
docs(readme): actualiza instrucciones de instalacion
```

## 📁 Estructura del repositorio

```
sistema-inepro/
├── .github/             # plantillas de PRs e issues
├── docs/                # documentación técnica
├── frontend/            # código del front-end
├── backend/             # código del back-end (en construcción)
├── database/            # scripts SQL del modelo de datos
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## 🎓 Cadena de evidencias del programa

Este repositorio es parte del recorrido formativo del Tecnólogo ADSO:

- **GA3** — Modelo entidad-relación y script SQL
- **GA4** — Diagramas UML
- **GA5** — Pruebas de software
- **GA6-EV02** — Componentes front-end (Dulce Maestría)
- **GA6-EV03** — Implementación front-end del Sistema InePro
- **GA7-AA1-EV01** ← *estamos aquí* — Plan de versionamiento
- **GA7-AA2 y siguientes** — Construcción del software

## 📄 Licencia

Distribuido bajo licencia **MIT**. Ver [LICENSE](./LICENSE) para más detalles.

---

<p align="center">
  <sub>Hecho con ❤️ en Pitalito, Huila · SENA 2026</sub>
</p>
