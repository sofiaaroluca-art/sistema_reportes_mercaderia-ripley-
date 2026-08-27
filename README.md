# Sistema de Reportes de Garita + Módulo Inteligente ML

Proyecto académico basado en los mockups de UX para un sistema de gestión de flujo de mercadería y reportes. Incluye:

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

## 1. Requisitos

Tener instalado Python 3.10 o superior.

## 2. Crear entorno virtual

En Visual Studio Code, abrir la carpeta del proyecto y ejecutar:

```bash
python -m venv venv
```

Activar entorno virtual en Windows PowerShell:

```bash
.\venv\Scripts\Activate.ps1
```

Si PowerShell bloquea la activación, ejecutar:

```bash
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\venv\Scripts\Activate.ps1
```

## 3. Instalar librerías

```bash
pip install -r requirements.txt
```

## 4. Ejecutar proyecto

```bash
python run.py
```

Abrir en el navegador:

```text
http://127.0.0.1:5000
```

## 5. Credenciales de prueba

```text
Usuario: jose.alguay@ripley.pe
Contraseña: 123456
```

También puedes usar:

```text
Usuario: admin
Contraseña: admin123
```

## 6. Base de datos

Por defecto el sistema usa SQLite para que corra rápido sin instalar MySQL. El archivo se crea automáticamente en:

```text
instance/sistema_reportes.db
```

El script MySQL solicitado está en:

```text
database/schema_mysql.sql
```

Para usar MySQL:

1. Crear la base ejecutando `database/schema_mysql.sql` en MySQL.
2. Copiar `.env.example` como `.env`.
3. Cambiar `DB_ENGINE=mysql` y completar usuario, clave, host y base de datos.
4. Ejecutar nuevamente `python run.py`.

## 7. Módulo Machine Learning

Ruta dentro del sistema:

```text
/ml/dashboard
```

El módulo entrena un Árbol de Decisión para clasificar mercadería en:

- Normal
- Riesgo operativo

Variables usadas:

- Categoría
- Camión
- Cantidad total
- Número de productos
- Stock estimado
- Stock mínimo
- Demanda semanal
- Unidades en tránsito
- Tiempo de reposición
- Días sin reposición
- Incidencias
- Rotación del producto

## 8. Estructura del proyecto

```text
sistema_reportes_ripley/
├── run.py
├── config.py
├── requirements.txt
├── README.md
├── .env.example
├── database/
│   └── schema_mysql.sql
├── app/
│   ├── __init__.py
│   ├── models/
│   │   ├── usuario.py
│   │   ├── camion.py
│   │   ├── categoria.py
│   │   └── reporte.py
│   ├── controllers/
│   │   ├── auth.py
│   │   ├── reportes.py
│   │   └── ml.py
│   ├── services/
│   │   └── ml_service.py
│   ├── templates/
│   │   ├── base.html
│   │   ├── login.html
│   │   ├── dashboard.html
│   │   ├── nuevo_reporte.html
│   │   ├── ver_reporte.html
│   │   └── ml_dashboard.html
│   └── static/
│       ├── css/style.css
│       ├── js/main.js
│       └── img/
└── docs/
    └── rubrica_avance_3.md
```
