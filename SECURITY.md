# Seguridad

Para comunicar una vulnerabilidad, escribe a **contacto@interdato.com** con el repositorio, la versión o commit afectado, el impacto y pasos mínimos para reproducirla. No publiques credenciales, datos personales ni pruebas con información sensible en issues o pull requests públicos.

## Controles de este repositorio

- El workflow **Security** busca secretos en el historial git disponible en cada push y pull request; también puede ejecutarse manualmente y semanalmente.
- El escáner se descarga en una versión fija y se comprueba su SHA-256 antes de ejecutarlo. Sus resultados ocultan los valores detectados.
- Los nuevos controles de CI usan permisos de lectura y no reciben claves de servicios externos.
- Dependabot propone actualizaciones semanales de las acciones de GitHub. Las propuestas requieren revisión; no se fusionan automáticamente.

Estos controles detectan clases concretas de problemas y no sustituyen una revisión del cambio, los permisos de la cuenta o la configuración del hosting. El estado verde de CI no es una certificación de seguridad.

## Alcance

El agente y las skills son instrucciones para Claude Code. Revisa las propuestas antes de aplicarlas o desplegarlas y evita incluir secretos o datos de clientes en prompts o ejemplos públicos.

La automatización heredada `efficiency-improver` es independiente de la instalación de las skills. Conserva sus propias condiciones, permisos y referencias a secrets de GitHub; esas referencias no son claves publicadas. Su ejecución requiere la configuración del proveedor y puede consumir cuota. Los nuevos controles Security no necesitan esa configuración ni activan esa automatización.
