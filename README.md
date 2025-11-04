# 🧾 TAREA-SIS-2420: Gestión de Inventario

## 📖 Descripción General
Este proyecto es una aplicación desarrollada en **Python** para la **gestión de inventario, ventas y control de stock**, creada como parte de la materia **SIS-2420**.  
El sistema permite **registrar, editar, actualizar y eliminar productos**, así como **gestionar ventas, generar facturas en formato PDF** y mantener un registro en una **base de datos SQLite**.

El objetivo del proyecto es aplicar los conocimientos de programación estructurada y manejo de bases de datos en un entorno práctico, utilizando librerías de interfaz gráfica y empaquetado de aplicaciones.

---

## 🧩 Contenido del Repositorio

| Archivo / Carpeta | Descripción |
|--------------------|-------------|
| `index.py` | Punto de entrada principal del sistema. Ejecuta la interfaz gráfica y enlaza los módulos. |
| `manager.py` | Controlador principal del flujo del programa. Coordina las funciones entre los distintos módulos. |
| `inventario.py` | Módulo encargado del **CRUD (crear, leer, actualizar, eliminar)** de productos: nombre, precio, cantidad, proveedor, etc. |
| `ventas.py` | Módulo de **gestión de ventas y generación de facturas PDF**. Permite seleccionar productos, procesar pagos y registrar facturas. |
| `container.py` | Contiene **funciones auxiliares** y complementarias utilizadas en todo el programa. |
| `database.db` | Base de datos **SQLite** utilizada para almacenar productos, ventas y registros. Creada y gestionada mediante **DB Browser for SQLite**. |
| `facturas/` | Carpeta donde se almacenan automáticamente las facturas generadas en formato PDF. |
| `imagenes/` y `icono/` | Contienen **recursos gráficos e íconos** usados en la interfaz (descargados desde Google). |
| `GestionDelInventario.spec` | Archivo de configuración generado por **PyInstaller** para convertir el proyecto en un ejecutable `.exe`. |

---

## ⚙️ Requisitos

- **Python 3.8 o superior**
- **Visual Studio Code** (recomendado para la ejecución)
- **Librerías externas:**
  - `tkinter` → para la interfaz gráfica  
  - `Pillow` → para manejo de imágenes e íconos  
  - `sqlite3` → conexión a la base de datos  
  - `reportlab` o similar → para generar facturas en PDF  
  - (Cualquier otra dependencia incluida en `requirements.txt`)

---

## 🚀 Instalación y Ejecución

### 🔹 Opción 1: Ejecutar directamente desde Visual Studio Code
1. Clonar o descargar el repositorio:
   ```bash
   git clone https://github.com/Marcos-JM777/TAREA-SIS-2420
   1. Abrir la carpeta del proyecto en Visual Studio Code.
2. Asegurarse de tener instaladas las dependencias necesarias.
3. Ejecutar el archivo principal:
   ```bash
   python index.py
   ```
   o directamente presionando Run ▶️ dentro de VS Code.

🔹 Opción 2: Crear un ejecutable (.exe)

El proyecto puede convertirse en un archivo ejecutable de Windows utilizando PyInstaller:

```bash
pyinstaller --onefile --windowed index.py
```

El archivo .exe resultante se generará dentro de la carpeta dist y podrá ejecutarse sin necesidad de abrir Visual Studio Code.

🧠 Funcionalidades Principales

🗃️ Módulo de Inventario

· Registro de productos con nombre, precio, cantidad, proveedor y stock disponible.
· Edición y actualización de datos en tiempo real.
· Eliminación segura de productos obsoletos.
· Visualización detallada de los productos registrados.

💵 Módulo de Ventas

· Selección de productos desde el inventario.
· Cálculo automático del total de la venta.
· Registro de transacciones y generación de facturas en PDF.
· Almacenamiento de cada venta en la base de datos database.db.

🧰 Otras características

· Interfaz gráfica desarrollada con Tkinter, con íconos y temas visuales personalizados.
· Manejo de imágenes mediante la librería Pillow.
· Integración de base de datos SQLite3 para almacenar la información de manera persistente.
· Compatible con la conversión a ejecutable .exe mediante PyInstaller.

🗂️ Base de Datos

La base de datos utilizada (database.db) fue diseñada y gestionada con DB Browser for SQLite.
Contiene las siguientes tablas principales:

· productos → información de inventario.
· ventas → registro de facturas generadas.

🧑‍💻 Autor

· Nombre: Marcos J. M.
· Materia: SIS-2420 — Programación
· Lenguaje: Python
· Entorno: Visual Studio Code
· Gestión: II/2025

📄 Licencia

Proyecto académico sin fines comerciales.
Uso libre con fines educativos o de práctica.

Este proyecto refleja la aplicación práctica de Python en la creación de sistemas de inventario con interfaz gráfica, manejo de bases de datos y generación automática de documentos.
