# Predicción del Riesgo de Enfermedad Cardiovascular usando Machine Learning y Datos Clínicos

VIDEO ENTREGA FINAL: https://youtu.be/yrthzv6COqU

## Descripción del Proyecto

Las enfermedades cardiovasculares constituyen una de las principales causas de morbilidad y mortalidad a nivel mundial, representando aproximadamente el 32% de todas las muertes globales [1]. Este proyecto aborda el desarrollo de un sistema de apoyo al tamizaje clínico basado en técnicas de Machine Learning para la detección temprana y estratificación del riesgo de enfermedad cardiovascular.

### Objetivos

- Desarrollar modelos predictivos de aprendizaje automático para clasificar el riesgo de enfermedad cardiovascular
- Identificar patrones en variables clínicas, demográficas y de comportamiento del paciente
- Validar modelos con métricas de rendimiento y seleccionar el mejor modelo

### Autores

- Camilo Cuellar
- Lukas Piedrahita  
- Felipe Uribe

Facultad de Ingeniería, Universidad de Antioquia, Medellín, Colombia

---

## Dataset

El conjunto de datos contiene **70,000 registros sin valores faltantes**, compuesto por:

| Categoría | Variables |
|-----------|-----------|
| **Información Objetiva** | Edad (días), Estatura (cm), Peso (kg), Género |
| **Resultados de Examen** | Presión sistólica (mmHg), Presión diastólica (mmHg), Colesterol (nivel), Glucosa (nivel) |
| **Factores de Comportamiento** | Consumo de tabaco, Consumo de alcohol, Actividad física |
| **Variable Objetivo** | Enfermedad Cardiovascular (0: ausencia, 1: presencia) |

**Características:**
- Dataset balanceado (≈50% prevalencia)
- Población mayoritariamente de mediana edad (48-58 años)
- Valores validados según plausibilidad clínica

---

## Uso del Notebook

### Requisitos

Este proyecto está configurado para ejecutarse en **Google Colab**, lo que facilita el acceso a recursos computacionales y evita problemas de dependencias locales.

### Instrucciones para Ejecutar en Colab

1. **Abre el notebook en Colab:**
   - Ve a [Google Colab](https://colab.research.google.com/)
   - Sube el archivo `2.Descripción_del_Problema.ipynb`
   - O clona este repositorio directamente en Colab

### Modificaciones para Ejecutar Localmente

Si deseas ejecutar el notebook localmente, necesitarás:

1. Reemplazar la línea `gdown` por una lectura directa del archivo CSV:
   ```python
   csv_path = 'ruta/local/cardio_train.csv'
   df = pd.read_csv(csv_path, sep=';')
   ```

2. Asegúrate de que las librerías necesarias estén instaladas:
   ```bash
   pip install pandas matplotlib seaborn
   ```

---

## Contenidos del Repositorio

```
├── README.md                          # Este archivo
├── 2.Descripción_del_Problema.ipynb   # Notebook principal: EDA y limpieza de datos
└── [En desarrollo: más notebooks y modelos]
```

---

## Resultados Preliminares

Después de la limpieza de datos (eliminación de 1,407 registros con valores inviables):

- **Registros válidos:** 68,593
- **Edad promedio:** 53.3 años
- **Prevalencia de enfermedad cardiovascular:** 49%
- **Correlaciones notables:**
  - Presión sistólica ↔ Enfermedad cardiovascular: 0.43
  - Presión diastólica ↔ Enfermedad cardiovascular: 0.33

---

## Referencias

[1] World Health Organization. "Cardiovascular diseases (CVDs)." 2025.

[2] G. A. Roth et al. "Global burden of cardiovascular diseases and risk factors, 1990–2019." Journal of the American College of Cardiology, vol. 76, no. 25, pp. 2982–3021, 2020.
