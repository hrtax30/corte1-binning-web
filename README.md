# Corte 1 — Agrupamiento por Rangos (Binning)

**Demo:** https://hrtax30.github.io/corte1-binning-web/  
**Repositorio:** https://github.com/hrtax30/corte1-binning-web

> Proyecto de programacion Web.  
> Se replica en JavaScript una hoja de Excel que normaliza datos, calcula una
> Y-sumatoria ponderada por coeficientes y aplica **binning** (rangos) con anchos 0.1 y 0.05.  
> El usuario **solo** ingresa un **Factor de multiplicación** para los coeficientes; el resto se recalcula.

---

## 🚀 ¿Qué hace la app?

- **Entrada única:** `Factor` para escalar los coeficientes.
- **Cálculos automáticos:**
  - Y sumatoria ponderada (Y1..Y7 × coeficientes × factor)
  - **Normalización min–max** de X y de la Y sumatoria
  - **Binning**:
    - 10 bins → ancho **0.1** (0.00–0.10 … 0.90–1.00)
    - 20 bins → ancho **0.05** (0.00–0.05 … 0.95–1.00)
- **Tablas**: Coeficientes · Datos crudos + Y Sumatoria · Normalización · Binning 0.1 · Binning 0.05
- **Gráficos (Chart.js)**:
  1. Y normalizado vs X normalizado
  2. Promedios por bin (0.1)
  3. Promedios por bin (0.05)
  4. Combinado (0.1 vs 0.05)

---

## 🧪 Verificación contra Excel

- Se contrastaron **361 filas** (inicio, medio y final + chequeo masivo).
- **Mayor diferencia absoluta** entre lo calculado en JS y Excel:  
  `≈ 0.00000498` (debido a redondeos). ✅

---

## 🧭 Uso

1. Abrir la **demo**: https://hrtax30.github.io/corte1-binning-web/
2. Escribir un **Factor** (ej. `1`, `0.8`, `1.2`, `10`) y pulsar **Calcular**.
3. Revisar tablas y gráficos actualizados.

> Tip: Si cambias el factor, todas las tablas y gráficos se recalculan.

---

## 🛠️ Tecnologías

- HTML + CSS
- **JavaScript**
- **Chart.js** para los gráficos

---


