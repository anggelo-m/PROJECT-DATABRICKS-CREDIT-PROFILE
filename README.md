# Azure Databricks Data Engineer – Credit Profile Project

Repositorio que contiene el desarrollo completo de un proyecto analítico en **Azure Databricks** enfocado en la evaluación y análisis de perfiles crediticios para el sector bancario/retail. Se implementa un pipeline ETL utilizando la **Arquitectura Medallion (Bronze / Silver / Gold)** para procesar grandes volúmenes de datos financieros y de clientes.

Las fuentes de datos provienen de:
* **Datos de Clientes** (`application_record.csv`)
* **Historial Crediticio / Transacciones** (`credit_record.csv`)

## 🔹 Arquitectura General

* **Ingesta:** Carga de archivos CSV hacia Azure Data Lake / Databricks.
* **Procesamiento:** Transformación a escala con Azure Databricks (PySpark / Spark SQL).
* **Gobierno de datos:** Gestión unificada con Unity Catalog.
* **Orquestación:** Automatización con Jobs de Databricks.
* **Visualización:** Consumo de datos con Power BI y Databricks SQL.

**Servicios Provisionados en Azure:**
![Servicios Provisionados Azure](evidencias/Servicios%20provisionados%20Azure.JPG)

**Arquitectura del proyecto:**

![Arquitectura del Proyecto](evidencias/diagrama%20de%20proyecto.png)

## 🔹 Tecnologías Utilizadas

* Azure Databricks
* Azure Data Lake Storage Gen2
* Python (PySpark)
* Unity Catalog
* Power BI
* GitHub (CI/CD)

## 🔹 Arquitectura Medallion

* **🟤 Bronze:** Ingesta e incorporación de datos crudos (`01_ingestion` y `02_ingestion`).
* **⚪ Silver:** Limpieza, estandarización y enriquecimiento para generar una vista unificada del cliente (`03_transform` y `04_transform`).
* **🟡 Gold:** Modelado dimensional y agregados listos para consumo analítico y cálculo de riesgo (`05_load`).

## 🔹 Orquestación y Pipeline

El pipeline está completamente automatizado y orquestado. A continuación se muestra la evidencia de la configuración y ejecución exitosa del flujo completo, asegurando que los datos viajen desde la ingesta hasta la capa Gold sin errores.

**Tipo de Workflow GitHub:**
![Configuración del Workflow](evidencias/workflow%20GitHub.JPG)

**Tipo de Workflow Configurado:**
![Configuración del Workflow](evidencias/type%20of%20workflow.JPG)

**Ejecución Exitosa del Workflow:**
![Resultado del Workflow](evidencias/workflow%20execution.JPG)

## 🔹 Consumo Analítico

La capa **Gold** es consumida para construir dashboards interactivos enfocados en el análisis de clientes y distribución de riesgo crediticio, aportando valor directo a la toma de decisiones.

**Dashboard en Power BI:**
![Dashboard de Análisis Crediticio en Power BI](dashboard/dashboard%20Power%20Bi.JPG)

**Dashboard en Databricks:**
![Dashboard en Databricks](dashboard/dashboard%20Databricks.JPG)

## 🔹 Estructura del Repositorio

```text
PROJECT-DATABRICKS-CREDIT-PROFILE/
├── .github/                          
│   └──  deply-notebook.yml            # CI/CD Databricks
├── PrepAmb                          
│   └──  preparacion_ambiente.ipynb    # Preparacion de Ambiente
├── certificaciones
├── dashboard
│   ├── dashboard Databricks.JPG           # Captura de visualización en Databricks
│   └── dashboard Power Bi.JPG             # Captura del dashboard final en Power BI
├── datasets/                          # Archivos de origen de datos
│   ├── application_record.csv
│   └── credit_record.csv
├── evidencias/                        # Capturas de ejecución y arquitectura en Azure
│   ├── Servicios provisionados Azure.JPG
│   ├── diagrama de proyecto.png
│   ├── type of workflow.JPG
│   ├── workflow GitHub.JPG
│   └── workflow execution.PNG
├── proceso/                           # Notebooks de procesamiento ETL (Medallion)
│   ├── 01_ingestion_application_record.ipynb
│   ├── 02_ingestion_credit_record.ipynb
│   ├── 03_transform_application_record.ipynb
│   ├── 04_transform_credit_record.ipynb
│   └── 05_load.ipynb
├── reversion/                         # Scripts para limpieza y eliminación de objetos
└── seguridad/                         # Scripts para permisos y conexiones con servicios externos
```
## 👤 Autor

**Anggelo Murillo** *Data Engineer | Data Scientist | Ingeniero Mecatrónico*

🎓 **Acreditación:** Databricks Lakehouse Fundamentals

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)]([https://www.linkedin.com/in/TU-ENLACE-AQUI](https://www.linkedin.com/in/anggelo-murillo-cordova-627bb217b/))
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/anggelo-m)
