# Tema 3 - Creación de modelos de IA en Microsoft Azure con ML Workspaces

---

## Introducción y Objetivos

Este tema profundiza en las funcionalidades de **Azure Machine Learning**, la plataforma de Microsoft para crear y gestionar modelos de IA. Se abordan todas las fases del ciclo de vida de un modelo: ingestón y exploración de datos, ingeniería de variables, entrenamiento, ajuste de hiperparámetros, despliegue, monitorización y operación.

Los objetivos incluyen:
- Usar eficazmente el entorno de Azure para crear modelos ML.
- Aprovechar la automatización para agilizar procesos.
- Reutilizar código mediante el SDK de Azure ML para Python.

---

## Entorno de Trabajo (Workspace)

Se puede crear mediante:
- Azure CLI (`az ml workspace create`)
- PowerShell
- REST API
- Portal Web

Al crear el entorno, también se generan:
- Cuenta de almacenamiento
- Azure Key Vault (credenciales)
- Application Insights (monitorización)
- Azure Container Registry (imágenes Docker)

**Machine Learning Studio** proporciona:
- **Author**: Jupyter, AutoML, Designer
- **Assets**: Datasets, experimentos, pipelines, modelos
- **Manage**: Computación, datos, etiquetado, integraciones

---

## Ingestión y Exploración de Datos, Ingeniería de Variables y Pipelines

### Ingestión de Datos
Se gestionan con `dataset` y `datastore`.
- Dataset: tabular o binario
- Datastore: Blobs, Azure Files, SQL, Datalakes, Databricks

**Herramientas**:
- Manual: Azure Storage Explorer, CLI, AzCopy, Azure Portal, Azure Data Studio
- Automática: Azure Data Factory, Azure Synapse Spark

### Exploración de Datos
Usando Jupyter Notebooks:
```python
from azureml.core import Datastore, Dataset
datastore = Datastore.get(ws, 'nombre_datastore')
dataset = Dataset.Tabular.from_delimited_files([(datastore, 'fichero.csv')])
df = dataset.to_pandas_dataframe()
```

### Ingeniería de Variables
Incluye etiquetado de imágenes/textos con Azure ML Labeling Service. Soporta clasificación simple, múltiple, segmentación y etiquetado de textos.

### Pipelines
Permiten dividir procesos en bloques reutilizables. Ejemplo:
```python
step = PythonScriptStep(name='train', script_name='script.py', ...)
pipeline = Pipeline(ws, steps=[step])
pipeline.validate()
experiment.submit(pipeline)
```

---

## Entrenamiento de Modelos y Redes Neuronales

### Modelos Clásicos
Usa Jupyter Notebooks. Registro de dataset, ejecuciones, métricas y modelos. Ejemplo con LGBM:
```python
run.log("accuracy", accuracy_score(y_test, y_pred))
run.register_model(model_name='lgbm', model_path='outputs/lgbm.pkl')
```

### Deep Learning con GPU
Se usan VMs con GPU (ej. STANDARD_NC6). Se configura como `ComputeTarget` para acelerar entrenamiento:
```python
AmlCompute.provisioning_configuration(vm_size='STANDARD_NC6')
```

---

## Ajuste de Hiperparámetros con HyperDrive

### Estrategias:
- Grid Search
- Random Search
- Bayesian Optimization

### Early Stopping Policies:
- MedianStoppingPolicy
- TruncationSelectionPolicy
- BanditPolicy

Ejemplo:
```python
config = HyperDriveConfig(..., max_total_runs=32, max_concurrent_runs=4)
experiment.submit(config)
```

---

## AutoML (Machine Learning Automatizado)

AutoML permite entrenar modelos sin escribir código complejo. Se puede usar por GUI o Python.

Ejemplo:
```python
config = AutoMLConfig(task='classification', training_data=..., label_column_name=..., ...)
experiment.submit(config)
```

---

## Deep Learning Distribuido con Horovod

Permite paralelismo de datos con varios nodos:
```python
import horovod.keras as hvd
hvd.init()
opt = hvd.DistributedOptimizer(Adadelta(...))
```

Configuración MPI:
```python
MpiConfiguration(process_count_per_node=1, node_count=2)
```

---

## Despliegue y Operación de Modelos

### Autodespliegue:
```python
model = run.register_model(...)
service = Model.deploy(ws, 'servicio1', [model])
```

### Operaciones post-despliegue:
- **Profile**: estima hardware ideal
- **Application Insights**: monitorización en tiempo real
- **Data Drift Detector**: detecta degradación del modelo por cambios en los datos

---

## Cuaderno de Ejercicios (Resumen)
- Crear dataset desde CSV
- Crear infraestructura con `AmlCompute`
- Configurar y lanzar AutoML con `AutoMLConfig`
- Ejecutar entrenamiento en R con Dockerfile
- Hacer random search con `HyperDrive` + `BanditPolicy`

---

## Recursos y Referencias
- Microsoft Learn
- Medium
- Documentación oficial de Azure ML
- Blog Educator Developer

---

Este resumen contiene todos los apartados, ejemplos y explicaciones prácticas necesarias para comprender el Tema 3. Si deseas convertirlo en una guía paso a paso o ejemplos ejecutables, puedo ayudarte con eso también.