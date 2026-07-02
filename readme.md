# Descripción del proyecto

Este proyecto implementa un framework de automatización de pruebas utilizando Python. Incluye pruebas de interfaz web (UI) con Selenium WebDriver, pruebas de API con Requests, generación de reportes HTML mediante Pytest y organización del código siguiendo el patrón Page Object Model (POM).

El objetivo es disponer de una estructura escalable y mantenible que permita incorporar nuevos casos de prueba de manera sencilla.


# Tecnologías utilizadas

* Python 3.11+
* Pytest
* Selenium WebDriver
* Behave (BDD)
* Requests
* Pytest-HTML
* WebDriver Manager
* Git
* GitHub


# Estructura del proyecto

```bash
proyecto_final/
│
├── pages/
│   ├── login_page.py
│   ├── inventory_page.py
│   └── cart_page.py
│
├── tests/
│   ├── ui/
│   │   ├── test_login.py
│   │   ├── test_inventory.py
│   │   ├── test_cart.py
│   │   ├── test_checkout.py
│   │   
│   │
│   └── api/
│       ├── test_get_users.py
│       ├── test_create_user.py
│       └── test_delete_user.py
│
├── features/
│   ├── login.feature
│   ├── environment.py
│   └── steps/
│       └── login_steps.py
│
├── utils/
│   ├── driver_factory.py
│   ├── logger.py
│   ├── datos.py
│   └── helpers.py
│
├── data/
│   ├── login.csv
│   └── usuarios.json
│
├── reports/
│   ├── reporte.html
│   
│
├── requirements.txt
├── pytest.ini
├── conftest.py
└── README.md
```

# Funcionalidades implementadas

## Pruebas UI

Se automatizaron los siguientes escenarios utilizando Selenium WebDriver:

* Login exitoso.
* Login con credenciales inválidas.
* Navegación por el inventario.
* Agregar productos al carrito.
* Proceso de Checkout.

Las pruebas implementan el patrón **Page Object Model (POM)** para separar la lógica de interacción con la interfaz de la lógica de las pruebas.


## Pruebas de API

Se realizaron pruebas utilizando la biblioteca Requests sobre una API pública.

Casos implementados:

* GET
* POST
* DELETE

En cada prueba se validan:

* Código HTTP.
* Contenido JSON.
* Estructura de la respuesta.
* Escenarios de éxito y error.


## Parametrización de datos

Los datos de prueba son leídos desde archivos externos (CSV/JSON), permitiendo ejecutar un mismo caso de prueba con diferentes conjuntos de datos.


## Capturas de pantalla

Cuando una prueba de interfaz falla, el framework captura automáticamente una imagen de la pantalla.

Las capturas se almacenan en:


Cada archivo incluye:

* Nombre del test.
* Fecha.
* Hora.


## Reportes HTML

El proyecto genera reportes HTML utilizando **pytest-html**.

Los reportes incluyen:

* Estado de cada prueba.
* Tiempo de ejecución.
* Errores.
* Capturas de pantalla de las pruebas fallidas.


## Logging

Se implementó un sistema de logging para registrar los pasos importantes durante la ejecución de las pruebas.

Los archivos de log se almacenan en:


# Dependencias principales

pytest
selenium
requests
behave
webdriver-manager
pytest-html

# Control de versiones

El proyecto utiliza Git para el control de versiones.

El desarrollo se realizó mediante ramas independientes y posteriormente se integró a la rama.

# Autor

**Lilia Mosquera Villanueva**

Proyecto desarrollado como trabajo final de Automatización de Pruebas utilizando Python, Selenium, Pytest y Requests.


