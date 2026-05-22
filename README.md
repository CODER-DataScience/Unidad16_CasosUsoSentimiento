## Unidad 16 · Casos de uso del análisis de sentimiento

## 🎯 Objetivo
Diseñar un esquema básico de métricas para evaluar el impacto del análisis de sentimiento en un caso de uso empresarial.

## 📌 Caso de uso seleccionado
**Gestión de crisis**: detectar rápidamente un aumento en menciones negativas y activar protocolos de respuesta.

## ⚙️ Objetivos específicos
- Identificar cambios súbitos en la polaridad de menciones.
- Priorizar la respuesta de comunicación y soporte.
- Reducir el impacto reputacional y financiero.

## 📊 Métricas definidas
| Métrica            | Descripción | Justificación |
|--------------------|-------------|---------------|
| Tiempo de respuesta | Horas/minutos hasta detectar y reportar cambios en sentimiento | Crítico en crisis: cada minuto cuenta |
| Precisión (Accuracy) | % de clasificaciones correctas | Evita falsas alarmas y asegura foco en problemas reales |
| Cobertura (Coverage) | % de menciones analizadas vs. total | Garantiza que no se escapen volúmenes importantes |

## 📡 Método de recolección de datos
- **Pipeline de streaming** desde redes sociales y reseñas.
- Aplicación de modelo de análisis de sentimiento preentrenado.
- Dashboard con:
  - Tiempos de detección.
  - Número de menciones clasificadas vs. totales.
  - Validación manual de una muestra para calcular precisión.

## 📂 Archivos
- `notebooks/ejercicio_metricas.ipynb`: Notebook con ejemplo de simulación de datos y cálculo de métricas.
- `data/ejemplos.csv`: Dataset simulado de menciones (positivo/negativo).

---
