# Dashboard Monitor (Python + Selenium + Flask)

Sistema de monitoreo automatizado para un dashboard operativo. Detecta códigos de error, registra eventos y permite ejecutar verificaciones manuales desde una interfaz web.

## ¿Qué resuelve?
- Monitorea un dashboard y detecta **códigos de error** de forma automática.
- Permite ver el **último estado** y ejecutar un **check manual** desde una app Flask.
- Asigna el responsable según **turnos definidos en JSON**.
- Estructura lista para integrarse con notificaciones (SMS/WhatsApp) y escalamiento.

## Componentes del proyecto
- **`dashboard_monitor.py`**: chequeo del dashboard (Selenium) y detección de errores.
- **`vpn_connect.py`**: módulo de conexión a VPN (pensado para ejecución en entornos restringidos).
- **`notifier.py`**: capa de notificaciones (estructura preparada para Twilio / canales similares).
- **`app.py`**: interfaz web (Flask) para visualizar estado y ejecutar chequeos manuales.
- **`turnos.json`**: configuración de turnos/responsables por fecha.
- **`main.py`**: punto de entrada para ejecución del monitoreo.
- **`requirements.txt`**: dependencias.

## Stack
- Python
- Selenium (modo headless)
- Flask
- python-dotenv (opcional para variables de entorno)

## Ejecución
### 1) Instalar dependencias
```bash
pip install -r requirements.txt
