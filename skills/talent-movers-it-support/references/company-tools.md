# Herramientas de negocio de Talent Movers (fuera de Microsoft 365)

Estas herramientas **no usan SSO de Microsoft 365** — cada una tiene su propio usuario/contraseña independiente. Esto significa que el asistente **nunca puede leer ni actuar sobre estas cuentas directamente** (no hay ningún MCP server conectado a ellas todavía). Para cualquier problema de acceso en estas herramientas, la única opción es guiar el self-service de la propia plataforma o escalar a un ticket para que lo resuelva quien administra esa herramienta en Talent Movers.

| Herramienta | Para qué se usa | Quién la administra | URL de "olvidé mi contraseña" |
|---|---|---|---|
| **Breezy HR** | Reclutamiento / CRM de candidatos | José Manuel | https://app.breezy.hr/forgot-password |
| **Microsoft Teams** | Comunicación interna (sí usa SSO de M365, es la excepción de esta tabla — ver sección Entra ID del SKILL.md) | José Manuel (admin de Entra ID) | (self-service de Microsoft 365, no aplica aquí) |
| **MightyCall** | Llamadas (en proceso de migración a Twilio — mantener ambas mientras dure la transición) | José Manuel | https://panel.mightycall.com/MightyCall/Login/RetrieveLogin |
| **Twilio** | Llamadas (reemplazo de MightyCall, en migración) | Ivo | https://www.twilio.com/reset-password |
| **HubSpot** | Ventas | Gipson (o José Manuel bajo autorización de Gipson) | En app.hubspot.com/login, clic en "Forgot password" bajo el campo de contraseña |
| **PandaDoc** | Envío y firma de contratos | José Manuel | En pandadoc.com → Login → "Forgot Password?" |
| **Didit** | KYC (verificación de identidad) y data vault | José Manuel | No tiene URL pública de self-service — la consola de negocio (business.didit.me) usa login por correo; si un empleado no puede entrar, siempre es ticket para José Manuel, no self-service |

## Cómo manejar solicitudes sobre estas herramientas

**1. Olvidé mi contraseña / no puedo entrar (pero la cuenta existe y no está desactivada):**
Trátalo como categoría 1 (FAQ) — indica al empleado que use el flujo de "olvidé mi contraseña" de la propia herramienta (link en la tabla de arriba, una vez completada). No necesitas ticket para esto, es exactamente igual de self-service que el reset de Microsoft 365.

**2. Necesito una cuenta nueva / mi cuenta está desactivada / necesito cambiar mis permisos dentro de la herramienta:**
Esto **no pasa por el flujo de Entra ID** (esa herramienta no vive en Entra ID), pero aplica el mismo principio de fondo: tú no puedes crear ni modificar estas cuentas, así que siempre se resuelve como ticket en FreeScout, dirigido específicamente a quien administra esa herramienta según la tabla de arriba (menciónalo por nombre en el asunto o la nota del ticket, ej. "Para: José Manuel" o "Para: Gipson"). Incluye en el ticket qué herramienta es, qué necesita el empleado exactamente, y por qué.

Nota sobre HubSpot: como el acceso lo administra Gipson (o José Manuel solo bajo su autorización), cualquier solicitud sobre HubSpot debe dejar claro en el ticket que necesita el visto bueno de Gipson antes de ejecutarse — no asumas que José Manuel puede resolverlo unilateralmente aunque también tenga acceso.

**3. Didit específicamente — cuidado extra:**
Didit maneja KYC y es el data vault de la empresa — datos sensibles de identidad. Si un empleado te pide algo relacionado con acceso a Didit o a los datos que contiene, sé especialmente conservador: nunca asumas que una solicitud es rutinaria solo porque parece un simple problema de acceso — siempre escala a ticket, y menciona explícitamente en el ticket que se trata de un sistema de KYC/datos sensibles para que quien lo revise le dé la prioridad de seguridad que corresponde.

---
Con esto, todos los administradores de la tabla están confirmados.
