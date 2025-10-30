# ETL — Medallion (Databricks / Delta Lake)

Proyecto educativo de Ingeniería de Datos que implementa una **arquitectura Medallion** en **Databricks** con **Delta Lake**:

- **Bronze**: ingesta cruda y persistente.  
- **Silver**: limpieza, normalización y **chequeos de integridad referencial**.  
- **Gold**: cálculos de negocio, particiones y *time travel*.

> Stack: Databricks Community Edition · Delta Lake · SQL (notebooks).

---

## 🗺️ Visión general

```mermaid
flowchart LR
  A[Archivos CSV] --> B[Bronze  \n raw_empleados/raw_producto/raw_locales/raw_ventas]
  B --> C[Silver \n dim_vendedor / dim_producto / fact_ventas]
  C --> D[Gold \n fact_ventas_final \n (particionada por mes + monto_total)]
