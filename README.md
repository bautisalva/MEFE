# MEFE

Este repositorio contiene un notebook de análisis estadístico para evaluar la **efectividad de una aplicación móvil de aprendizaje de idiomas**. El caso surge de un ejercicio de métodos estadísticos y funciones de estimación (MEFE).

## Contexto

Un equipo de desarrolladores lanzó una nueva app para mejorar la **retención de vocabulario** en estudiantes de idiomas extranjeros.  
Para medir su impacto, se diseñó un experimento con dos grupos:

- **Grupo A (control):** estudiantes usando métodos tradicionales.
- **Grupo B (experimental):** estudiantes usando la app.

Cada estudiante realizó:
- 20 pruebas diarias durante 1 mes (~600 pruebas por grupo).
- En cada prueba: recordar 10 palabras nuevas.

Se modela cada prueba como:
\[
X ~ Binomial(n=10, p)
\]

Donde:
- \( p \): probabilidad de recordar una palabra.
- Hipótesis nula: \( H_0: f = 0 \).
- Hipótesis alternativa: \( H_1: f > 0 \), donde \( f \) es la mejora en la probabilidad gracias a la app.

---

## ¿Qué hace este notebook?

- **Simula datos** de pruebas binomiales para Grupo A y Grupo B.
- **Calcula razones de verosimilitud** para contrastar \( H_0 \) vs. \( H_1 \).
- Usa **simulaciones Monte Carlo** para estimar:
  - Distribuciones bajo \( H_0 \) y \( H_1 \)
  - Curvas de potencia.
  - Probabilidad de error tipo II.
  - Tamaño mínimo de efecto detectable.
- Genera **gráficos** para visualizar resultados clave.
