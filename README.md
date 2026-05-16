# Test List Django Project

Aplicación Django simple para gestionar tareas.

## Descripción

Este proyecto es una aplicación de tareas basada en Django 6.0.5 con un modelo `Task` que almacena título, descripción, estado de completado y fechas de creación/actualización.

## Características

- Lista de tareas disponibles en la página principal `/`
- Detalle de cada tarea en `/tareas/<id>/`
- Modelo `Task` con campos `title`, `description`, `completed`, `created_at` y `updated_at`
- Usa SQLite como base de datos por defecto
- Plantillas HTML en `templates/`

## Requisitos

- Python 3.11 (recomendado)
- Django 6.0.5
- tzdata
- sqlite3 (integrado con Python)

## Instalación

1. Crear y activar un entorno virtual:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Instalar dependencias:

```powershell
pip install -r requirements.txt
```

3. Aplicar migraciones:

```powershell
python manage.py migrate
```

4. (Opcional) Crear un superusuario para acceder a `/admin/`:

```powershell
python manage.py createsuperuser
```

## Ejecución

Iniciar el servidor de desarrollo:

```powershell
python manage.py runserver
```

Luego abrir en el navegador:

- `http://127.0.0.1:8000/` para ver la lista de tareas
- `http://127.0.0.1:8000/tareas/<id>/` para ver el detalle de una tarea
- `http://127.0.0.1:8000/admin/` para administrar el modelo desde el panel de Django

## Estructura de carpetas

- `manage.py` - comando principal de Django
- `base_project/` - configuración del proyecto Django
- `tasks/` - aplicación de tareas
- `templates/` - plantillas HTML
- `static/` - archivos estáticos
- `db.sqlite3` - base de datos SQLite
- `requirements.txt` - dependencias del proyecto

## Notas

- El proyecto está configurado para desarrollo (`DEBUG = True`). No se recomienda usar esta configuración en producción.
- La base de datos por defecto es `db.sqlite3` y se crea al ejecutar las migraciones.
