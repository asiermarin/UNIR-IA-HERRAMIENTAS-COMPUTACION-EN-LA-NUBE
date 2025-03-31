# Tema 1 - Introducción, contexto y característicvas de proveedores y servicios de IA de la nube

---

## 1.1 Introducción y objetivos

La **IA** y la **computación en la nube** son dos mega-tendencias tecnológicas clave en la actualidad. Están profundamente conectadas:  
- La nube proporciona la infraestructura necesaria para ejecutar modelos de IA.
- La IA demanda mucha potencia de cómputo que muchas organizaciones no pueden costear de forma local (*on premise*).

**Ventajas de la nube:**
- Escalabilidad, pago por uso y acceso rápido a servicios avanzados.
- Ahorro en infraestructura y personal.

**Objetivos del tema:**
- Comprender el mercado de IA en la nube y sus principales proveedores.
- Reconocer cuándo es mejor usar la nube frente a soluciones locales.
- Diseñar estrategias para reducir costes en proyectos de IA.
- Asesorar sobre el uso de servicios de IA en la nube.

---

## 1.2 El mercado de servicios de inteligencia artificial en la nube

### ✅ **Características**
- **Flexible:** pago por uso, escalado dinámico.
- **Ágil:** provisión de capacidades en minutos.
- **Escalable:** capacidad casi ilimitada para ajustarse a la demanda.

### 🎁 **Beneficios**
- Reducción de plazos para adopción de IA.
- Costes controlados y eficiencia (pagas por lo que usas).
- Reutilización de modelos preentrenados.
- Menos necesidad de expertos (gracias al AutoML).
- Acceso a software y plataformas actualizadas sin instalar nada.

### 📈 **Grado de adopción**
- En 2023, el 70 % de entornos cloud ya incluían IA.
- Microsoft (Azure) lidera con 54 % de adopción de IA generativa.
- Muchas empresas siguen en fase de experimentación.
- El 69 % usa la nube para hospedar modelos propios en lugar de servicios IA nativos.

### 🔧 **Ejemplos de herramientas utilizadas**
- **Hugging Face Transformers**: modelos de lenguaje, visión, audio, etc.
- **LangChain**: integración de LLMs en apps.
- **TensorFlow Hub**: repositorio de modelos listos para usar.
- **BERT**: modelo de clasificación de texto muy usado.

### ⚠️ **Problemas comunes**
- Falta de gobernanza.
- Riesgos por decisiones erróneas de IA.
- Ineficiencias por contratación descoordinada.
- Problemas de cumplimiento legal y ciberseguridad.

---

## 1.3 Porfolio de capacidades de IA en la nube

### 🤖 **AutoML**
- Permite crear modelos sin saber programar.
- Automatiza:
  - Preparación de datos (limpieza, enriquecimiento).
  - Ingeniería de variables (creación automática de nuevas).
  - Generación y evaluación de modelos.
  - Puesta en producción con APIs y workflows automáticos.
  - Mantenimiento y actualización automática de modelos.
  - Evaluación del impacto de la calidad del dato.

### 🧪 **Servicios para expertos**
- Uso de notebooks Jupyter para crear modelos con código (Python).
- Incluye: entrenamiento, experimentación, monitorización, etc.
- Soporta bibliotecas open-source como PyTorch o TensorFlow.

### 🗣️ **Procesamiento de lenguaje natural**
- **Conversión voz-texto**
- **Tokenización**
- **Análisis gramatical**
- **Traducción automática**
- **Análisis de sentimientos**
- **Resumen de documentos**

### 👁️ **Visión artificial**
- Identificación de objetos, acciones, anomalías.
- OCR y transcripción de vídeo.
- Seguimiento de objetos.
- Generación de imágenes por IA a partir de texto.

### 🧩 **Otros servicios**
- **Detección de anomalías:** en sistemas, fraudes, etc.
- **Sistemas de recomendación:** contenido personalizado basado en comportamiento del usuario.

---

## 1.4 Proveedores principales de IA en la nube

### 🌍 **Alibaba Cloud**
- Especializada en personalización y traducción multilingüe.
- Preentrenados adaptables a cualquier sector (salud, banca…).

### 📦 **Amazon Web Services (AWS)**
- SageMaker: automatiza todo el ciclo de vida de modelos.
- Fuerte en productización y operativización de modelos.

### 🔍 **Google Cloud Platform**
- Vertex AI: integra visión, lenguaje, AutoML y herramientas de bajo nivel.
- Pionera en IA responsable.

### 🪟 **Microsoft Azure**
- Servicios de lenguaje, visión y AutoML.
- Precios escalables, ideal para empezar con poca inversión.

### 📈 **H20.ai**
- Solo IA (no computación en la nube general).
- Experta en AutoML para todo tipo de datos y entornos híbridos.

### 🧠 **IBM**
- Chatbots, visión, AutoML.
- Foco en calidad del dato, sesgos y explicabilidad.

### 🔒 **Oracle**
- Servicios de voz, visión y AutoML.
- Despliegue flexible: nube, on-premise o híbrido.

---

### 🧠 Diferencias clave entre proveedores grandes

- **Servicios gestionados**: el proveedor se encarga del mantenimiento.
- **Proceso extremo a extremo**: desde el entrenamiento al despliegue.
- **Escalabilidad y flexibilidad**: adaptan recursos automáticamente.
- **Bibliotecas ricas** de algoritmos.
- **Soporte para código propio** con herramientas open-source.
- **AutoML potente** para todas las etapas.
- **Monitorización avanzada** de modelos desplegados.
- **Integración total** con el resto del ecosistema cloud.

---

## 1.5 Nube vs On-Premise: ventajas y desventajas

### ☁️ **Ventajas de la nube**
- Perfecta para pruebas y experimentación.
- Ahorro inicial y rapidez de implementación.
- Ideal si el presupuesto es limitado.

### 🖥️ **Ventajas on-premise**
- Menor coste a largo plazo si se usa intensamente.
- Mayor personalización.
- Control absoluto sobre privacidad y datos sensibles.

### 🌀 **Ventajas del enfoque híbrido**
- Para cumplir regulaciones de privacidad geográfica.
- Combina lo mejor de ambos mundos según la fase o el tipo de datos.

---

## 1.6 Seguridad y privacidad

### 🔐 **Seguridad**
Modelo de responsabilidad compartida:
- El proveedor debe:
  - Cumplir estándares (ISO, etc.)
  - Hacer auditorías, cifrado, backup, respuesta ante incidentes.
- El cliente debe:
  - Controlar accesos y privilegios.
  - Autenticar correctamente.
  - Supervisar configuración y actividad.

### 🛡️ **Privacidad**
- Falta de normativa global homogénea (aunque avanza rápidamente).
- ISO 27018 protege datos personales.
- EU AI Act (Ley de la IA europea):
  - Clasifica aplicaciones según nivel de riesgo.
  - Impone requisitos: transparencia, gestión de riesgos, gobernanza de datos, explicabilidad, etc.

---

## 1.7 Cuaderno de ejercicios – Ejemplos destacados

### 📌 Ejemplo 1: Artículo de Zangana y Zeebaree (2024)
Recomiendan:
- IA explicable.
- Métricas estandarizadas.
- Seguridad avanzada.
- Escalabilidad y ética.
- Colaboración intersectorial.

### 📌 Ejemplo 2: Comparación entre proveedores cloud
3 aspectos clave si necesitas mucha computación puntualmente:
1. ¿Tiene modelos preentrenados?
2. ¿Ofrece GPUs/TPUs?
3. ¿Permite pagar por uso?

### 📌 Ejemplo 3: Ahorro de costes en IA en la nube
- Costes basados en uso real (no inversión inicial).
- Menor necesidad de personal técnico (gracias a AutoML).

### 📌 Ejemplo 4: Requisitos de seguridad exigibles al proveedor
- Estándares, auditorías, cifrado, backups, SLAs, cumplimiento legal.

### 📌 Ejemplo 5: Consejo de Accenture
> No empieces por la IA. Empieza por el problema de negocio.  
> Evita preguntas como “¿Cómo usamos IA ya?” y plantea “¿Qué problema queremos resolver?”.

---

## 1.8 Referencias y recursos clave

- **Azure AutoML**: [Documentación oficial](https://learn.microsoft.com/en-us/azure/machine-learning/concept-automated-ml)
- **Hugging Face, LangChain, BERT, TensorFlow Hub**
- **Informe Gartner (2023)**: evaluación de proveedores.
- **Informe Wiz (2024)**: adopción actual de IA en la nube.
- **EU AI Act (2024)**: marco legal europeo.

---

## ✅ Conclusión del Tema 1

La IA en la nube ha evolucionado rápidamente y se ha convertido en una herramienta fundamental para organizaciones de todos los tamaños. Comprender su funcionamiento, ventajas, limitaciones y el ecosistema de proveedores es esencial para tomar decisiones estratégicas sobre cómo implementar soluciones de IA de forma segura, eficiente y rentable.

---