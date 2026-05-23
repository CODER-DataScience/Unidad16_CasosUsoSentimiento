# Unidad 16 · Casos de uso del análisis de sentimiento

## 🎯 Objetivo
Diseñar un esquema básico y aplicable de métricas para evaluar el impacto del análisis de sentimiento en un caso de uso empresarial.  
El caso seleccionado es **Gestión de crisis**, donde el análisis de sentimiento permite detectar tempranamente un aumento en menciones negativas y activar protocolos de respuesta rápida para reducir el impacto reputacional.

---

## 📌 Caso de uso: Gestión de crisis
El análisis de sentimiento aplicado a gestión de crisis ayuda a:
- Detectar señales tempranas de crisis reputacional.
- Priorizar la respuesta de comunicación y soporte.
- Reducir el impacto financiero y en la confianza del cliente.

---

## 🎯 Objetivos específicos
1. Reducir el tiempo de respuesta a menciones negativas.  
2. Detectar tendencias que anticipen una crisis.  
3. Mejorar la precisión en la clasificación de comentarios críticos.  

---

## 📊 Métricas definidas
| Métrica                  | Qué mide | Cómo calcular | Acción/Decisión habilitada |
|--------------------------|----------|---------------|----------------------------|
| Recall clase negativa    | Proporción de menciones negativas correctamente detectadas | TP_neg / (TP_neg + FN_neg) | Evita que se escapen reclamos graves |
| Accuracy ponderada       | % de clasificaciones correctas ajustado por desbalance | sum(w_i * acc_i) | Reduce riesgo de métricas infladas por clases mayoritarias |
| Tiempo de respuesta      | Tiempo entre publicación y detección | timestamp_detectado - timestamp_publicado | Evalúa eficiencia del pipeline de crisis |

---

## 📌 Justificación de métricas
- **Recall negativo**: crítico para no dejar pasar reclamos graves (riesgo: falsos negativos).  
- **Accuracy ponderada**: evita métricas engañosas en datasets desbalanceados (riesgo: sobrevalorar clase mayoritaria).  
- **Tiempo de respuesta**: directamente ligado al impacto reputacional y financiero (riesgo: demora en activar protocolos).  

---

## 📡 Método de recolección de datos
- **Fuente de datos**: menciones en redes sociales (Twitter API), tickets de soporte, reseñas.  
- **Datos necesarios**: texto, etiqueta de sentimiento (manual o automática), timestamp.  
- **Set de evaluación**: muestreo semanal, validación manual de un subset.  
- **Frecuencia**: batch diario o streaming en tiempo real para crisis.  

---

## 📂 Archivos del proyecto
- `data/ejemplos.csv`: dataset simulado con menciones positivas y negativas.  
- `notebooks/ejercicio_metricas.ipynb`: notebook con cálculo de métricas e interpretación.  
- `README.md`: documentación del caso, objetivos, métricas y pipeline.  
