# CodeForge AI V7

Esta versión cambia el proceso: el usuario final no ejecuta PowerShell, BAT, Python ni PyInstaller.

GitHub Actions construye automáticamente `CodeForgeAI_Setup.exe`.

Proceso:
1. Subir esta carpeta a un repositorio GitHub.
2. Ejecutar el workflow `Build CodeForge AI Windows Installer` desde Actions, o crear un tag `v7.0.0`.
3. Descargar el artifact `CodeForgeAI-Windows-Installer`.
4. Dentro está `CodeForgeAI_Setup.exe`.
5. El usuario final solo ejecuta ese instalador.

El instalador incluye la aplicación empaquetada y no requiere Python en el PC del usuario.

Nota de seguridad: una compilación nueva puede seguir mostrando Smart App Control como editor no reconocido si no está firmada con un certificado de confianza. Esta versión no desactiva ni salta las protecciones de Windows. Para distribución pública se debe firmar el instalador.
