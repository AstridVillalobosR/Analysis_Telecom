# 📊 Análisis Exploratorio de Clientes — ConnectaTel

<p align="center">
  <img src="Representacion_Telecomunicaciones.png" width="600">
</p>

## 🎯 Objetivo

Analizar el comportamiento de los clientes de la empresa de telecomunicaciones latinoamericana **ConnectaTel**, con el propósito de:

- Identificar patrones de uso.
- Detectar comportamientos atípicos.
- Segmentar clientes según edad y nivel de uso.
- Analizar la cancelación de planes (churn).
- Identificar oportunidades para optimizar la oferta comercial y mejorar la experiencia del usuario.

---

## 📁 Datasets

Para el análisis se utilizaron tres fuentes de información:

| Dataset | Descripción |
|---|---|
| `plans` | Información de los planes: precio, minutos incluidos, GB incluidos y costos adicionales. |
| `users` | Información de los clientes: edad, ciudad, fecha de registro y plan contratado. |
| `usage` | Registro del uso realizado: llamadas, duración y mensajes. |

---

## 🔎 Metodología

### 📥 1. Carga y exploración de datos

Se importaron los datasets y se realizó una exploración inicial mediante:

- `head()`
- `info()`
- `shape()`

Esta revisión permitió identificar problemas iniciales relacionados con la calidad y estructura de los datos.

### 🧹 2. Calidad de los datos

Se analizaron:

- Valores nulos.
- Valores inválidos.
- Valores atípicos o *sentinels*.
- Tipos de datos.
- Consistencia de las variables.

Posteriormente, se realizaron los ajustes necesarios para garantizar la calidad de la información utilizada en el análisis.

### 📅 3. Fechas y valores inválidos

Se revisaron y estandarizaron las fechas, identificando registros imposibles y valores *sentinel*.

También se extrajo el año de las fechas para facilitar el análisis temporal.

### 🧩 4. Análisis de datos faltantes

Se analizó el comportamiento de los valores faltantes en las variables `duration` y `length`, con el objetivo de determinar si presentaban algún patrón asociado a otras variables del dataset.

### 📞 5. Agrupación del comportamiento de uso

Se generaron nuevas variables agregadas por usuario:

- Cantidad total de mensajes.
- Cantidad total de llamadas.
- Cantidad total de minutos de llamada.

Posteriormente, estas variables fueron integradas con la información de los clientes para obtener una visión consolidada del comportamiento de cada usuario.

### 📈 6. Distribuciones y valores atípicos

Se utilizaron diferentes visualizaciones para analizar:

- Distribución de usuarios por plan.
- Comportamiento de mensajes, llamadas y minutos.
- Diferencias entre los planes Básico y Premium.
- Valores atípicos mediante *boxplots*.

Se utilizó el **IQR (Rango Intercuartílico)** para identificar los valores extremos y determinar las acciones correspondientes.

### 👥 7. Segmentación de clientes

Los clientes fueron clasificados según dos criterios:

**Por edad**
- 🧑 Joven
- 🧑‍💼 Adulto
- 👴 Adulto Mayor

**Por nivel de uso**
- 🟢 Bajo
- 🟡 Medio
- 🔵 Alto

Estas segmentaciones permitieron analizar la composición de la base de clientes y encontrar patrones de comportamiento.

### 📉 8. Análisis de cancelación (Churn)

Finalmente, se analizó la tasa de cancelación de los clientes:

- Por tipo de plan.
- Por nivel de uso.
- Por grupo de edad.

Esto permitió identificar segmentos con mayor riesgo de cancelación y plantear posibles oportunidades de retención.

---

## 💡 Principales hallazgos

- 👥 La mayor concentración de clientes corresponde al grupo **Adulto**.
- 📱 El **nivel de uso medio** representa la mayor parte de los usuarios.
- 📊 El plan **Básico** concentra la mayor cantidad de clientes.
- 📉 Los usuarios de **alto uso presentan la mayor tasa de churn**, lo que representa una oportunidad para analizar estrategias de retención.
- 📞 Se identificaron valores extremos principalmente en la variable de **minutos de llamada**, asociados a un grupo reducido de usuarios con consumos considerablemente superiores al promedio.

---

## 🛠️ Herramientas utilizadas

<p align="center">

🐍 **Python** &nbsp;&nbsp; | &nbsp;&nbsp;
🐼 **Pandas** &nbsp;&nbsp; | &nbsp;&nbsp;
📊 **Matplotlib** &nbsp;&nbsp; | &nbsp;&nbsp;
📈 **Seaborn** &nbsp;&nbsp; | &nbsp;&nbsp;
📓 **Jupyter Notebook**

</p>

---

## 🚀 Resultado

El análisis permitió transformar los datos de clientes y uso en **insights accionables**, identificando patrones de comportamiento, segmentos relevantes y oportunidades relacionadas con la retención de clientes y la optimización de la oferta comercial.


