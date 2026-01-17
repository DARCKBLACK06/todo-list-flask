# 📝 Todo List CRUD con Flask

Proyecto sencillo de tipo **CRUD** desarrollado con **Flask** y **SQLAlchemy**, desplegado en **PythonAnywhere** utilizando **WSGI** y **virtualenv**. Pensado con estructura clásica, clara y funcional.

> Tradicional, directo y sin magia negra: Flask como debe usarse.

---

## 🚀 Tecnologías utilizadas

* Python 3.10
* Flask 3.x
* Flask-SQLAlchemy
* SQLite
* HTML (Jinja2)
* Git & GitHub
* PythonAnywhere (hosting gratuito)

---

## 📂 Estructura del proyecto

```
todo-list-flask/
├── run.py
├── requirements.txt
├── todor/
│   ├── __init__.py
│   ├── auth.py
│   ├── todo.py
│   ├── models.py
│   └── templates/
│       ├── auth/
│       ├── todo/
│       └── index.html
└── .gitignore
```

---

## ⚙️ Instalación local

### 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/DARCKBLACK06/todo-list.git
cd todo-list
```

---

### 2️⃣ Crear y activar entorno virtual

```bash
python -m venv venv

# En Linux / macOS
source venv/bin/activate

# En Windows
venv\\Scripts\\activate
```

---

### 3️⃣ Instalar dependencias

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Ejecutar la aplicación

```bash
python run.py
```

Luego abre el navegador en:

```
http://127.0.0.1:5000
```

---

## 🗄️ Base de datos

* Se utiliza **SQLite**.
* La base de datos se crea automáticamente al iniciar la aplicación:

```python
sqlite:///todolist.db
```

No requiere configuración adicional.

---

## 🌐 Despliegue en PythonAnywhere

### 1️⃣ Clonar el repositorio en PythonAnywhere

```bash
cd ~
git clone https://github.com/DARCKBLACK06/todo-list-flask.git
cd todo-list
```

---

### 2️⃣ Crear virtualenv en PythonAnywhere

```bash
python3.10 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

### 3️⃣ Configurar Web App

* Web → Add new web app
* Manual configuration
* Python 3.10
* Framework: Flask (manual)

---

### 4️⃣ Configurar archivo WSGI

Contenido del archivo WSGI:

```python
import sys

path = "/home/JavierE06/todo-list-flask"
if path not in sys.path:
    sys.path.append(path)

from run import app as application
```

---

### 5️⃣ Configurar Virtualenv

En la sección **Virtualenv**:

```
/home/JavierE06/todo-list-flask/venv/
```

---

### 6️⃣ Recargar aplicación

Presiona **Reload** y accede a:

```
https://JavierE06.pythonanywhere.com
```

---

## 🧠 Notas importantes

* El entorno virtual **NO** se sube al repositorio.
* El archivo `.gitignore` evita subir dependencias innecesarias.
* El proyecto usa el patrón **Factory** (`create_app`).
* La aplicación está pensada para fines académicos.

---

## 🎓 Autor

**Javier E06**
Estudiante de IRIC – Ingeniería en Redes Inteligentes y Ciberseguridad

---

> Código sencillo, estructura clara y despliegue real. Lo demás es ruido.
