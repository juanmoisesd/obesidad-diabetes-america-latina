# Obesidad y Diabetes en América Latina (2000–2024)

> Base de datos epidemiológica, clínica y salud-económica sobre obesidad y diabetes tipo 2 en América Latina.

[![Mendeley Data](https://img.shields.io/badge/Mendeley%20Data-9z2vs38byh-red)](https://data.mendeley.com/drafts/9z2vs38byh)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Dataset](https://img.shields.io/badge/Archivos-21-blue)]()

## 📋 Descripción

Este repositorio contiene datos epidemiológicos, clínicos y económico-sanitarios sobre **obesidad** y **diabetes tipo 2** en América Latina para el período 2000–2024. Cubre 18 países y compila datos de prevalencia, mortalidad, costos directos por paciente, acceso a insulina, factores de riesgo metabólico y programas nacionales de intervención.

**Repositorio Mendeley Data:** [9z2vs38byh](https://data.mendeley.com/drafts/9z2vs38byh)  
**Dataset paralelo en inglés:** [obesity-diabetes-latin-america](https://github.com/juanmoisesd/obesity-diabetes-latin-america)

## 🌍 Cobertura Geográfica

Argentina · Bolivia · Brasil · Chile · Colombia · Costa Rica · Cuba · Ecuador · El Salvador · Guatemala · Honduras · México · Nicaragua · Panamá · Paraguay · Perú · Uruguay · Venezuela

## 📊 Estadísticas Clave (2024)

| Indicador | Valor |
|-----------|-------|
| Prevalencia media de diabetes (región) | 10.8% (IDF 2023) |
| País con mayor prevalencia | México (15.2%) |
| Adultos con diabetes en LATAM | 34.2 millones |
| Sin diagnóstico | ~40% |
| Costo anual estimado | USD 59.4 mil millones |
| Muertes atribuibles/año | ~290,000 |

## 📁 Estructura del Repositorio

```
obesidad-diabetes-america-latina/
├── analysis_notebook.ipynb          # Notebook Jupyter de análisis
├── prevalencia_obesidad_diabetes_latam.csv    # Prevalencias por país y año
├── mortalidad_diabetes_latam.csv              # Mortalidad por país y año
├── costos_sanitarios_por_pais.csv            # Costos directos en USD
├── idf_atlas_resumen.csv                     # Resumen Atlas IDF 2009–2023
├── tendencias_imc_latam.csv                  # Tendencias de IMC adultos
├── indicadores_paho_diabetes.csv             # Indicadores PAHO por país
├── factores_riesgo_metabolico.csv           # Hipertensión, colesterol, etc.
├── diabetes_por_edad_sexo.csv               # Desagregación edad/sexo
├── obesidad_ninos_adolescentes.csv          # Niños y adolescentes
├── programas_nacionales_diabetes.csv        # Programas de intervención
├── entorno_alimentario_latam.csv            # UPF, SSB, disponibilidad
├── acceso_insulina_asequibilidad.csv        # Acceso y precios de insulina
├── complicaciones_diabetes.csv             # Nefropatía, retinopatía, etc.
├── gasto_pib_salud_comparativo.csv         # GDP y gasto sanitario
├── politicas_obesidad_latam.md             # Resumen de políticas nacionales
├── revision_literatura_diabetes.bib        # Referencias bibliográficas
├── notas_metodologicas.md                  # Metodología y fuentes
├── diccionario_de_datos.md                 # Descripción de variables
└── estadisticas_resumen_regional.json      # Estadísticas consolidadas
```

## 🔬 Fuentes de Datos

| Fuente | Variables | Acceso |
|--------|-----------|--------|
| **IDF Diabetes Atlas** (ediciones 4–11, 2009–2023) | Prevalencia, sin diagnóstico, carga económica | [diabetesatlas.org](https://diabetesatlas.org) |
| **PAHO ENLACE** | Mortalidad, comorbilidades, cobertura | [enlace.paho.org](https://www.paho.org/es/enlace) |
| **OMS Global Health Observatory** | IMC, inactividad física, factores de riesgo | [who.int/data/gho](https://www.who.int/data/gho) |
| **Banco Mundial (HNP)** | PIB, gasto sanitario, gasto de bolsillo | [datatopics.worldbank.org](https://datatopics.worldbank.org/health) |
| **Encuestas Nacionales** | ENSANUT (México), PNS (Brasil), ENS (Chile), ENSIN (Colombia) | Ministerios de salud |

## 📈 Variables Principales

- **Prevalencia (%)** de obesidad (IMC≥30) y diabetes (adultos 20–79) por país/año
- **Mortalidad** estandarizada por edad (por 100,000 habitantes)
- **Costos directos** por paciente diabético (USD 2022 PPP)
- **Acceso a insulina**: precio en sector público vs privado, cobertura (%)
- **Factores de riesgo**: hipertensión, colesterol, síndrome metabólico, inactividad física
- **Complicaciones**: nefropatía, retinopatía, amputaciones, ERCA
- **Entorno alimentario**: ventas de UPF per cápita, consumo de bebidas azucaradas

## 🚀 Uso Rápido

```python
import pandas as pd
import matplotlib.pyplot as plt

# Cargar datos de prevalencia
df = pd.read_csv('prevalencia_obesidad_diabetes_latam.csv')

# Tendencia por país
fig, ax = plt.subplots(figsize=(12, 5))
for pais in ['Mexico', 'Brazil', 'Argentina', 'Colombia', 'Chile']:
    sub = df[df['country'] == pais]
    ax.plot(sub['year'], sub['diabetes_prevalence_pct'], label=pais, marker='o')
ax.set_title('Prevalencia de Diabetes (%) 2000–2024')
ax.legend()
plt.tight_layout()
plt.savefig('diabetes_tendencias.png', dpi=150)
```

## 📄 Licencia

Este dataset se distribuye bajo licencia [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).  
Puedes usar, compartir y adaptar los datos siempre que cites la fuente.

## 📚 Cita Sugerida

> De la Serna, Juan Moisés. *Obesidad y Diabetes en América Latina (2000–2024): Prevalencia, Mortalidad y Costos Sanitarios por País*. Mendeley Data, 2024. Dataset ID: 9z2vs38byh. GitHub: juanmoisesd/obesidad-diabetes-america-latina

## 🔗 Recursos Relacionados

- 🇬🇧 **English version:** [obesity-diabetes-latin-america](https://github.com/juanmoisesd/obesity-diabetes-latin-america) (Mendeley: k8ksc5zxyr)
- 📊 **Cambio Climático:** [cambio-climatico-espana-iberoamerica](https://github.com/juanmoisesd/cambio-climatico-espana-iberoamerica)
- 🔐 **Ciberseguridad:** [ciberseguridad-america-latina](https://github.com/juanmoisesd/ciberseguridad-america-latina)
