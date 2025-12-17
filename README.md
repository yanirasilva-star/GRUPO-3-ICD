## Dinámica de la inflación subyacente y política monetaria en el Perú

**Pregunta de investigación**  
### *¿Cuál es la influencia de la tasa de interés de referencia en la dinámica de la inflación subyacente de corto plazo en el Perú?*

Este proyecto analiza la evolución de la inflación subyacente interanual en el Perú durante el período 2013–2025, utilizando información oficial del Banco Central de Reserva del Perú (BCRP). El trabajo combina herramientas de econometría y técnicas de *machine learning*, con un énfasis explícito en la coherencia económica, la consistencia temporal y la evaluación predictiva fuera de muestra.

El enfoque del estudio es predominantemente **predictivo y descriptivo**, más que de identificación causal estricta, y busca entender cómo la inflación subyacente responde a su propia persistencia, a las expectativas de inflación y a la postura de la política monetaria en horizontes cortos.

#### Estructura del notebook

El desarrollo del análisis se organiza en cuatro presentaciones:

##### **P1. Análisis exploratorio de datos**
Se construye una base de datos mensual a partir del API del BCRP, que incluye inflación subyacente, expectativas de inflación, tasas de interés y variables operativas de liquidez. Esta etapa aborda la limpieza, transformación temporal, análisis descriptivo, visualización de tendencias y detección de posibles outliers, interpretados como episodios macroeconómicos relevantes.

##### **TG 2. Formulación del problema supervisado de nowcasting**
Se define un esquema de predicción *one-step-ahead* (h = 1), mediante la creación de rezagos de la inflación, expectativas y variables monetarias. La construcción del dataset respeta estrictamente la causalidad temporal y evita cualquier uso de información futura. Se implementan particiones entrenamiento–prueba y validación cruzada específica para series de tiempo.

##### **TG 3. Modelado y evaluación predictiva**
Se estiman y comparan distintos modelos: baselines de persistencia, regresión OLS, Ridge Regression y modelos no lineales (Random Forest y XGBoost). El análisis incorpora diagnósticos econométricos, regularización, métricas de desempeño fuera de muestra (MSE y R²) y comparaciones sistemáticas entre enfoques lineales y no lineales.

##### **TG 4. Análisis causal y modelación no lineal**
Se desarrolla un diagrama causal (DAG) que sintetiza la estructura económica subyacente, diferenciando claramente entre reacción de política monetaria y transmisión rezagada hacia la inflación. Además, se implementa un modelo de redes neuronales tipo MLP como extensión metodológica para explorar posibles no linealidades.

#### Principales resultados
- La inflación subyacente exhibe **alta persistencia**, siendo sus propios rezagos el principal determinante de corto plazo.
- Las **expectativas de inflación rezagadas** desempeñan un rol relevante, consistente con un régimen creíble de metas de inflación.
- La **tasa de interés de referencia contemporánea** refleja principalmente la **función de reacción del BCRP**, mientras que los efectos contractivos sobre la inflación operan con rezagos.
- Los modelos lineales (OLS y Ridge) ofrecen el mejor desempeño predictivo fuera de muestra, superando a los modelos no lineales en este horizonte.
- Los enfoques de *machine learning* aportan valor complementario, pero no mejoran la precisión frente a especificaciones lineales bien diseñadas en un proceso altamente persistente.
#### Limitaciones y extensiones
El análisis se concentra en predicciones de corto plazo (h = 1). Extensiones naturales incluyen esquemas de predicción en dos etapas (filtrado de persistencia y modelación de residuos), horizontes más largos y arquitecturas dinámicas como redes LSTM, que podrían capturar mejor ajustes graduales en contextos inflacionarios más volátiles.




