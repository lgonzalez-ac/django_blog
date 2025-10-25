# Django Blog — App de Blog Post

Esta es una aplicación de ejemplo para gestionar entradas de blog (Blog Post) construida con Django.

## Resumen

`django_blog` es una pequeña aplicación Django que provee funcionalidad para crear, editar y listar entradas de blog. Está pensada para servir como punto de partida educativo o base para una aplicación más completa.

## Estructura principal

- `manage.py` — comando de gestión de Django.
- `requirements.txt` — dependencias del proyecto.
- `db.sqlite3` — base de datos por defecto (SQLite) para desarrollo.
- `blogs/` — aplicación principal con modelos, vistas y tests.
- `django_project/` — configuración del proyecto (`settings.py`, `urls.py`, etc.).

## Requisitos

- Python 3.8+ (ajusta según tu entorno).
- pip
- (opcional) virtualenv o venv para entornos virtuales.

## Instalación rápida (Windows / PowerShell)

1. Crear y activar un entorno virtual:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Instalar dependencias:

```powershell
pip install -r requirements.txt
```

3. Aplicar migraciones y crear superusuario:

```powershell
python manage.py migrate
python manage.py createsuperuser
```

4. Ejecutar servidor de desarrollo:

```powershell
python manage.py runserver
```

Abre `http://127.0.0.1:8000/` en tu navegador. El panel de administración estará en `http://127.0.0.1:8000/admin/`.

## Características

- CRUD básico para entradas de blog (crear, leer, actualizar, borrar).
- Panel de administración para gestionar posts y usuarios.
- Estructura lista para extender (API, autenticación, paginación, búsqueda).

## Modelos y puntos de entrada importantes

- Los modelos principales están en `blogs/models.py`.
  - Normalmente hay un modelo `Post` que contiene campos como: `title`, `slug`, `content`, `author`, `created_at`, `updated_at`, `status`.
- Las vistas y la lógica están en `blogs/views.py`.
- Las rutas están configuradas en `django_project/urls.py` y, posiblemente, en `blogs/urls.py` si existen rutas específicas de la app.

Nota: Para ver exactamente los campos y las URLs, revisa `blogs/models.py` y `blogs/views.py`.

## Pruebas

Ejecuta las pruebas de la app con:

```powershell
python manage.py test
# o para la app específica
python manage.py test blogs
```

## Despliegue (sugerencias)

- Para producción, usa una base de datos como PostgreSQL.
- Configura variables de entorno para `SECRET_KEY`, `DEBUG=False`, y la configuración de base de datos.
- Sirve archivos estáticos con `collectstatic` y un servidor como Gunicorn + Nginx.

## Contribuir

1. Haz fork del repositorio.
2. Crea una rama con tu feature o fix: `git checkout -b feature/mi-cambio`.
3. Envía un pull request describiendo tu cambio.

## Licencia y contacto

Añade la licencia del proyecto aquí si corresponde. Para preguntas o soporte, contacta al mantenedor del repositorio.

---

README creado para la app "Blog Post" — ajusta detalles específicos (campos del modelo, rutas, dependencias) si tu proyecto difiere de las convenciones comunes.