<h1 align="center">REST API FLASK</h1>

<p align="center">
    <a href="https://www.python.org/downloads/release/python-31012/" align="center">
        <img alt="Python" src="https://img.shields.io/badge/Python%20Download-3.10.12-blue">
    </a>
    <a href="https://flask.palletsprojects.com/en/3.0.x/" align="center">
        <img alt="PEP8" src="https://img.shields.io/badge/Flask%20Docs-Python-blue">
    </a>
</p>

<p align="center">Este proyecto es una API desarrollada en Flask para un sistema de facturación, que permite la autenticación de usuarios, devuelve un token único temporal y envía una petición para obtener datos de una base 'MariaDB' y retorna información sobre facturas por día de un endpoint en formato json. Este proyecto fue creado por Yulian Planas bajo la necesidad de una aplicación para integraciones de tercero destinadas a las necesidades de una PYME para el manejo de stock y facturación.</p>

---
## Instalación
Requiere Python 3.10 o superior. Si quieres usar Python 3.11 (las versiones más recientes), puedes descargar en: [Python Official Downloads](https://www.python.org/downloads/ "Python Downloads").

1. Crea un entorno virtual ***(Recomendado)***

    ```
    python.exe -m venv .env
    ```

2. Instala las dependencias necesarias.

    ```
    pip install -U -r requirements.txt
    ```

3.  Ejecuta el archivo desde la consola.

    ```
    python.exe index.py
    ```

## Dependencias Principales

1. **Flask**
2. **Flask-JWT-Extended**
3. **Flask-SQLAlchemy**

## Funcionalidades Principales

1. **Autenticación**: La aplicación utiliza JWT para gestionar la autenticación de usuarios.
2. **Conexión a Bases de Datos**: Configuración de múltiples bases de datos según sucursales.
3. **Obtención de Facturas**: Endpoint para obtener facturas según una fecha dada.

## Verificaciones de Seguridad Implementadas

1. **Validación de Credenciales**: Verifica que las credenciales proporcionadas en el inicio de sesión sean correctas.
2. **Token JWT Expirado**: Controla la expiración del token JWT para mantener la seguridad de la sesión.
3. **Control de Acceso a Sucursales**: Asegura que los usuarios solo puedan acceder a las sucursales autorizadas.

## Registro de Conexiones
 
- Se implementó un registro de conexiones en el endpoint `/login`, almacenando intentos de inicio de sesión en el archivo `log.txt` con información de hora y dirección IP.

## Recomendaciones

- Esta aplicación funciona localmente para el desarrollo de pruebas y estudio. Para usar en producción, se recomienda utilizar `gunicorn`, `nginx` y `docker`.

---

## License
By downloading this, you agree to the Commons Clause license and that you're not allowed to sell this repository or any code from this repository. For more info see https://commonsclause.com/.
