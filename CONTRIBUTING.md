# 🤝 Guía de Contribución — Sistema InePro

Este documento resume las convenciones de trabajo del equipo. Si vas a contribuir al proyecto (aunque sea cambiando una sola línea), lee esto primero.

> 📘 Para el detalle completo y la justificación de cada decisión, consulta el informe **GA7-220501096-AA1-EV01: Plan de Versionamiento**.

---

## 🌿 Estructura de ramas

| Rama | Propósito | Vida |
|---|---|---|
| `main` | Producción estable (Netlify/Vercel) | Permanente |
| `develop` | Integración del equipo | Permanente |
| `feature/*` | Nuevas funcionalidades | Corta (1-5 días) |
| `fix/*` | Correcciones de errores | Corta (horas-días) |
| `docs/*` | Cambios de documentación | Corta (horas) |
| `refactor/*` | Reorganización sin cambio funcional | Corta |
| `test/*` | Mejoras o nuevas pruebas | Corta |
| `chore/*` | Mantenimiento del proyecto | Corta |
| `hotfix/*` | Correcciones urgentes en producción | Excepcional |

### Reglas de nombrado de ramas

✅ **Formato:** `<tipo>/<descripcion-corta-en-kebab-case>`

```
feature/login-jwt
fix/total-pedido-redondeo
docs/actualiza-readme
chore/actualiza-eslint
```

❌ **Evitar:**
- Mayúsculas, tildes, ñ, espacios o caracteres especiales
- Nombres genéricos: `cambios`, `nuevo`, `arreglo`
- Sin prefijo de tipo: `login-jwt` (debe ser `feature/login-jwt`)

---

## 💬 Mensajes de commit — Conventional Commits

Adoptamos el estándar [**Conventional Commits 1.0.0**](https://www.conventionalcommits.org/es/v1.0.0/).

### Formato

```
<tipo>(<ambito opcional>): <descripcion en imperativo>

<cuerpo opcional con detalle>

<footer opcional con referencias a issues>
```

### Tipos válidos

| Tipo | Significado |
|---|---|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de un error |
| `docs` | Cambios en documentación |
| `refactor` | Refactor sin cambio funcional |
| `test` | Pruebas |
| `chore` | Mantenimiento |
| `style` | Solo formato/estilo |

### Reglas

- Descripción en **imperativo presente**, **en español**
- Máximo **72 caracteres** en el título
- Si rompe compatibilidad, marca con `!`: `feat!: rediseña endpoint de pedidos`
- Si cierra un issue, agrégalo en footer: `Closes #14`

### Ejemplos

✅ **Bueno:**

```
feat(pedidos): agrega filtro por rango de fechas

Permite al usuario filtrar la lista de pedidos seleccionando
una fecha de inicio y una fecha de fin. El filtro se combina
con el filtro existente de estado.

Closes #34
```

❌ **Malo:**

```
cambios varios
```

```
ARREGLE UN BUG MUY GRAVE PORFA REVISEN
```

---

## 🔁 Flujo paso a paso de una funcionalidad

1. **Sincronizar develop:** `git checkout develop && git pull origin develop`
2. **Crear rama:** `git checkout -b feature/mi-nueva-funcionalidad`
3. **Trabajar y hacer commits frecuentes** siguiendo Conventional Commits
4. **Push de la rama:** `git push -u origin feature/mi-nueva-funcionalidad`
5. **Abrir Pull Request** hacia `develop` (no hacia `main`)
6. **Llenar la plantilla** y asignar reviewer
7. **Esperar revisión** (máximo 24h hábiles)
8. **Aplicar cambios** si la revisión los solicita
9. **Merge con "Squash and merge"** cuando esté aprobado
10. **Eliminar la rama local:** `git branch -d feature/mi-nueva-funcionalidad`

---

## 👀 Proceso de Pull Requests

### Antes de abrir el PR
- ✅ Tu rama está actualizada con `develop`
- ✅ El código compila/corre sin errores
- ✅ Las pruebas pasan
- ✅ Los commits siguen Conventional Commits

### Al abrir el PR
- ✅ Título sigue formato Conventional Commits
- ✅ Llenas la plantilla de PR completa
- ✅ Asignas a la otra integrante como reviewer obligatoria
- ✅ Etiquetas con labels (`frontend`, `backend`, `database`, etc.)

### Durante la revisión
- ⏱ La reviewer responde en máximo **24h hábiles**
- 💬 Los comentarios son constructivos y educativos
- 🔁 Aplica cambios en nuevos commits (no fuerza-push)

### Para mergear
- 📦 Estrategia: **"Squash and merge"** por defecto
- 🗑 La rama feature se elimina automáticamente
- 👤 El merge lo hace preferiblemente la autora del PR

---

## 📁 Archivos obligatorios del repositorio

- ✅ `README.md` — Documento de entrada
- ✅ `.gitignore` — Lo que NO se versiona
- ✅ `LICENSE` — Licencia MIT
- ✅ `CONTRIBUTING.md` — Este archivo
- ✅ `.env.example` — Plantilla de variables de entorno
- ✅ `.github/pull_request_template.md`
- ✅ `.github/ISSUE_TEMPLATE/bug.md`
- ✅ `.github/ISSUE_TEMPLATE/feature.md`

---

## 🆘 ¿Dudas?

Si tienes dudas sobre las convenciones, pregúntale primero a la otra integrante del equipo. Si la duda persiste, escríbele al instructor Jhon Faiber.

**Recuerda:** las convenciones existen para que el repositorio sea consistente y legible. Cuando llega la prisa, son lo primero que se quiere romper, y son justamente lo que más vale la pena respetar en esos momentos.
