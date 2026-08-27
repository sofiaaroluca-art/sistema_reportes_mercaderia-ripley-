# 🚛 Sistema de Reportes de Garita + Módulo Inteligente ML

Sistema web desarrollado para la **gestión del flujo de mercadería y generación de reportes operativos**, incorporando un módulo de **Machine Learning 🤖** para identificar posibles situaciones de riesgo operativo.

## ✨ Características principales

* 🔐 **Autenticación de usuarios**
* 📊 **Dashboard** para consulta y gestión de reportes
* 📝 **Registro y validación** de nuevos reportes
* 👁️ **Visualización de reportes** en modo solo lectura
* 🚚 Gestión de **camiones y categorías**
* 👥 Gestión de **usuarios**
* 🗃️ Registro de **reportes y detalles de reporte**
* 💾 Base de datos con **SQLite** y soporte opcional para **MySQL**
* 🤖 Módulo de **Machine Learning**
* 🌳 Modelo basado en **Árbol de Decisión**
* ⚠️ Clasificación de mercadería en:

  * 🟢 **Normal**
  * 🔴 **Riesgo Operativo**
* 📈 **Análisis Exploratorio de Datos (EDA)**
* 📊 Métricas de evaluación y **matriz de confusión**
* 🔎 Análisis de **importancia de variables**

## 🛠️ Tecnologías utilizadas

| Tecnología                       | Uso                               |
| -------------------------------- | --------------------------------- |
| 🐍 **Python**                    | Lenguaje principal                |
| 🌐 **Flask**                     | Framework backend                 |
| 🤖 **Scikit-learn**              | Machine Learning                  |
| 🐼 **Pandas**                    | Procesamiento y análisis de datos |
| 🎨 **HTML5 / CSS3 / JavaScript** | Interfaz web                      |
| 🗄️ **SQLite / MySQL**           | Base de datos                     |
| 📦 **Bootstrap**                 | Diseño de interfaz                |

## 🤖 Módulo de Machine Learning

El sistema incorpora un modelo de **Árbol de Decisión** orientado a la identificación de riesgo operativo en la gestión de mercadería.

### 📌 Variables utilizadas

* 🏷️ Categoría
* 🚚 Camión
* 📦 Cantidad total
* 🧾 Número de productos
* 📊 Stock estimado
* ⚠️ Stock mínimo
* 📈 Demanda semanal
* 🚛 Unidades en tránsito
* ⏱️ Tiempo de reposición
* 📅 Días sin reposición
* 🚨 Incidencias
* 🔄 Rotación del producto

### 📊 Análisis del modelo

El módulo permite visualizar:

* 📈 Métricas de rendimiento
* 🎯 Resultados de clasificación
* 🔲 Matriz de confusión
* 🔎 Importancia de variables
* 📊 Gráficos del análisis exploratorio de datos (EDA)

## 🚀 Instalación y ejecución

### 1️⃣ Crear entorno virtual

```bash
python -m venv venv
```

### 2️⃣ Activar el entorno

```powershell
.\venv\Scripts\Activate.ps1
```

Si PowerShell bloquea la ejecución:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\venv\Scripts\Activate.ps1
```

### 3️⃣ Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4️⃣ Ejecutar el sistema

```bash
python run.py
```

🌐 **Acceso local:**

```text
http://127.0.0.1:5000
```

## 🗄️ Base de datos

El proyecto utiliza **SQLite** por defecto, permitiendo ejecutar el sistema sin necesidad de instalar un servidor de base de datos adicional.

📁 Ubicación:

```text
instance/sistema_reportes.db
```

También se incluye un script para **MySQL**:

```text
database/schema_mysql.sql
```

## 📂 Estructura del proyecto

```text
sistema_reportes_ripley/
│
├── 🚀 run.py
├── ⚙️ config.py
├── 📦 requirements.txt
├── 📖 README.md
├── 🔧 .env.example
│
├── 🗄️ database/
│   └── schema_mysql.sql
│
├── 💻 app/
│   ├── models/
│   │   ├── usuario.py
│   │   ├── camion.py
│   │   ├── categoria.py
│   │   └── reporte.py
│   │
│   ├── controllers/
│   │   ├── auth.py
│   │   ├── reportes.py
│   │   └── ml.py
│   │
│   ├── services/
│   │   └── ml_service.py
│   │
│   ├── templates/
│   │   ├── base.html
│   │   ├── login.html
│   │   ├── dashboard.html
│   │   ├── nuevo_reporte.html
│   │   ├── ver_reporte.html
│   │   └── ml_dashboard.html
│   │
│   └── static/
│       ├── css/
│       ├── js/
│       └── img/
│
└── 📚 docs/
    └── rubrica_avance_3.md
```

## 🎯 Objetivo del proyecto

Desarrollar una solución web que permita **centralizar la gestión de reportes de garita y el flujo de mercadería**, complementándola con técnicas de **Machine Learning** para apoyar la identificación temprana de posibles riesgos operativos.

---

### 🎓 Proyecto académico

Desarrollado como propuesta tecnológica para la **gestión logística y análisis inteligente de mercadería**.

⭐ Si este proyecto te resulta interesante, ¡no dudes en explorar el código!


- Login visual.

<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/74cb84e0-21f2-4dc6-bd8a-22615ef757f6" />

- Dashboard de reportes.
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/86ec3f75-6c64-42f3-b862-9287158acdb6" />
- Registro de nuevo reporte.
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/a076dc99-aa52-4c61-a13e-af9ed1e06fe9" />
- Módulo inteligente de riesgo operativo
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/caec4a54-fbcf-4646-8d73-72965249cd85" />
- Módulo de Machine Learning para predecir riesgo operativo.
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/ffd6d356-ae1b-4417-9d3b-b46b4f5cd044" />
- EDA, gráficos, métricas, matriz de confusión e importancia de variables.
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/230ff6a7-fb6b-4b76-83f5-284c16be39da" />
- Algoritmos No Supervisados
<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/23a8366d-e5f2-4e72-8c36-efbcced744ea" />

