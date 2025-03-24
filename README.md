# Modelos de regresion lineal y series de tiempo

obtener un intervalo de confianza en un modelo de regresión lineal múltiple tras determinar el conjunto de variables significativas más adecuado

Cargamos librerías y datos a utilizar
<br>![image](https://github.com/user-attachments/assets/4ea5e374-ccd5-482f-ac5b-64ad04f65759)

Creamos los grupos de prueba y variables a utilizar
<br>![image](https://github.com/user-attachments/assets/87c72500-d1c5-4248-a0e6-1453ad095a31)

Creamos las matrices necesarias para el cálculo de las betas
<br>![image](https://github.com/user-attachments/assets/4d54cb32-3879-4987-ab1c-9abc5957120d)

Seguimos con las Y’s pronosticadas y los residuales
<br>![image](https://github.com/user-attachments/assets/545b9e83-935f-44ea-8509-a81653dcd119) ![image](https://github.com/user-attachments/assets/ec6df31e-c57f-471f-a0ca-4dec93cdbcd2)

Realizamos los cálculos de las sumas de cuadrados, y los valores necesarios para calcular el valor crítico de t de student
<br>![image](https://github.com/user-attachments/assets/15217bf7-32ae-4b9e-840c-26059c9db899)
<br>![image](https://github.com/user-attachments/assets/8184aeae-b1e6-434c-8979-9ba604ea9d30)
<br>![image](https://github.com/user-attachments/assets/fdd51f8f-6b3c-4ac9-ac7c-933cd7929ee6)

Hacemos el cálculo para el vector particular donde TV, Radio y Periódicos son de 100, 50 y 70
<br>![image](https://github.com/user-attachments/assets/3b1dd58a-2839-491b-bdd4-56248336a813)

Obtenemos que las ventas con estos valores serían de 15.7121

Realizamos la validación de supuestos de regresión, calculando el sesgo con el método manual y con la librería scipy
<br>![image](https://github.com/user-attachments/assets/0622ed78-8026-4cbf-97b4-5c5a288ef31a)

La kurtosis de la misma forma
<br>![image](https://github.com/user-attachments/assets/630a852b-2d65-424f-822b-9b6f58622ffb)

Y el método Jarque-Bera
<br>![image](https://github.com/user-attachments/assets/6e342744-e11c-48d7-82bc-33e828115f39)

Los residuales no tienen distribución normal, rechazamos H0

Probamos la inexistencia de autocorrelación
<br>![image](https://github.com/user-attachments/assets/be9825a1-6248-4eb3-90cf-f33f7dafa57a)

Obtenemos el mismo resultado de la forma manual
<br>![image](https://github.com/user-attachments/assets/230c60a5-5517-4b64-977d-0dc7e7d64863)

DW es aproximado a 2, por lo que podemos descartar la existencia de autocorrelación entre los residuales

Realizamos la prueba de homocedasticidad
<br>![image](https://github.com/user-attachments/assets/8aaa5c8f-8b01-4446-aec2-edc3b5f64813)
<br>![image](https://github.com/user-attachments/assets/1b851fa2-620c-474e-8f73-425c1a319d66)

Al realizar la prueba alternativa obtenemos discrepancia de resultados por lo que se deberia probar mas a fondo
<br>![image](https://github.com/user-attachments/assets/f8890d09-8bc8-4ca7-8957-333ddc13cb8e)

Debido a que tenemos múltiples variables buscamos multicolinealidad
<br>![image](https://github.com/user-attachments/assets/a39e1070-267a-4df7-a984-6cca5d2c0f1b)

Determinamos que no existe multicolinealidad con el método VIF
