# Herramientas de negocio de Talent Movers (fuera de Microsoft 365)

Estas herramientas **no usan SSO de Microsoft 365** — cada una tiene su propio usuario/contraseña independiente. Esto significa que el asistente **nunca puede leer ni actuar sobre estas cuentas directamente** (no hay ningún MCP server conectado a ellas todavía). Para cualquier problema de acceso en estas herramientas, la única opción es guiar el self-service de la propia plataforma o escalar a un ticket para que lo resuelva quien administra esa herramienta en Talent Movers.

| Herramienta | Para qué se usa | Quién la administra (completar) | URL de "olvidé mi contraseña" (completar) |
|---|---|---|---|
| **Breezy HR** | Reclutamiento / CRM de candidatos | — | — |
| **Microsoft Teams** | Comunicación interna (sí usa SSO de M365, es la excepción de esta tabla — ver sección Entra ID del SKILL.md) | — | — |
| **MightyCall** | Llamadas (en proceso de migración a Twilio — mantener ambas mientras dure la transición) | — | — |
| **Twilio** | Llamadas (reemplazo de MightyCall, en migración) | — | — |
| **HubSpot** | Ventas | — | — |
| **PandaDoc** | Envío y firma de contratos | — | — |
| **Didit** | KYC (verificación de identidad) y data vault | — | — |

## Cómo manejar solicitudes sobre estas herramientas

**1. Olvidé mi contraseña / no puedo entrar (pero la cuenta existe y no está desactivada):**
Trátalo como categoría 1 (FAQ) — indica al empleado que use el flujo de "olvidé mi contraseña" de la propia herramienta (link en la tabla de arriba, una vez completada). No necesitas ticket para esto, es exactamente igual de self-service que el reset de Microsoft 365.

**2. Necesito una cuenta nueva / mi cuenta está desactivada / necesito cambiar mis permisos dentro de la herramienta:**
Esto **no pasa por el flujo de Entra ID** (esa herramienta no vive en Entra ID), pero aplica el mismo principio de fondo: tú no puedes crear ni modificar estas cuentas, así que siempre se resuelve como ticket en FreeScout dirigido a quien administra esa herramienta específica (completar en la tabla quién es, por ahora dirígelo genéricamente a IT). Incluye en el ticket qué herramienta es, qué necesita el empleado exactamente, y por qué.

**3. Didit específicamente — cuidado extra:**
Didit maneja KYC y es el data vault de la empresa — datos sensibles de identidad. Si un empleado te pide algo relacionado con acceso a Didit o a los datos que contiene, sé especialmente conservador: nunca asumas que una solicitud es rutinaria solo porque parece un simple problema de acceso — siempre escala a ticket, y menciona explícitamente en el ticket que se trata de un sistema de KYC/datos sensibles para que quien lo revise le dé la prioridad de seguridad que corresponde.

---
**Nota para quien mantiene este archivo:** llenar la columna de "quién administra" y los links de reset en cuanto se tenga esa información — mientras tanto, cualquier escalación a ticket sobre estas herramientas debe ir dirigida genéricamente a IT, quien la redirigirá a quien corresponda.
