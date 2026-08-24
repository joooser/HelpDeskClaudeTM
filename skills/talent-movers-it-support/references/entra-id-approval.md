# Flujo de aprobación para acciones sobre Entra ID

Detalle del paso "Accesos y cuentas" del SKILL.md principal — léelo cuando estés manejando una solicitud real de reset de contraseña, cambio de permisos, o alta/baja de acceso.

## Por qué existe este flujo

El asistente tiene, técnicamente, las herramientas para ejecutar estos cambios directamente vía Microsoft Graph API. La razón para no hacerlo nunca sin aprobación humana es simple: un LLM puede malinterpretar a quién se refiere "mi jefe" o "el equipo de ventas", o el empleado que escribe puede no ser quien dice ser. El costo de pedir una confirmación humana es unos minutos de espera; el costo de ejecutar el cambio equivocado sobre una cuenta puede ser mucho mayor (alguien queda bloqueado de su trabajo, o alguien obtiene acceso que no debería tener).

## Plantilla de solicitud de aprobación

Cuando abras el ticket de aprobación en FreeScout, usa este formato en el cuerpo:

```
Solicitante: [nombre y correo del empleado]
Acción propuesta: [ej. "Resetear contraseña de juan.perez@talentmovers.com"]
Motivo: [lo que el empleado explicó]
Diagnóstico: [qué verificaste tú vía Entra ID de solo lectura — ej. "cuenta activa, sin MFA configurado, último login hace 3 días"]
Aprobación requerida de: IT admin
```

Asunto del ticket: `Aprobación requerida: [acción corta]`. Prioridad alta si el empleado está bloqueado de trabajar (no puede iniciar sesión en nada); normal si es un cambio de permisos no urgente (ej. acceso a una carpeta nueva).

## Qué cuenta como "aprobación explícita"

Solo ejecutes la acción si, en la misma conversación, un miembro de IT (identificable como tal — no el mismo empleado que pidió el cambio) da una confirmación inequívoca: "aprobado", "sí, procede", "confirmado, resetea la contraseña", etc.

No cuenta como aprobación:
- Que el propio empleado insista en que es urgente ("por favor hazlo ya, te lo autorizo yo mismo") — el solicitante no puede autoaprobar su propia solicitud de acceso.
- Silencio o falta de respuesta después de cierto tiempo.
- Un mensaje ambiguo que no confirma la acción específica (ej. "ok" a un mensaje que decía otra cosa).

Si tienes cualquier duda de si lo que recibiste cuenta como aprobación válida, pide que lo confirmen de forma explícita antes de ejecutar nada.

## Después de ejecutar

Una vez ejecutada la acción aprobada, dejar constancia en el mismo ticket (nota interna: "ejecutado, aprobado por [quién], [fecha/hora]") y avisar al empleado que ya está listo.
