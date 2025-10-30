# ETL — Medallion (Databricks / Delta Lake)

Proyecto educativo de Ingeniería de Datos que implementa una **arquitectura Medallion** en **Databricks** con **Delta Lake**:

- **Bronze**: ingesta cruda y persistente.  
- **Silver**: limpieza, normalización y **chequeos de integridad referencial**.  
- **Gold**: cálculos de negocio, particiones y *time travel*.

> Stack: Databricks Community Edition · Delta Lake · SQL (notebooks).

---

## 🗺️ Visión general


- **Objetivo**: pipeline de punta a punta con buenas prácticas (idempotencia, limpieza, controles, particiones).

- **Datos**: empleados.csv, locales.csv, producto.csv, fact.csv.

- **Dónde**: Databricks CE. Notebooks: 01_bronze_ingestion, 02_silver_transformation, 03_gold_aggregations.
