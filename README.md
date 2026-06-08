# Proyecto-Northwind-PowerBI-Dashboard

Análisis completo de la base de datos Northwind usando Power BI Desktop.
4 dashboards especializados que simulan reportes reales de distintas
áreas de negocio: ventas, logística, inventario y RRHH.

---

## Screenshots

### 1. Dashboard de ventas (enfoque ejecutivo)
![Dashboard Ventas](1. Dashboard de Rendimiento de Ventas (Enfoque Ejecutivo))
<img width="587" height="319" alt="image" src="https://github.com/user-attachments/assets/645ee9a1-8423-4268-b5dd-b6555c1d594b" />

### 2. Análisis de logística y envíos
![Dashboard Logística](2. Análisis de Logística y Envíos (Enfoque de Operaciones))
<img width="587" height="318" alt="image" src="https://github.com/user-attachments/assets/aa10ea5b-4625-4743-8cbd-d800693304ba" />

### 3. Gestión de inventario y proveedores
![Dashboard Inventario](3. Gestión de Inventario y Proveedores (Enfoque de Compras))
<img width="586" height="316" alt="image" src="https://github.com/user-attachments/assets/e1eb87ac-f005-44dc-8c5f-39afa8c8bb5b" />

### 4. Desempeño del equipo de ventas
![Dashboard Empleados]4. Desempeño del Equipo de Ventas (Enfoque de Recursos Humanos))
<img width="590" height="333" alt="image" src="https://github.com/user-attachments/assets/b4853307-f896-46fc-a8e7-a9fb56fbebfc" />

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
