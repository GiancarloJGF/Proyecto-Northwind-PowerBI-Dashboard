# Proyecto-Northwind-PowerBI-Dashboard

Análisis completo de la base de datos Northwind usando Power BI Desktop.
4 dashboards especializados que simulan reportes reales de distintas
áreas de negocio: ventas, logística, inventario y RRHH.

---

## Screenshots

### 1. Dashboard de ventas (enfoque ejecutivo)
![Dashboard Ventas](1. Dashboard de Rendimiento de Ventas (Enfoque Ejecutivo))

### 2. Análisis de logística y envíos
![Dashboard Logística](screenshots/02-logistica.png)

### 3. Gestión de inventario y proveedores
![Dashboard Inventario](screenshots/03-inventario.png)

### 4. Desempeño del equipo de ventas
![Dashboard Empleados](screenshots/04-empleados.png)

---

## Herramientas utilizadas
- **Power BI Desktop** — visualizaciones e informes
- **SQL Server** — base de datos fuente (Northwind)
- **DAX** — medidas calculadas y Time Intelligence

## KPIs y medidas DAX principales
| Medida | Descripción |
|--------|-------------|
| `Ingresos Totales` | UnitPrice × Quantity × (1 - Discount) |
| `Total Órdenes` | DISTINCTCOUNT de OrderID |
| `Ticket Promedio` | Ingresos / Total Órdenes |
| `Crecimiento YoY %` | Comparación año actual vs anterior |
| `Días de Entrega` | DATEDIFF entre OrderDate y ShippedDate |

## Cómo usar
1. Clona el repositorio
2. Ejecuta `sql/instnwnd.sql` en SQL Server
3. Abre `Northwind_Dashboard.pbix` en Power BI Desktop
4. Actualiza la cadena de conexión a tu servidor

## Dataset
Base de datos **Northwind** de Microsoft.
Fuente: [sql-server-samples](https://github.com/microsoft/sql-server-samples)
