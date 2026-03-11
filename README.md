# Telecom-X-Parte-2
Segunda parte Challenge Telecom X 
 Informe de Retención de Clientes: Proyecto Telecom X
# 1. Resumen del Desempeño de Modelos
Tras evaluar diversos algoritmos y aplicar técnicas de balanceo (SMOTE) y normalización (StandardScaler), los resultados fueron:
•	Modelo Recomendado: Regresión Logística.
•	Capacidad de Detección (Recall): 79%. Logramos identificar a casi 8 de cada 10 clientes que están por abandonar la empresa.
•	Precisión: 51%. El modelo es sensible, lo que permite actuar preventivamente aunque genere algunas falsas alarmas (preferible en este modelo de negocio).

# 2. Factores Críticos de Cancelación (Los "Porqués")
Basado en el análisis de Importancia de Variables y Coeficientes, identificamos los tres pilares que disparan el Churn:
1.	Vulnerabilidad Contractual: Los contratos mes a mes son el predictor #1 de fuga. La falta de un compromiso a largo plazo facilita la salida del cliente ante cualquier oferta de la competencia.
2.	Barrera de Antigüedad (Tenure): Existe un "periodo crítico" en los primeros 6 a 12 meses. Si el cliente supera este tiempo, su probabilidad de fuga cae drásticamente (correlación negativa de -0.35).
3.	Incidencia Técnica/Precio en Fibra Óptica: Sorprendentemente, los clientes de Fibra Óptica tienen un mayor índice de cancelación que los de DSL, lo que sugiere una insatisfacción con el precio premium o con la estabilidad del servicio.

# 3. Estrategias de Retención Propuestas
Basándonos en la evidencia de los datos, sugerimos las siguientes acciones:
Estrategia A: Incentivo de Migración Contractual
•	Acción: Ofrecer un descuento del 15% o meses de streaming gratuitos (Netflix/Disney+) a los clientes con contrato mensual que acepten migrar a un contrato de 1 o 2 años.
•	Justificación: El modelo muestra que el contrato a largo plazo es el "escudo" más fuerte contra el Churn.
Estrategia B: Programa de "Aterrizaje Seguro" (First Year Care)
•	Acción: Implementar un seguimiento proactivo de atención al cliente durante los primeros 6 meses, incluyendo una llamada de "salud del servicio" al tercer mes.
•	Justificación: Los Boxplots demostraron que la mayoría de las cancelaciones ocurren en clientes con baja antigüedad.
Estrategia C: Auditoría de Calidad en Fibra Óptica
•	Acción: Realizar encuestas de satisfacción específicas (NPS) para el segmento de Fibra Óptica y revisar si el pricing es competitivo frente a los nuevos competidores.
•	Justificación: Es la variable con mayor correlación positiva con la fuga (0.31).

# 4. Conclusión Técnica
El proyecto demuestra que el uso de SMOTE fue fundamental para equilibrar el desbalanceo original (73/26), permitiendo que el modelo aprenda los patrones de la minoría. La estandarización permitió que variables de gran magnitud como Charges.Total no sesgaran los resultados, logrando un modelo equilibrado y altamente explicativo para la toma de decisiones gerenciales.


