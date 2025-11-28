### GRUPO-3-ICD
# ¿Cuál es la influencia de la tasa de interés de referencia en la dinámica de la inflación en el corto plazo en el Perú?

Este proyecto estudia la dinámica de la inflación subyacente interanual en el Perú entre 2013 y 2025, utilizando información del Banco Central de Reserva del Perú y aplicando técnicas econométricas y de *machine learning*. El objetivo principal es comprender qué factores explican su comportamiento en el corto plazo y evaluar la capacidad predictiva de distintos modelos.

El desarrollo del trabajo avanzó de manera progresiva. En la primera etapa (T1) se construyó la base de datos a partir del API del BCRP, realizando la limpieza, ordenamiento y preparación de las series. En la segunda etapa (T2) se formuló el problema supervisado mediante la creación de rezagos para la inflación, las expectativas y las variables de política monetaria, asegurando consistencia temporal y causalidad. La tercera etapa (T3) estuvo dedicada a la estimación y comparación de modelos como OLS, Ridge y Random Forest, incorporando validación cruzada para series de tiempo, análisis de diagnósticos, exploración de multicolinealidad y evaluación de desempeño predictivo.

La etapa final (T4) añadió dos componentes clave. El primero fue el diagrama causal (**GAP**) elaborado con la librería *daft*, que resume la estructura conceptual del modelo: la persistencia inflacionaria, el rol de las expectativas, la transmisión de la política monetaria a través de la tasa de referencia y la presencia de shocks externos. El segundo componente fue la implementación de un modelo de redes neuronales tipo **MLP**, con el propósito de identificar posibles no linealidades. Aunque el MLP mostró un desempeño adecuado, no superó a los modelos lineales, lo que confirma el carácter altamente persistente y casi lineal de la inflación subyacente en el Perú.

En conjunto, el proyecto evidencia que la inflación subyacente está impulsada principalmente por su propia inercia y por las expectativas rezagadas, mientras que la tasa de referencia del BCRP constituye el principal canal de transmisión de la política monetaria. Los modelos lineales resultan ser los más estables e interpretables, y las técnicas no lineales ofrecen una visión complementaria. El repositorio incluye el código, las visualizaciones y la documentación completa del proceso desarrollado desde T1 hasta T4.





