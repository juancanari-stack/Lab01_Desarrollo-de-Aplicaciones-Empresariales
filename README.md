# mydjango

Proyecto Django de práctica que implementa un modelo `Item` con panel de administración y una vista pública que lista los ítems registrados.

## Estructura del proyecto

```
src/
├── config/          # Configuración del proyecto (settings, urls, wsgi, asgi)
├── core/            # App principal
│   ├── models.py    # Modelo Item
│   ├── admin.py     # Registro de Item en el panel de administración
│   ├── views.py     # Vista para listar los ítems
│   ├── urls.py      # Rutas de la app
│   └── templates/core/
│       ├── base.html
│       └── item_list.html
├── manage.py
├── requirements.txt
└── db.sqlite3
```

## Requisitos previos

- Python 3.10 o superior
- pip

## Instalación y ejecución

1. Clonar el repositorio:
   ```bash
   git clone <URL-del-repositorio>
   cd mydjango/src
   ```

2. Crear y activar un entorno virtual:
   ```bash
   python -m venv .venv
   .venv\Scripts\Activate.ps1   # Windows PowerShell
   ```

3. Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

4. Aplicar las migraciones:
   ```bash
   python manage.py migrate
   ```

5. Crear un superusuario:
   ```bash
   python manage.py createsuperuser
   ```

6. Levantar el servidor de desarrollo:
   ```bash
   python manage.py runserver
   ```

## Uso

- **Página principal:** [http://127.0.0.1:8000/](http://127.0.0.1:8000/) — muestra el listado de ítems registrados.
- **Panel de administración:** [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/) — permite agregar, editar y eliminar ítems (requiere iniciar sesión con el superusuario).
