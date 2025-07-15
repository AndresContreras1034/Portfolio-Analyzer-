# 📊 Portfolio Analyzer (versión inicial en desarrollo)

Este proyecto es una herramienta escrita en Python para analizar y visualizar el crecimiento de inversiones personales a lo largo del tiempo. Está diseñada con una estructura modular y clara, ideal para ampliaciones futuras (como conectarse a APIs o agregar una interfaz gráfica).

---

## 🗂️ Estructura del proyecto

```
portfolio-analyzer/
├── data/
│   ├── raw/           # Archivos de entrada originales (ej. CSV con inversiones)
│   └── processed/     # Archivos limpios o transformados listos para análisis
│
├── src/               # Código fuente principal del sistema
│   ├── loader.py      # Carga y guardado de archivos CSV
│   ├── analyzer.py    # Lógica de análisis financiero (ROI, ganancias, etc.)
│   ├── visualizer.py  # Gráficas de crecimiento y distribución de activos
│   └── utils.py       # Funciones auxiliares como formato de moneda
│
├── notebooks/         # Notebooks exploratorios opcionales (visualización manual)
│
├── reports/
│   ├── graphs/        # Imágenes de gráficas generadas automáticamente
│   └── summary.md     # Reporte resumen de métricas principales
│
├── tests/             # Pruebas unitarias para las funciones clave
│
├── main.py            # Script principal que une todo el flujo
├── requirements.txt   # Dependencias necesarias (pandas, matplotlib)
└── README.md          # Documentación general del proyecto
```

---

## 🔄 Flujo general del sistema

1. **main.py** ejecuta el flujo completo:
   - Usa `loader.py` para cargar `data/raw/investments.csv`
   - Procesa y analiza los datos con `analyzer.py`
   - Genera visualizaciones automáticas con `visualizer.py`
   - Muestra resultados por consola y guarda gráficas en `reports/graphs/`

2. **El archivo de entrada (`investments.csv`)** debe tener columnas como:
   - `Date`, `Asset`, `Amount`, `Value`

3. **Se guardan datos limpios en `data/processed/`** y las gráficas finales en `reports/graphs/`.

---

## 🛠️ En desarrollo

Este proyecto está en construcción. A futuro se incluirán:

- Integración con APIs externas de precios en tiempo real
- Dashboards interactivos con Plotly o Streamlit
- Módulo de autenticación y sesiones (para uso personal seguro)

---

## ▶️ Próximo paso

1. Completar la base de `src/` y `main.py`
2. Probar todo con un CSV de ejemplo
3. Subir el repositorio a GitHub con commits limpios y documentados

---

## 📦 Instalación rápida (cuando esté listo)

```bash
pip install -r requirements.txt
python main.py
```
```

Prueba de UML

classDiagram
    class Usuario {
        +String nombre
        +String correo
        +registrar()
        +login()
    }

    class Pedido {
        +int id
        +Date fecha
        +agregarProducto()
        +calcularTotal()
    }

    class Producto {
        +String nombre
        +double precio
        +String categoria
    }

    class Carrito {
        +List<Producto> productos
        +agregarProducto()
        +eliminarProducto()
        +vaciar()
    }

    Usuario --> Carrito : tiene
    Carrito --> Producto : contiene
    Usuario --> Pedido : realiza
    Pedido --> Producto : incluye
