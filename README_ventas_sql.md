# 🛒 Análisis de Ventas con Python + SQL (SQLite)

Proyecto de análisis de datos end-to-end: diseño de base de datos relacional, carga de datos, consultas SQL avanzadas y visualización de resultados con Python.

---

## 🎯 Objetivo

Simular el flujo de trabajo de un analista de datos en una distribuidora:
- Diseñar e implementar un **esquema relacional** con múltiples tablas
- Cargar y gestionar datos con **SQLite desde Python**
- Extraer insights de negocio con **consultas SQL avanzadas**
- Visualizar los resultados con **Matplotlib y Seaborn**

---

## 🛠️ Tecnologías utilizadas

| Herramienta | Uso |
|-------------|-----|
| Python 3    | Lenguaje base |
| SQLite      | Base de datos relacional embebida |
| Pandas      | Lectura de queries SQL y análisis |
| Matplotlib  | Visualizaciones personalizadas |
| Seaborn     | Gráficos estadísticos |

---

## 🗃️ Esquema de la base de datos

```
clientes ──┐
           ├── ventas ── detalle_ventas ── productos
vendedores─┘
```

| Tabla           | Descripción                            |
|-----------------|----------------------------------------|
| `vendedores`    | Equipo de ventas con región asignada   |
| `clientes`      | Clientes con segmento y provincia      |
| `productos`     | Catálogo con categoría y precio        |
| `ventas`        | Cabecera de cada transacción           |
| `detalle_ventas`| Líneas de productos por venta          |

---

## 📊 Análisis realizados

1. **Facturación mensual** — evolución temporal con doble eje (USD y cantidad de ventas)
2. **Ranking de vendedores** — facturación y cantidad de ventas por vendedor
3. **Participación por categoría** — pie chart + barras comparativas
4. **Top 5 clientes** — usando CTE (`WITH ... AS`)
5. **Variación mensual** — usando Window Functions (`LAG`, `SUM OVER`)

---

## 🧠 Técnicas SQL utilizadas

- `JOIN` entre múltiples tablas
- `GROUP BY` con funciones de agregación (`SUM`, `COUNT`, `AVG`)
- **CTE** — Common Table Expressions (`WITH ... AS`)
- **Window Functions** — `LAG()`, `SUM() OVER()`
- Cálculo de porcentajes en SQL puro

---

## 🚀 Cómo ejecutar

```bash
# 1. Clonar el repositorio
git clone https://github.com/blenddzy/analisis-ventas-sql.git
cd analisis-ventas-sql

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Abrir el notebook
jupyter notebook analisis_ventas_sql.ipynb
```

> El notebook crea y puebla la base de datos automáticamente al ejecutarse.

---

## 👤 Autor

**Federico Gregori** — Analista de Negocios & Técnico en Ciencia de Datos  
📍 Córdoba, Argentina  
🔗 [LinkedIn](https://www.linkedin.com/in/fgregori995) · [GitHub](https://github.com/blenddzy)
