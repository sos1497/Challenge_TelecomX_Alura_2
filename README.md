# 📊 Challenge TelecomX - Predicción de Bajas (Churn)

## 🎯 Objetivo del Proyecto

Identificar por qué el **25.7%** de los clientes cancelan sus servicios y crear un modelo que nos avise quiénes están en riesgo para poder ofrecerles una solución a tiempo.

---

## 🛠️ Tecnologías Usadas

* **Lenguaje:** Python 🐍
* **Librerías:** Pandas, NumPy, Matplotlib, Seaborn y Scikit-Learn.
* **Entorno:** Google Colab.

---

## 🧹 Primera Parte: Limpiando los Datos (Data Wrangling)

El archivo original estaba bastante desordenado, así que hice lo siguiente:

* **Desarmar JSON:** Convertí datos complejos en una tabla simple.
* **Limpieza:** Borré errores y llené espacios vacíos.
* **Nuevas Variables:** Creé columnas como `Cargos_Diarios` y `Evasion_Binario` para entender mejor la plata que entra y sale.

---

## 📈 Hallazgos Clave

* **El "Mes a Mes" es un peligro:** Los clientes sin contrato fijo se van muchísimo más.
* **El precio duele:** Los que se van suelen pagar entre **$70 y $100** dólares al mes (más caro que el promedio).
* **Los primeros 12 meses son clave:** Si un cliente pasa del primer año, es muy probable que se quede para siempre.
* **Problemas con la Fibra:** Los clientes con Fibra Óptica se quejan o se van más.

---

## 🤖 Segunda Parte: El Modelo Predictivo

Para no solo mirar el pasado, sino predecir el futuro, entrené dos modelos:

1. **Regresión Logística:** (Mi elección final). Fue el mejor detectando a los que se quieren ir (**68% de acierto** en detectar desertores).
2. **Random Forest:** Muy bueno, pero un poco más "distraído" con los clientes que se van.

> **¿Por qué elegí la Regresión Logística?** Porque en este negocio es mejor marcar a alguien que "quizás" se va y darle un descuento, que no darse cuenta y perder al cliente para siempre.

---

## 💡 ¿Qué debería hacer la empresa? (Conclusiones)

1. **Cuidar a los nuevos:** Hacer llamadas de cortesía o dar regalos durante los primeros **12 meses**.
2. **Revisar la Fibra Óptica:** Ver si el precio es muy alto o si el internet está fallando, porque ahí estamos perdiendo gente valiosa.
3. **Contratos Largos:** Darle beneficios a la gente que firme por 1 o 2 años, ya que son los clientes más fieles.
