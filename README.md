# Proyecto-Northwind-PowerBI-Dashboard

Análisis completo de la base de datos Northwind usando Power BI Desktop.
4 dashboards especializados que simulan reportes reales de distintas
áreas de negocio: ventas, logística, inventario y RRHH.

---

## Screenshots


### 1. Dashboard de ventas (enfoque ejecutivo)
Este sería el reporte principal. Ideal para directores que quieren ver la salud financiera de la empresa de un vistazo.
Métricas Clave (KPIs): Ingresos totales (calculando UnitPrice * Quantity * (1 - Discount)), número de órdenes, ticket promedio y margen de descuento promedio.
Visualizaciones recomendadas:
Gráfico de líneas: Evolución de las ventas mes a mes (análisis de tendencias).
Mapa: Ventas por país o región de facturación (ShipCountry).
Gráfico de barras: Top 5 clientes que más generan ingresos y Top 5 productos más vendidos.
Plus para GitHub: Añade un filtro de fecha inteligente (Time Intelligence) para comparar el año actual contra el año anterior (YoY Growth) usando DAX.

![Dashboard Ventas](1. Dashboard de Rendimiento de Ventas (Enfoque Ejecutivo))
<img width="587" height="319" alt="image" src="https://github.com/user-attachments/assets/645ee9a1-8423-4268-b5dd-b6555c1d594b" />


### 2. Análisis de logística y envíos
Northwind tiene datos geniales sobre tiempos de entrega. Este reporte demostrará que sabes optimizar procesos.
Métricas Clave (KPIs): Días promedio de envío (diferencia entre OrderDate y ShippedDate), porcentaje de pedidos retrasados (comparando RequiredDate con ShippedDate) y costo total de flete (Freight).
Visualizaciones recomendadas:
Gráfico de embudo o barras: Rendimiento de las empresas de envío (Shippers). ¿Cuál es la más rápida? ¿Cuál es la más cara?
Tabla dinámica / Matriz: Países de destino con mayores retrasos promedio.
Tarjetas condicionales: Que cambien a color rojo si el promedio de días de retraso supera un límite.

![Dashboard Logística](2. Análisis de Logística y Envíos (Enfoque de Operaciones))
<img width="587" height="318" alt="image" src="https://github.com/user-attachments/assets/aa10ea5b-4625-4743-8cbd-d800693304ba" />


### 3. Gestión de inventario y proveedores
Aquí demuestras cómo ayudarías al departamento de compras a no quedarse sin stock.
Métricas Clave (KPIs): Total de productos en stock, productos descontinuados y valor total del inventario.
Visualizaciones recomendadas:
Gráfico de dispersión (Scatter plot): Unidades en stock vs. Unidades ordenadas (UnitsInStock vs. UnitsOnOrder) por producto, para identificar cuáles necesitan reabastecimiento urgente.
Treemap: Distribución del catálogo por categorías de productos.
Tabla con alertas: Lista de productos que están por debajo del nivel de reorden (ReorderLevel).

![Dashboard Inventario](3. Gestión de Inventario y Proveedores (Enfoque de Compras))
<img width="586" height="316" alt="image" src="https://github.com/user-attachments/assets/e1eb87ac-f005-44dc-8c5f-39afa8c8bb5b" />


### 4. Desempeño del equipo de ventas
Un análisis del comportamiento de los empleados de Northwind.
Métricas Clave (KPIs): Ventas totales por empleado, cantidad de órdenes gestionadas y promedio de descuento otorgado por cada uno (para ver quién "regala" más margen).
Visualizaciones recomendadas:
Gráfico de barras apiladas: Ventas de cada empleado divididas por región o territorio.
Gráfico de radar o matriz de desempeño: Comparativa de empleados según sus ventas vs. sus tiempos de procesamiento de órdenes.

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
