# 📊 Análisis de Cancelaciones de Clientes (Churn Analysis)

Este proyecto tiene como objetivo analizar el comportamiento de cancelación de clientes de una empresa de telecomunicaciones, identificando patrones, tendencias y factores que influyen en la pérdida de clientes (churn). A través de diversas visualizaciones y métricas, se busca brindar información útil para diseñar estrategias de fidelización.

## 🔍 Objetivos del análisis

- Identificar características comunes entre los clientes que cancelan.
- Determinar qué tipo de contratos, servicios o métodos de pago están más asociados al churn.
- Evaluar la relación entre la antigüedad del cliente y su propensión a cancelar.
- Proponer posibles estrategias de retención.

## 🧾 Dataset

El dataset contiene información de clientes y suscripciones, con columnas como:

- `customerID`: ID único del cliente
- `Churn`: si canceló o no
- `customer_gender`, `customer_SeniorCitizen`, `customer_Partner`, `customer_Dependents`: datos demográficos
- `customer_tenure`: meses desde la contratación
- `phone_PhoneService`, `phone_MultipleLines`
- `internet_InternetService`, `internet_OnlineBackup`, `internet_DeviceProtection`, `internet_TechSupport`, `internet_StreamingTV`, `internet_StreamingMovies`
- `account_Contract`, `account_PaperlessBilling`, `account_PaymentMethod`
- `account_Charges.Monthly`, `account_Charges.Total`

> ⚠️ Antes de comenzar el análisis, se realizó una limpieza y expansión de columnas para facilitar la visualización y el manejo de datos.

## 📁 Estructura del proyecto

├── images/ # Carpeta donde se guardan los gráficos generados

├── TelecomX_LATAM,ipynb/ # Notebook con el análisis exploratorio y visualizaciones

├── TelecomX_DATA.json/ # Dataset original y limpio 

├── README.md # Este archivo


## 🛠️ Librerías utilizadas

- pandas
- numpy
- matplotlib
- seaborn
- plotly (opcional)
- os (para manejo de archivos)

## 💾 Cómo ejecutar

1. Cloná el repositorio:

```bash
git clone https://github.com/marsavil/telecom_x_challenge.git
```

2. Asegurate de tener un entorno virtual con las dependencias:

```bash
pip install -r requirements.txt
```

3. Ejecutá el notebook

## 📈 Visualizaciones

Los gráficos se generan automáticamente y se guardan en la carpeta /images. Para exportarlos, se utiliza una función personalizada:
```python
def exportar_grafico(grafico, nombre):
    os.makedirs('images', exist_ok=True)
    imagen = grafico()
    imagen.savefig(os.path.join('images', f'grafico_{nombre}.png'), bbox_inches='tight')
    imagen.close()
```
## ✅ Principales hallazgos
La mayoría de las cancelaciones se dan en los primeros meses de servicio.

Los clientes con contratos mes a mes tienen mayor tasa de churn.

Usar factura electrónica se asocia con cancelaciones más frecuentes.

Los clientes que contratan más servicios adicionales tienden a permanecer más tiempo.

Los métodos de pago automáticos están relacionados con menor tasa de cancelación.

## 📌 Próximos pasos
Generar modelos predictivos de churn.

Incorporar variables externas (satisfacción, encuestas, etc.).

Automatizar alertas para clientes en riesgo de cancelar.

## 🤝 Contribuciones
¡Las contribuciones son bienvenidas! Podés abrir issues o hacer pull requests con sugerencias de mejoras o nuevas visualizaciones.

## 📜 Licencia
Este proyecto está bajo la licencia MIT. Ver LICENSE para más detalles.




