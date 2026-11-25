# 🚀 API REST - CRUD de Usuarios

API backend desarrollada con **Python**, **FastAPI** y **PostgreSQL** para la gestión completa de usuarios (Crear, Leer, Actualizar y Eliminar), con validación de datos, encriptación de contraseñas y despliegue en la nube.

---

## 🛠️ Tecnologías utilizadas

* **Lenguaje:** Python 3.11+
* **Framework Web:** FastAPI + Uvicorn
* **ORM:** SQLAlchemy
* **Validación de datos:** Pydantic
* **Seguridad:** Passlib (hashing de contraseñas con `bcrypt`)
* **Base de datos:** PostgreSQL (alojada en **Neon**)
* **Despliegue:** **Render**

---

## 📁 Estructura del proyecto

```text
CRUD_usuarios/
├── database.py       # Configuración de conexión y sesión con PostgreSQL
├── models.py         # Modelos de tablas de la base de datos (SQLAlchemy)
├── schemas.py        # Esquemas de validación de entrada y salida (Pydantic)
├── main.py           # Inicialización de FastAPI y definición de endpoints
├── requirements.txt  # Dependencias del proyecto
└── .gitignore        # Archivos excluidos del control de versiones
```

---

## 📌 Endpoints disponibles

| Método | Ruta | Descripción | Código de éxito |
| :--- | :--- | :--- | :--- |
| `POST` | `/users/` | Registrar un nuevo usuario (valida correo único y encripta contraseña) | `201 Created` |
| `GET` | `/users/` | Obtener la lista de todos los usuarios (soporta paginación `skip` y `limit`) | `200 OK` |
| `GET` | `/users/{user_id}` | Consultar un usuario específico por su ID | `200 OK` |
| `PATCH` | `/users/{user_id}` | Actualizar parcialmente los datos de un usuario | `200 OK` |
| `DELETE` | `/users/{user_id}` | Eliminar un usuario de la base de datos | `204 No Content` |

---

## ⚙️ Instalación y ejecución local

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com
   cd API_usuarios
   ```

2. **Crear y activar el entorno virtual:**
   ```bash
   # En Windows:
   python -m venv venv
   venv\Scripts\activate

   # En Linux / Mac:
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configurar variables de entorno:**
   Crea un archivo `.env` en la raíz del proyecto y agrega tu cadena de conexión de PostgreSQL:
   ```env
   DATABASE_URL=postgresql+psycopg://usuario:contraseña@host/nombre_bd?sslmode=require
   ```

5. **Iniciar el servidor de desarrollo:**
   ```bash
   uvicorn main:app --reload
   ```

6. **Probar la API:**
   Abre tu navegador en **`http://127.0.0`** para interactuar con la documentación automática de Swagger UI.

---

## 🌐 Demo en producción

* **Documentación interactiva (Swagger):** `https://onrender.com` *(Reemplaza con tu URL real de Render)*

---

## 👤 Autor

* **Kevin / Frank Smith Hurtado** - [GitHub](https://github.com)
