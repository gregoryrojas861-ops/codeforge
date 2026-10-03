# CodeForge AI V3

IDE de escritorio inspirado en VS Code para trabajar con múltiples lenguajes y un agente autónomo local.

## Características
- Editor con pestañas, explorador de archivos y búsqueda global.
- Terminal PowerShell integrada.
- IA local con Ollama, sin créditos por petición del proveedor.
- Agente autónomo: inspecciona → planifica → edita → ejecuta → detecta errores → corrige → prueba → verifica.
- Vista de cambios antes de aplicar modificaciones.
- Snapshots y restauración.
- Aprobación obligatoria para comandos peligrosos.
- Tests automáticos y análisis básico de seguridad.
- Diagnóstico Python.
- Detección de herramientas y servidores LSP instalados.
- Git.
- Modo Profesor.
- Panel de tareas y registro del agente.
- Preparado para empaquetar con PyInstaller.

## Requisitos
Windows 10/11, Python 3.11+ y opcionalmente Ollama.

## Instalación
1. Ejecuta `install_windows.bat`.
2. Ejecuta `run_windows.bat`.
3. Para IA local instala Ollama y descarga un modelo de código, por ejemplo `qwen2.5-coder:7b`.

La IA local evita créditos por API, pero depende del hardware y del modelo instalado.

## Seguridad
CodeForge no ejecuta comandos peligrosos automáticamente. El agente debe solicitar aprobación explícita antes de ejecutarlos.
