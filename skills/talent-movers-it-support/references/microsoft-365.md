# Microsoft 365 / Teams / Entra ID

Administrador en Talent Movers: **José Manuel** (ver `company-tools.md`).

## Olvidé mi contraseña (todavía veo la pantalla de login normal)
Esto es self-service, el empleado lo puede resolver solo:
1. Ir a la pantalla de login de Microsoft 365 y hacer clic en "¿Olvidó su contraseña?" / "Forgot my password".
2. Completar la verificación con MFA (código de la app Authenticator, SMS, o el método que tenga configurado).
3. Definir una nueva contraseña.

**Si no funciona** (el empleado no tiene MFA configurado, o el portal dice que la cuenta está bloqueada/deshabilitada): esto ya no es self-service — decirle que contacte a José Manuel para que lo revise directamente en Entra ID.

## No puedo entrar a Teams / Teams no carga
1. Cerrar sesión completamente y volver a entrar (a veces el token de sesión expira sin avisar).
2. Si es la app de escritorio, revisar que esté actualizada — Teams a veces deja de funcionar en versiones viejas.
3. Probar la versión web (teams.microsoft.com) para descartar si es un problema del cliente instalado o de la cuenta.
4. Si nada de esto funciona y el problema persiste, es un caso para José Manuel.

## Configurar el correo en un celular o dispositivo nuevo
1. Descargar la app de Outlook (recomendado sobre el cliente de correo nativo del teléfono, da mejor soporte a las políticas de seguridad de la empresa).
2. Agregar la cuenta con el correo corporativo (@talentmovers.com) y la contraseña.
3. Completar el MFA si lo pide.
4. Si el dispositivo requiere inscribirse en algún sistema de gestión de dispositivos de la empresa, eso también lo maneja José Manuel — si el empleado ve una pantalla pidiendo "inscribir dispositivo" y no sabe qué hacer, dirígelo a él.

## VPN
Talent Movers todavía no tiene documentado aquí qué cliente VPN usa ni sus pasos de conexión — si un empleado pregunta por VPN, dile que confirme con José Manuel cuál es el procedimiento actual, y de ser posible pide que se actualice este archivo con esa información.

## Cuenta bloqueada / no me deja entrar y no hay opción de recuperar contraseña
No es self-service — dirige directamente a José Manuel con el mensaje de error exacto que ve el empleado (ayuda mucho a diagnosticar más rápido).

---
**Nota para quien mantiene este archivo:** faltan detalles reales de Talent Movers en VPN y en cualquier política de dispositivos — completar cuando se tenga esa información. El resto de este archivo es orientación general de Microsoft 365 aplicable a la mayoría de configuraciones estándar.
