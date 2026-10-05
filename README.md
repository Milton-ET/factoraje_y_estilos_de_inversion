# Modelo de Factoraje y Análisis de Estilos de Inversión (Sharpe & Fama-French)

## Descripción del Proyecto
Este proyecto desarrolla e implementa modelos econométricos cuantitativos en Python para descomponer los rendimientos de activos y portafolios de inversión en función de factores de riesgo sistemáticos y estilos de inversión.

Se evalúa el comportamiento empírico de acciones como **Berkshire Hathaway (BRK-A)** y **Microsoft (MSFT)**, el mercado industrial de EE. UU. (30 y 49 industrias), y fondos indexados como **Vanguard 500 Index Investor (VFINX)**.

## Metodologías Aplicadas
1. **Capital Asset Pricing Model (CAPM):** Evaluaciones de beta ($\beta$) de mercado y generación de alpha ($\alpha$) mediante regresión OLS.
2. **Modelo de 3 Factores de Fama-French:** Descomposición de retornos utilizando exceso de mercado ($Mkt-RF$), tamaño ($SMB$) y valor ($HML$).
3. **Análisis de Estilo de Sharpe (Returns-Based Style Analysis - RBSA):** Optimización cuadrática restringida con el algoritmo `SLSQP` ($\sum w_i = 1, w_i \ge 0$) para inferir asignaciones sectoriales e identificación de *Style Drift* mediante ventanas móviles de 5 años (*rolling windows*).

## Resultados Clave
* **BRK-A:** Muestra una evolución hacia el factor de valor ($HML$) a lo largo del tiempo, manteniendo exposición nula al factor de pequeña capitalización ($SMB$), consistente con la filosofía de inversión en empresas consolidadas de Warren Buffett.
* **VFINX:** El análisis de *rolling window* confirmó un perfil estable correspondiente a la categoría *Large Blend*, alineándose estrechamente con la clasificación oficial de Morningstar.

## Estructura del Repositorio
* `notebooks/`: 
  * `Portfolio_proyect.ipynb`: Código fuente interactivo con las estimaciones econométricas, optimizaciones OLS/SLSQP y visualizaciones de *Style Drift*.
* `data/`:
  * `brka_d_ret.csv`: Rendimientos diarios de Berkshire Hathaway y Microsoft.
  * `F-F_Research_Data_Factors_m.csv`: Factores mensuales de Fama-French (Mkt-RF, SMB, HML, RF).
  * `ind30_m_vw_rets.csv`: Rendimientos mensuales ponderados por valor de 30 industrias de EE. UU.
  * `ind49_m_vw_rets.csv`: Rendimientos mensuales ponderados por valor de 49 industrias de EE. UU.
* `docs/`:
  * `Rep_3_E1.pdf`: Reporte ejecutivo final con las interpretaciones teóricas y financieras.
  * `Cod_3_E1.pdf`: Documentación del código fuente y salidas del modelo en PDF.

## Colaboradores
Proyecto realizado en colaboración académica para la Licenciatura en Actuaría (BUAP):
* Mateo Vega Vázquez
* Julián Jesús Coatl Cienfuegos
* Ulises Galicia Flores
* Milton Escobar Trujillo