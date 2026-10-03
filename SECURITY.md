# Seguridad y confianza de CodeForge AI V5

## Qué significa "segura"

CodeForge AI puede estar técnicamente libre de malware y aun así Windows puede mostrar "editor desconocido" o advertencias de reputación. Son problemas diferentes:

1. **Seguridad del software:** revisar el código, dependencias, permisos y comportamiento.
2. **Confianza del editor:** Windows necesita una firma digital válida de un certificado que el equipo considere confiable.
3. **Reputación/distribución:** algunos mecanismos de Windows pueden mostrar advertencias a aplicaciones nuevas aunque estén firmadas.

## Lo que esta V5 hace

- No incluye un instalador que desactive Defender o Smart App Control.
- No incluye técnicas para saltarse advertencias de seguridad.
- El usuario puede compilar el EXE localmente.
- Incluye preparación para firma Authenticode.
- Incluye instalador Inno Setup.
- Incluye archivos de empaquetado MSIX.
- El agente mantiene aprobación previa para acciones clasificadas como peligrosas.

## Firma de producción

Para distribución pública, utiliza un certificado de firma de código emitido por una autoridad de certificación reconocida o una vía oficial de distribución que proporcione confianza.

Un certificado autofirmado sirve para pruebas internas cuando se instala explícitamente como certificado de confianza, pero **no convierte la aplicación en un editor públicamente reconocido**.

## Dependencias

El proyecto utiliza Python/PySide6 y dependencias declaradas en `requirements.txt`. Antes de distribuir una versión empresarial, fija versiones y genera un inventario de dependencias.

## Recomendación

Compila en una máquina Windows limpia, revisa `dist\CodeForgeAI`, prueba el EXE, genera el instalador, firma ambos artefactos y conserva el certificado privado fuera del repositorio.
