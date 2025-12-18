# 🛡️ Proyecto_Deteccion_Fraude

## 📌 Descripción General
Este proyecto implementa un **pipeline completo de datos** para la **detección de fraude en transacciones financieras**, integrando **Data Engineering**, **Analytics** y **Machine Learning**.

Se utiliza la **Arquitectura Medallón (Bronze – Silver – Gold)** sobre **Databricks Free Edition y Delta Lake**, partiendo desde la generación de datasets sintéticos en Python hasta el entrenamiento de un modelo de Machine Learning para clasificación de fraude.

---

## 🎯 Objetivos del Proyecto
- 📊 Implementar un pipeline de datos escalable con Arquitectura Medallón  
- 🧹 Limpiar, transformar e integrar múltiples fuentes de datos  
- 📈 Generar análisis descriptivo para detección de patrones de fraude  
- 🤖 Entrenar un modelo de Machine Learning para clasificación binaria  
- 💼 Construir un proyecto demostrable para portafolio profesional  

---

## 🧰 Tecnologías Utilizadas

### 🐍 Lenguaje y Librerías
- Python 3
- PySpark
- PySpark ML
- Pandas
- Matplotlib

### ☁️ Plataforma
- Databricks Free Edition
- Delta Lake

### 📦 Otros
- GitHub (documentación y versionamiento)
- Jupyter Notebook (.ipynb)

---

## 🗂️ Generación de Datasets
Los datos utilizados en el proyecto fueron **generados previamente con Python**, simulando un escenario real de fraude financiero.

📁 Archivos generados en formato CSV:
- `customers.csv` → Información de clientes  
- `cards.csv` → Información de tarjetas  
- `merchants.csv` → Información de comercios  
- `devices.csv` → Información de dispositivos  
- `transactions.csv` → Transacciones financieras  

Estos archivos representan la **fuente de datos crudos (raw data)** del proyecto.

---

## 🏗️ Arquitectura Medallón

La Arquitectura Medallón organiza los datos en tres capas, asegurando calidad, trazabilidad y escalabilidad.

---

### 🥉 Bronze – Datos Crudos
📥 Ingesta directa de los archivos CSV:
- Datos cargados sin transformaciones
- Conserva el estado original de la información
- Permite auditoría y trazabilidad

✔️ Objetivo: preservar los datos tal como llegan

---

### 🥈 Silver – Datos Procesados
🧹 Limpieza y estandarización de los datos:
- Conversión de tipos de datos
- Eliminación de inconsistencias
- Separación lógica de entidades:
  - Clientes
  - Tarjetas
  - Comercios
  - Dispositivos
  - Transacciones

✔️ Objetivo: datos confiables y estructurados

---

### 🥇 Gold – Datos Analíticos
📊 Integración final orientada a análisis:
- Unificación de todas las entidades
- Creación de columnas analíticas
- Datos listos para análisis, visualización y ML

✔️ Objetivo: datos listos para toma de decisiones

---

## 📈 Análisis de Datos (Analytics)
Sobre la capa **Gold**, se realizaron análisis descriptivos para entender el comportamiento del fraude:

- 🔢 Total de transacciones
- 🚨 Porcentaje de fraude
- 🌍 Fraude por ciudad
- 💳 Fraude por tipo de tarjeta
- 🏪 Fraude por rubro de comercio
- 💰 Distribución de montos

Estos análisis permiten identificar **patrones clave antes del modelado predictivo**.

---

## 🤖 Machine Learning – Detección de Fraude

📓 Notebook de análisis:
- `Analisis_Fraude_Brandon_Viru.ipynb`

---

### 🔧 Feature Engineering
Se seleccionaron las variables más relevantes para el modelo:

- 💰 `monto`
- 💳 `limite_credito`
- 👤 `edad`
- 📱 `es_principal`
- 🚨 `es_fraude` (variable objetivo)

Se utilizó **VectorAssembler** para construir la columna `features`, requerida por Spark ML.

---

### 🧠 Modelo Entrenado
- **Regresión Logística**
- Clasificación binaria:
  - `0` → No fraude
  - `1` → Fraude

✔️ Elegido por ser:
- Interpretable
- Eficiente
- Estándar en detección de fraude

---

### 📊 Evaluación del Modelo
- Métrica utilizada: **AUC (Area Under the ROC Curve)**

Resultado obtenido:
AUC ≈ 0.68

📌 Interpretación:
- El modelo identifica patrones reales de fraude
- Buen desempeño para un dataset sintético
- Pipeline completo validado correctamente

---

## 📁 Estructura del Repositorio
Proyecto_Deteccion_Fraude/
│
├─ notebooks/
│ ├─ Arquitectura_Medallon_Brandon_Viru.ipynb
│ ├─ Analisis_Fraude_Brandon_Viru.ipynb
│
├─ README.md


---

## 🚀 Conclusiones
- ✅ Implementación completa de Arquitectura Medallón
- ✅ Integración de Data Engineering, Analytics y ML
- ✅ Entrenamiento y evaluación de un modelo de fraude
- ✅ Proyecto alineado a buenas prácticas reales
- ✅ Ideal para portafolio profesional y académico

---

## 👨‍💻 Autor
**Brandon Viru**  
Ingeniería de Sistemas  
Data Engineering | Analytics | Machine Learning
