# 🐊 MACHETE DE EXPOSICIÓN ORAL (8 MINUTOS)
## TPI: CrocScale IA — AI-Sales Engine
**Materia:** Aproximación al Campo Laboral (IFTS Nº 24) | **Docente:** Prof. Gabriela Geronimo  
**Estudiante:** Nicolás Marcelo Galarza Vázquez  

---

### ⏱️ MAPA RÁPIDO DE TIEMPOS
* **Slide 1 [0:00 - 1:00]:** Presentación personal, IFTS 24 y de qué trata el proyecto.
* **Slide 2 [1:00 - 2:00]:** CrocScale IA, modelo B2B, clientes de Once y stack técnico.
* **Slide 3 [2:00 - 3:00]:** El problema: 70% ventas perdidas, chats ciegos y pagos manuales.
* **Slide 4 [3:00 - 4:15]:** AI-Sales Engine: OCR (10% seña), Lead Scoring (ML) y Churn.
* **Slide 5 [4:15 - 5:15]:** Los números de impacto: -90% tiempo, +25% ventas, 10x escala.
* **Slide 6 [5:15 - 6:15]:** Tu rol: AI Architect & Lead Data Engineer (ETL, n8n, 98% ahorro tokens).
* **Slide 7 [6:15 - 7:15]:** Competencias: Técnica (SQL/Redis), Analítica (EDA/ML), Soft (Storytelling).
* **Slide 8 [7:15 - 8:00]:** Conclusión, roadmap (Voice/MLibre) y cierre formal.

---

### 🟢 SLIDE 1 | CARÁTULA E INTRODUCCIÓN [0:00 - 1:00]
* **Idea clave:** Romper el hielo con seguridad, presentarte y titular el proyecto.
* **Qué decir:**
  - *"Buenas noches profesora y compañeros. Soy Nicolás Galarza Vázquez, estudiante de la Tecnicatura en Ciencia de Datos e Inteligencia Artificial del IFTS 24."*
  - *"Hoy presento mi Trabajo Práctico Integrador de Aproximación al Campo Laboral, basado en mi propia empresa: **CrocScale IA**."*
  - *"El proyecto se titula **AI-Sales Engine**: una arquitectura que une la Ciencia de Datos con la IA multimodal para resolver cuellos de botella en la venta por WhatsApp e Instagram, validando transferencias por OCR y prediciendo el comportamiento de compra con Machine Learning."*
* **👉 Frase de transición:** *"Para entender el porqué de este proyecto, paso a contarles qué es y cómo opera la organización."*

---

### 🟢 SLIDE 2 | ORGANIZACIÓN: CROCSCALE IA [1:00 - 2:00]
* **Idea clave:** No es un proyecto ficticio; es una empresa activa con clientes reales y stack sólido.
* **Qué decir:**
  - *"CrocScale IA es una startup y agencia de automatizaciones B2B orientada al comercio mayorista y minorista."*
  - *"Nuestra propuesta de valor es el **despliegue express en 24 a 48 horas**, sin la burocracia pesada de Meta, garantizando **respuestas en 30 segundos a 1 minuto**."*
  - *"Trabajamos con clientes reales de la zona de Once y Gran Buenos Aires: **ADAR Insumos** (ferretería/bazar), **Bross Underwear** (indumentaria masculina), **Nacha Home** y **NNN Store**."*
  - *"Tecnológicamente nos auto-hospedamos con **Easypanel sobre VPS de Hostinger**, usamos **Redis** como memoria temporal para que no choquen los mensajes en WhatsApp, **Supabase PostgreSQL** para el almacenamiento relacional de pedidos, y orquestamos con **n8n** y modelos LLM de última generación."*
* **👉 Frase de transición:** *"Al relevar la operatoria de estos clientes, nos encontramos con un problema estructural."*

---

### 🟢 SLIDE 3 | EL PROBLEMA: CUELOS DE BOTELLA [2:00 - 3:00]
* **Idea clave:** El 70% de las ventas online mueren por lentitud y los datos de chat se desperdician.
* **Qué decir:**
  - *"El primer dolor es la **latencia**: el **70% de las ventas online se pierden** por falta de respuesta inmediata. Si un cliente escribe a las 11 de la noche y nadie responde, le compra al de al lado."*
  - *"El segundo es la **ceguera de datos**: los chats se guardaban como texto plano en WhatsApp sin generar inteligencia de negocio. No se sabía quién tenía intención real de compra ni quién estaba por abandonar la marca."*
  - *"Y el cuello de botella más grave era la **validación manual de comprobantes**: cuando un cliente manda una captura de transferencia bancaria, el vendedor humano tarda horas en entrar al home banking, cotejar el saldo y calcular si cubre el **10% de seña obligatoria**. Eso demoraba el despacho y abría la puerta a fraudes o comprobantes truchos."*
* **👉 Frase de transición:** *"Para solucionar estos tres dolores de raíz, desarrollé la propuesta técnica del TPI."*

---

### 🟢 SLIDE 4 | PROYECTO: AI-SALES ENGINE [3:00 - 4:15]
* **Idea clave:** 3 pilares técnicos: OCR Multimodal, Lead Scoring supervisado y Alertas de Churn.
* **Qué decir:**
  - *"El **AI-Sales Engine** se acopla directamente a nuestro CRM y opera sobre tres pilares:"*
  - *"1. **Agente Multimodal OCR**: toma la imagen o PDF del comprobante en WhatsApp, extrae monto, banco y código de operación, y **valida algorítmicamente que cumpla la seña del 10%**. Si está OK, guarda en Supabase y avisa a Telegram para preparar el paquete."*
  - *"2. **Predictive Lead Scoring**: un modelo de Machine Learning supervisado (XGBoost / Scikit-Learn) entrenado sobre nuestra tabla de historiales (`n8n_chat_histories`). Analiza frecuencia, recencia y palabras de intención, asignando un score de 0 a 100. Los leads con puntaje mayor a 80 se derivan automáticamente al vendedor humano para cerrar la venta."*
  - *"3. **Analítica de Churn y Cross-Selling**: panel predictivo que detecta cuándo un cliente recurrente deja de comprar para disparar promociones automáticas y recomendar productos complementarios."*
* **👉 Frase de transición:** *"¿Qué impacto tuvo todo esto en la práctica? Veamos los números."*

---

### 🟢 SLIDE 5 | BENEFICIOS E IMPACTO [4:15 - 5:15]
* **Idea clave:** 3 métricas gigantes: -90%, +25% y 10x.
* **Qué decir:**
  - *"Los resultados en producción fueron contundentes:"*
  - *"**-90% en tiempo de validación de pagos**: pasamos de esperas de hasta 4 horas a una verificación automática en **menos de 10 segundos**, eliminando errores de tipeo y transferencias duplicadas."*
  - *"**+25% en la tasa de conversión comercial**: al priorizar los prospectos calientes por Lead Scoring, el equipo de ventas deja de perder tiempo en curiosos y atiende de inmediato a los que están listos para comprar."*
  - *"**10x en escalabilidad operativa**: una pyme con este motor puede procesar más de **20.000 conversaciones mensuales** sin necesidad de contratar más empleados de atención básica ni disparar sus costos fijos."*
* **👉 Frase de transición:** *"Detrás de estos resultados hubo un trabajo técnico integral que paso a detallar."*

---

### 🟢 SLIDE 6 | ROL DEL ESTUDIANTE [5:15 - 6:15]
* **Idea clave:** Liderazgo técnico integral (AI Automation Architect & Lead Data Engineer).
* **Qué decir:**
  - *"Mi rol en este proyecto fue el de **AI Automation Architect & Lead Data Engineer**, cubriendo de punta a punta la arquitectura:"*
  - *"En **Arquitectura de Datos**: diseñé la tubería conectando Meta Cloud API con Redis (para evitar que se pisen los mensajes en chats simultáneos) y modelé las tablas relacionales en Supabase PostgreSQL."*
  - *"En **Ciencia de Datos y ML**: realicé la limpieza y feature engineering de miles de líneas de chat no estructuradas, entrenando los algoritmos y desplegando microservicios en Python con FastAPI."*
  - *"En **Automatización y Prompt Engineering**: orquesté los flujos en n8n e implementé una optimización clave: inyectar el contexto en el `systemMessage`, lo que permitió **reducir un 98% el consumo de tokens** frente a arquitecturas comunes, volviéndolo económicamente viable."*
* **👉 Frase de transición:** *"Todo este desarrollo puso en juego las competencias troncales de la carrera."*

---

### 🟢 SLIDE 7 | COMPETENCIAS PUESTAS EN PRÁCTICA [6:15 - 7:15]
* **Idea clave:** Articulación de la triada formativa del IFTS 24 (Técnica, Analítica y Liderazgo/Soft).
* **Qué decir:**
  - *"Este proyecto me permitió articular tres grandes áreas formativas:"*
  - *"**Competencia Técnica**: integración de bases relacionales SQL, memoria en Redis, contenedores Docker y consumo de APIs sin pérdida de sesión."*
  - *"**Competencia Analítica**: pensamiento estadístico, EDA sobre texto no estructurado, y métricas de Machine Learning como Precision y Matrices de Confusión para asegurar que el OCR no apruebe pagos erróneos."*
  - *"**Competencia Transversal (Soft Skill)**: **Liderazgo Adaptativo, Data Storytelling y Frame Control**. De nada sirve tener un modelo con 95% de precisión si los vendedores no confían en el score o si el dueño del negocio no entiende el beneficio. Saber traducir métricas matemáticas a dinero y eficiencia comercial fue la clave para que la solución sea adoptada."*
* **👉 Frase de transición:** *"Para finalizar, comparto las conclusiones y el futuro del sistema."*

---

### 🟢 SLIDE 8 | CONCLUSIONES Y CIERRE [7:15 - 8:00]
* **Idea clave:** La IA transforma a la pyme argentina; agradecimiento y paso a preguntas.
* **Qué decir:**
  - *"Como conclusión: este trabajo demuestra que la Ciencia de Datos y la IA tienen una aplicación inmediata y tangible en la economía real de nuestras pymes."*
  - *"Pude volcar de manera práctica los conocimientos de la carrera en un producto en producción que hoy está operando con éxito."*
  - *"Hacia adelante, estamos trabajando en incorporar **Voice Bots con síntesis de voz ultra-natural**, integración directa con el catálogo de **MercadoLibre** y monitoreo continuo de **data drift**."*
  - *"Les agradezco mucho por su atención. Quedo a disposición de la profesora para preguntas o comentarios. ¡Muchas gracias!"*

---

### 🛡️ SALVAVIDAS: RESPUESTAS RÁPIDAS A PREGUNTAS TÍPICAS DE LA DOCENTE

1. **¿Por qué usaste Redis además de PostgreSQL?**  
   *Respuesta:* *"Porque WhatsApp recibe ráfagas de mensajes simultáneos del mismo usuario. Si le pegamos a PostgreSQL en cada mensaje colisiona la sesión; Redis actúa como búfer en memoria de ultra-alta velocidad que retiene los mensajes por unos segundos y entrega el bloque consolidado al LLM."*
2. **¿Cómo garantizás que el OCR no apruebe comprobantes falsos?**  
   *Respuesta:* *"Combinamos extracción de entidades con control de hashes para evitar comprobantes duplicados, y exigimos que coincidan monto, banco y código de transacción, validando estrictamente el 10% de seña antes de confirmar el pedido."*
3. **¿Por qué decís que ahorrás 98% de tokens?**  
   *Respuesta:* *"Muchos desarrolladores cometen el error de reinyectar el catálogo o el contexto en el mensaje `human` en cada turno de chat, acumulando miles de tokens repetidos. En CrocScale inyectamos las reglas en el `systemMessage` y recortamos la ventana de memoria a 8 turnos, procesando solo lo necesario."*
