# Challenge Telecom X

La evasión de clientes es uno de los principales desafíos para las empresas que operan bajo modelos de suscripción, como las compañías de telecomunicaciones. Cada cliente que cancela su servicio representa una pérdida directa de ingresos y aumenta los costos asociados a la adquisición de nuevos clientes.

En este proyecto se realiza un análisis de datos sobre los clientes de Telecom X con el objetivo de identificar patrones asociados con la cancelación del servicio. A través de técnicas de análisis exploratorio de datos se busca comprender qué factores pueden estar influyendo en el churn y generar insights que ayuden a mejorar las estrategias de retención.

## Objetivo del proyecto

- El objetivo principal es analizar los datos de clientes de Telecom X para:
- Identificar variables asociadas con la cancelación del servicio.
- Detectar patrones en variables categóricas y numéricas.
-Generar insights que ayuden a mejorar la retención de clientes.

### El dataset contiene información sobre clientes de Telecom X, incluyendo:
- **customerID**: número de identificación único de cada cliente
- **Churn**: si el cliente dejó o no la empresa
- **gender**: género (masculino y femenino)
- **SeniorCitizen**: información sobre si un cliente tiene o no una edad igual o mayor a 65 años
- **Partner**: si el cliente tiene o no una pareja
- **Dependents**: si el cliente tiene o no dependientes
- **tenure**: meses de contrato del cliente
- **PhoneService**: suscripción al servicio telefónico
- **MultipleLines**: suscripción a más de una línea telefónica
- **InternetService**: suscripción a un proveedor de internet
- **OnlineSecurity**: suscripción adicional de seguridad en línea
- **OnlineBackup**: suscripción adicional de respaldo en línea
- **DeviceProtection**: suscripción adicional de protección del dispositivo
- **TechSupport**: suscripción adicional de soporte técnico, menor tiempo de espera
- **StreamingTV**: suscripción de televisión por cable
- **StreamingMovies**: suscripción de streaming de películas
- **Contract**: tipo de contrato
- **PaperlessBilling**: si el cliente prefiere recibir la factura en línea
- **PaymentMethod**: forma de pago
- **Charges.Monthly**: total de todos los servicios del cliente por mes
-**Charges.Total**: total gastado por el cliente
- **Cuentas_diarias**: total gastado por dia por el cliente


## Preparación de datos

Antes de realizar el análisis se llevó a cabo un proceso de ETL (Extracción, Transformación y Carga).
### Extracción de datos
Los datos fueron cargados desde una API utilizando Pandas.
### Normalización de datos
El dataset contenía estructuras JSON anidadas (customer, phone, internet, account).
Estas estructuras fueron normalizadas utilizando pd.json_normalize() para convertirlas en columnas independientes.
### Limpieza de datos
Durante esta etapa se realizaron las siguientes tareas:
- Identiicación de valores nulos
- Verificación de registros duplicados
- Corrección de tipos de datos
- Estandarización de variables categóricas
- Conversión de variables binarias (yes/no) a valores numéricos (1/0)
- Creación de nuevas variables
- Se creó una nueva variable llamada Cuentas_Diarias, calculada a partir de los cargos mensuales, para facilitar algunos análisis adicionales.


## Tecnologías utilizadas
Las herramientas utilizadas en este proyecto son:
Python
Pandas - Manipulación y transformación de datos
Matplotlib - Visualización de datos
Google Colab - Desarrollo del análisis

## Resultados principales
Del análisis realizado se identificaron algunos patrones relevantes:

- Aproximadamente 26% de los clientes cancelan el servicio.
- Los contratos mensuales presentan mayor tasa de churn.
- Los clientes con menor antigüedad tienen mayor probabilidad de cancelar.
- El método de pago Electronic Check presenta la mayor tasa de evasión.
- Estos resultados sugieren que la duración del contrato y el tiempo de permanencia son factores importantes en la retención de clientes.

## Recomendaciones
Con base en los insights obtenidos, se proponen las siguientes estrategias:

**Incentivar contratos de mayor duración** - Ofrecer descuentos o beneficios para clientes que opten por contratos de 1 o 2 años.

**Mejorar la experiencia de clientes nuevos** - Implementar estrategias de onboarding y fidelización durante los primeros meses del cliente.

**Promover pagos automáticos** - Incentivar el uso de transferencias automáticas o tarjetas de crédito para reducir la probabilidad de bajas.

**Implementar modelos predictivos** - Utilizar estos datos para desarrollar modelos de predicción de bajas que permitan identificar clientes en riesgo y aplicar acciones preventivas.

