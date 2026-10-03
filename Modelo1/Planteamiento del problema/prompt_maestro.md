Eres un ingeniero de sistemas senior, analista de requisitos, arquitecto de soluciones de inteligencia artificial local y especialista en gestión de riesgos de IA con NIST AI Risk Management Framework (NIST AI RMF).

Redacta un documento académico formal, de nivel anteproyecto de ingeniería de sistemas, para el proyecto integrador del “Diplomado en Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab”.

El documento debe estar escrito en español profesional, claro, técnico y objetivo. Debe servir como punto de partida para el Módulo 1: Fundamentos, soberanía tecnológica y gobernanza de IA.

NO generes un documento de tesis completo. Entrega únicamente los siguientes apartados:

1. Planteamiento del problema.
2. Matriz preliminar de riesgos NIST AI RMF, mapeada por categorías.
3. Usuarios y partes interesadas.
4. Alcance.
5. Requisitos.
6. Criterios de éxito.
7. Tecnología e infraestructura requerida.

## Contexto del proyecto

El proyecto consiste en analizar, diseñar y proponer una solución inicial para apoyar la automatización de los procesos operativos y administrativos de una cafetería.

Actualmente, la cafetería realiza gran parte de sus actividades manualmente, registrando información en cuadernos físicos. De manera preliminar, se considera que esos registros pueden incluir información relacionada con:

- Ventas diarias.
- Pedidos.
- Productos disponibles.
- Inventario de insumos.
- Compras a proveedores.
- Gastos.
- Ingresos.
- Control básico de caja.
- Registro de clientes, si existe.
- Información de empleados o turnos, si existe.
- Reportes y consultas administrativas.

Sin embargo, esta información todavía NO ha sido confirmada. Está pendiente realizar una entrevista con la administradora de la cafetería para conocer el funcionamiento real del negocio, los procesos actuales, los problemas prioritarios, la información registrada, los usuarios, los recursos tecnológicos existentes y las restricciones operativas.

Por lo tanto, debes escribir con prudencia. No afirmes que todos los procesos anteriores existen. Usa expresiones como:

- “De manera preliminar…”
- “Se presume que…”
- “Podría incluir…”
- “Debe validarse mediante entrevista…”
- “[Pendiente de validación con la administradora]”.
- “La decisión definitiva dependerá del levantamiento de información”.

## Enfoque tecnológico obligatorio

La solución debe diseñarse bajo un enfoque local-first y no debe depender de nube ni de arquitectura híbrida.

Esto significa que:

- La información operativa de la cafetería debe permanecer en equipos o infraestructura local controlada por el negocio.
- No se debe proponer envío de información a APIs externas, servicios de IA en la nube ni almacenamiento externo como requisito de funcionamiento.
- El sistema debe poder operar localmente, idealmente incluso si no hay conexión permanente a Internet.
- La conexión a Internet solo podría utilizarse de forma excepcional para instalación inicial, descarga de actualizaciones, paquetes o modelos, pero no como requisito del funcionamiento cotidiano.
- La solución debe priorizar privacidad, control de datos, facilidad de uso y bajo costo operativo.
- Los usuarios pueden tener conocimientos tecnológicos limitados, por lo cual la interfaz debe ser sencilla, con lenguaje claro y procesos guiados.
- Debe existir supervisión humana para operaciones relevantes, especialmente cambios en registros, inventario, caja, precios, compras o reportes.

## Uso de inteligencia artificial local

La propuesta puede incluir un modelo de lenguaje local pequeño o mediano, ejecutado mediante herramientas como Ollama, GPT4All, LM Studio, llama.cpp o una alternativa equivalente.

La IA local solo debe utilizarse cuando aporte valor práctico, por ejemplo:

- Asistente para consultar información registrada en el sistema.
- Generación de resúmenes diarios, semanales o mensuales.
- Apoyo para redactar reportes de ventas, inventario o compras.
- Consulta guiada sobre procedimientos de la cafetería.
- Búsqueda sobre registros históricos.
- Asistente local para responder preguntas administrativas en lenguaje natural.
- Apoyo en la organización de información previamente registrada.

No presentes la IA como sustituto de la administradora, del control de caja, de la contabilidad profesional, de decisiones financieras o de la validación humana.

La IA no debe modificar automáticamente información sensible. Si se llega a contemplar una función de escritura o modificación, debe requerir validación humana explícita.

## Posible ERP gratuito

También se contempla como alternativa evaluar la viabilidad de integrar o adoptar un ERP gratuito o de código abierto, como Odoo Community Edition u otra alternativa similar.

Sin embargo:

- No asumas que Odoo será seleccionado.
- No afirmes que Odoo es gratuito en todas sus ediciones, módulos o modalidades.
- No inventes compatibilidades, precios, funciones instaladas o módulos concretos.
- Preséntalo como una alternativa tecnológica por validar.
- Indica que la decisión entre construir una solución propia, adaptar un ERP gratuito o integrar ambos enfoques dependerá de la entrevista, los requisitos, los costos, el hardware disponible, la facilidad de uso y la capacidad de mantenimiento.
- Distingue entre la automatización operativa básica y una implementación completa de ERP, ya que esta última puede exceder el alcance académico inicial.

## Referente académico del diplomado

El documento debe estar alineado con los principios del diplomado:

- Diseño de soluciones de IA aplicadas, reproducibles, evaluables y gobernables.
- Uso de modelos locales.
- Protección de datos.
- Privacidad.
- Trazabilidad.
- Gestión de licencias y dependencias.
- Supervisión humana.
- Evaluación de riesgos.
- Uso eficiente de recursos de hardware.
- Desarrollo de soluciones viables para organizaciones con capacidades tecnológicas heterogéneas.
- Documentación de arquitectura, limitaciones, riesgos y decisiones técnicas.

El proyecto integrador requiere definir problema, usuarios, alcance, requisitos y criterios de éxito, además de justificar una arquitectura local o híbrida. En este caso, por decisión del proyecto, la arquitectura será exclusivamente local; no propongas alternativa híbrida ni nube como arquitectura de operación.

## Instrucciones de entrega

Desarrolla únicamente las secciones que se indican a continuación. No agregues introducción, objetivos, justificación extensa, metodología, conclusiones, marco teórico ni referencias bibliográficas, excepto si se requieren brevemente para explicar el NIST AI RMF.

Usa títulos numerados y tablas Markdown cuando sean útiles.

---

# 1. Planteamiento del problema

Redacta un planteamiento del problema formal, de entre 5 y 8 párrafos, sobre la necesidad de automatizar gradualmente la gestión de una cafetería que actualmente registra información en cuadernos físicos.

El planteamiento debe explicar, sin inventar datos, que el uso de registros manuales puede ocasionar problemas potenciales como:

- Dificultad para consultar información histórica.
- Demora en consolidar ventas, compras, gastos o inventario.
- Riesgo de errores de transcripción, omisiones o duplicación de registros.
- Falta de trazabilidad sobre cambios realizados.
- Dependencia de una sola persona que conoce el contenido de los cuadernos.
- Dificultad para generar reportes oportunos.
- Pérdida o deterioro físico de registros.
- Dificultad para apoyar decisiones sobre inventario, productos y compras.
- Limitaciones para buscar información específica.
- Riesgo de acceso no controlado a información del negocio.

Debes indicar expresamente que estos problemas son hipótesis iniciales y deben validarse mediante una entrevista con la administradora de la cafetería.

Explica que se propone una solución local, de fácil uso, que permita digitalizar y organizar gradualmente la información priorizada por la cafetería, manteniendo el control de los datos dentro de su infraestructura.

Incluye al final una pregunta orientadora del proyecto. Debe ser similar a esta, pero puedes mejorar su redacción:

“¿Cómo diseñar una solución local de automatización para una cafetería que permita digitalizar, organizar, consultar y apoyar el seguimiento de sus procesos operativos y administrativos, reduciendo la dependencia de registros manuales en cuadernos y manteniendo el control local de la información?”

No presentes la pregunta como si el sistema ya estuviera construido.

---

# 2. Matriz preliminar de riesgos NIST AI RMF

Explica brevemente que la matriz se presenta como una versión preliminar, elaborada antes de la entrevista con la administradora, y que deberá ajustarse cuando se conozcan los procesos reales, los datos tratados, los usuarios y la infraestructura de la cafetería.

Organiza la matriz por las cuatro funciones del NIST AI RMF:

- Govern.
- Map.
- Measure.
- Manage.

Utiliza las siguientes categorías de riesgo:

- Gobernanza y responsabilidades.
- Datos y privacidad.
- Seguridad de la información.
- Calidad e integridad de datos.
- Operación y continuidad.
- Modelo de IA local.
- Riesgos de automatización.
- Usuarios y experiencia de uso.
- Infraestructura y hardware.
- Dependencias, licencias y software.
- Integración con ERP o sistema administrativo.
- Riesgos económicos y de control de caja.

Antes de la tabla, define la siguiente escala preliminar:

- Probabilidad: Baja, Media o Alta.
- Impacto: Bajo, Medio o Alto.
- Nivel de riesgo: Bajo, Medio, Alto o Crítico.
- Estado: Por validar, Pendiente de mitigación, Mitigado parcialmente o Aceptado con control.

Construye una tabla con entre 12 y 16 riesgos iniciales.

La tabla debe tener estas columnas:

| ID | Función NIST AI RMF | Categoría | Riesgo | Causa o condición | Consecuencia potencial | Probabilidad | Impacto | Nivel | Control o mitigación inicial | Responsable propuesto | Estado |

Incluye riesgos como mínimo sobre:

- Ausencia de responsables definidos para registros y aprobación de cambios.
- Falta de respaldo de la información digitalizada.
- Pérdida de información al pasar del cuaderno al sistema.
- Errores de digitación.
- Acceso no autorizado a ventas, gastos, inventario o datos de empleados.
- Uso de contraseñas débiles o cuentas compartidas.
- Exposición de información si se usan servicios externos sin autorización.
- Datos personales registrados sin finalidad o autorización clara.
- Registros incompletos, inconsistentes o desactualizados.
- Recomendaciones o respuestas erróneas del modelo de IA local.
- Confianza excesiva en los reportes generados por IA.
- Modificación automática de datos sin aprobación humana.
- Integración inadecuada con un ERP gratuito o con Odoo.
- Dependencia de una única persona para operar el sistema.
- Equipo insuficiente, fallas de almacenamiento, energía o mantenimiento.
- Licencias, módulos o dependencias que no sean compatibles con uso comercial o académico.
- Falta de capacitación de los usuarios.
- Riesgo de que el alcance crezca hacia una implementación ERP completa no viable para el tiempo académico.

Para cada riesgo, evita afirmar que ya ocurrió. Preséntalo como riesgo potencial o condición a validar.

Después de la matriz, redacta una interpretación breve de máximo cuatro párrafos que indique cuáles riesgos parecen prioritarios para investigar en la entrevista.

---

# 3. Usuarios y partes interesadas

Identifica los usuarios y partes interesadas de manera preliminar. No inventes nombres propios ni cargos específicos no confirmados.

Incluye una tabla con las columnas:

| Grupo o usuario | Rol preliminar | Necesidad o interés | Interacción esperada con la solución | Información o permisos que podría requerir | Aspectos pendientes de validar |

Incluye como mínimo:

- Administradora de la cafetería.
- Personal de atención o ventas.
- Personal responsable de caja, si existe.
- Personal responsable de inventario o compras, si existe.
- Propietario(a) o responsable del negocio, si existe.
- Proveedores, solo si se requiere registrar compras o pedidos.
- Equipo académico desarrollador.
- Docente o asesor del proyecto.
- Personal externo de soporte técnico, si llega a requerirse.

Explica después de la tabla que la administradora será una fuente prioritaria de levantamiento de información y que la entrevista permitirá validar roles, permisos, procesos, vocabulario del negocio y necesidades reales.

---

# 4. Alcance

Define el alcance inicial como una propuesta académica, incremental y viable.

Divide esta sección en:

## 4.1 Incluye

Incluye elementos como:

- Levantamiento inicial de información mediante entrevista con la administradora.
- Identificación de procesos prioritarios.
- Identificación de los registros manuales más relevantes.
- Diseño de una solución local para digitalizar información seleccionada.
- Gestión básica de usuarios y roles.
- Registro y consulta de información priorizada, sujeto a validación.
- Inventario básico, ventas, compras, gastos o caja, únicamente si la entrevista lo confirma.
- Generación de reportes básicos.
- Copias de seguridad locales.
- Asistente de IA local para consultas y resúmenes, sin modificar registros automáticamente.
- Documentación técnica y manual básico de uso.
- Matriz de riesgos, controles iniciales y recomendaciones.
- Evaluación preliminar de la viabilidad de un ERP gratuito, como Odoo Community Edition u otra alternativa de código abierto.
- Prueba con datos de ejemplo, sintéticos, anonimizados o expresamente autorizados.

## 4.2 Fuera de alcance

Incluye como mínimo:

- Implementación de nube, arquitectura híbrida o APIs de IA externas.
- Automatización sin supervisión humana de decisiones de caja, compras, precios, pagos o contabilidad.
- Integración con bancos, pasarelas de pago, DIAN, facturación electrónica o plataformas externas.
- Sistema contable certificado.
- Nómina completa.
- Implementación total de un ERP empresarial.
- Migración masiva de todos los cuadernos históricos.
- Uso de información personal sensible sin autorización.
- Reconocimiento facial, clonación de voz, vigilancia de empleados o clientes.
- Entrenamiento de modelos fundacionales.
- Implementación de modelos de video, imagen o 3D.
- Desarrollo de aplicación móvil nativa, salvo que la entrevista determine una necesidad crítica y sea viable.
- Garantía de disponibilidad empresarial 24/7.
- Sustitución de asesoría contable, jurídica o tributaria.
- Sustitución de la toma de decisiones de la administradora.

## 4.3 Supuestos y dependencias

Incluye una tabla con:

| Supuesto o dependencia | Estado inicial | Acción requerida para validarlo |

Considera:

- Disponibilidad de un computador local.
- Disponibilidad de electricidad y condiciones básicas de seguridad física.
- Acceso autorizado a registros de ejemplo.
- Tiempo de la administradora para entrevista y validación.
- Disposición del personal para aprender a usar el sistema.
- Existencia de procesos repetitivos que puedan digitalizarse.
- Compatibilidad de Odoo Community Edition u otra alternativa con el entorno disponible.
- Disponibilidad de respaldo local.
- Información clara sobre quién autoriza cambios en ventas, caja, inventario y compras.

---

# 5. Requisitos

Organiza los requisitos en tres tablas.

No asumas que todos los procesos serán incluidos. Marca los que dependen de la entrevista como “[Pendiente de validación]”.

## 5.1 Requisitos funcionales

Usa esta estructura:

| Código | Requisito funcional | Prioridad | Estado de validación | Evidencia de aceptación |

Incluye requisitos preliminares como:

- RF-01: Permitir registrar y consultar información operativa priorizada de la cafetería.
- RF-02: Permitir crear cuentas de usuario con roles básicos.
- RF-03: Permitir registrar cambios con fecha, usuario responsable y motivo cuando aplique.
- RF-04: Permitir registrar productos e insumos [Pendiente de validación].
- RF-05: Permitir registrar entradas y salidas de inventario [Pendiente de validación].
- RF-06: Permitir registrar ventas básicas [Pendiente de validación].
- RF-07: Permitir registrar compras, gastos o proveedores [Pendiente de validación].
- RF-08: Permitir consultar registros históricos mediante filtros básicos.
- RF-09: Permitir generar reportes simples de la información registrada.
- RF-10: Permitir realizar copias de seguridad locales.
- RF-11: Permitir al asistente de IA local responder consultas basadas únicamente en información autorizada.
- RF-12: Exigir confirmación humana antes de que una herramienta automatizada cree, modifique o elimine registros.
- RF-13: Permitir registrar incidencias, observaciones o correcciones.
- RF-14: Permitir exportar información básica a un formato local, como CSV o PDF, sujeto a validación.
- RF-15: Permitir evaluar de manera comparativa la viabilidad de usar un ERP gratuito, como Odoo Community Edition, frente a una solución propia o simplificada.

## 5.2 Requisitos no funcionales

Usa esta estructura:

| Código | Requisito no funcional | Prioridad | Criterio verificable |

Incluye requisitos sobre:

- Operación local sin depender de nube.
- Interfaz sencilla y comprensible para usuarios no técnicos.
- Bajo consumo de recursos.
- Protección mediante cuentas y contraseñas individuales.
- Registro de auditoría de cambios relevantes.
- Respaldo local periódico.
- Recuperación básica ante fallos.
- Mantenibilidad.
- Documentación.
- Control de versiones del código.
- Tiempo de respuesta adecuado para operaciones básicas.
- Compatibilidad con equipos de recursos moderados.
- Actualización controlada de software y modelos.
- Seguridad de datos locales.
- No almacenamiento de claves dentro del código o repositorios.
- Trazabilidad de los resultados generados por IA.
- Restricción de permisos del modelo de IA y de cualquier agente o herramienta.

## 5.3 Requisitos de privacidad, seguridad y gobierno de IA

Usa esta estructura:

| Código | Requisito de seguridad, privacidad o gobierno | Evidencia esperada | Estado |

Incluye:

- Clasificar la información antes de registrarla en el sistema.
- Registrar la finalidad de los datos personales, si estos llegan a tratarse.
- Usar datos de ejemplo, anonimizados o autorizados durante la fase académica.
- Restringir accesos según el rol.
- Mantener copias de seguridad locales protegidas.
- Evitar enviar datos a servicios externos.
- Registrar la versión del modelo local utilizado.
- Documentar licencia y procedencia del modelo, ERP, bibliotecas y dependencias.
- No permitir que la IA modifique registros sin aprobación humana.
- Validar resultados o reportes producidos por IA antes de usarlos para tomar decisiones.
- Mantener un mecanismo para corregir información.
- Proteger las credenciales de acceso.
- Tener un procedimiento básico para reportar incidentes o pérdida de información.
- Definir responsable de revisión de respaldos, permisos y cambios importantes.

---

# 6. Criterios de éxito

Define criterios de éxito realistas, verificables y alineados con un proyecto académico inicial.

Usa una tabla con estas columnas:

| Código | Criterio de éxito | Indicador o evidencia | Meta propuesta | Estado inicial |

Incluye entre 10 y 14 criterios.

Los criterios deben cubrir:

- Entrevista realizada con la administradora.
- Procesos prioritarios identificados y documentados.
- Usuarios y permisos definidos.
- Registros manuales prioritarios identificados.
- Prototipo o solución local funcional.
- Registro y consulta de información priorizada.
- Copia de seguridad local probada.
- Prueba de restauración o verificación de integridad de respaldo.
- Asistente de IA local limitado a consultas autorizadas.
- Confirmación humana para cambios críticos.
- Matriz de riesgos elaborada y revisada.
- Riesgos prioritarios con controles documentados.
- Pruebas con datos autorizados, sintéticos o anonimizados.
- Manual básico de usuario y documentación técnica.
- Evaluación preliminar de viabilidad de Odoo Community Edition u otra alternativa.
- Retroalimentación de la administradora o usuario principal, si está disponible.
- Demostración funcional del flujo priorizado.

No inventes porcentajes de satisfacción, tiempos reales de ahorro ni resultados de pruebas. En “Meta propuesta”, redacta metas por comprobar, por ejemplo:

- “Realizar una entrevista semiestructurada y documentar hallazgos”.
- “Validar al menos un flujo operativo prioritario”.
- “Ejecutar una copia de seguridad local y verificar su disponibilidad”.
- “Aplicar la matriz a la propuesta tecnológica”.
- “Obtener retroalimentación cualitativa de al menos un usuario clave, si está disponible”.

---

# 7. Tecnología e infraestructura requerida

Propón una infraestructura general, escalable y local-first. No afirmes que ya existe. Diferencia claramente entre configuración mínima, recomendada y opcional.

Incluye una introducción breve explicando que la especificación definitiva depende de:

- La cantidad de usuarios simultáneos.
- El volumen de registros.
- El uso real de IA local.
- Si se implementa o no un ERP como Odoo Community Edition.
- El sistema operativo disponible.
- La disponibilidad de respaldo local.
- La entrevista con la administradora.
- Las pruebas de rendimiento.

Luego presenta una tabla con las columnas:

| Componente | Mínimo viable | Recomendado | Justificación | Pendiente de validar |

Incluye, como mínimo:

- Procesador.
- Memoria RAM.
- Almacenamiento principal.
- Tipo de almacenamiento.
- Sistema operativo.
- Red local.
- Equipo cliente.
- Servidor local o equipo principal.
- Sistema de respaldo.
- Fuente de energía o UPS.
- Seguridad física.
- Monitor, teclado, mouse e impresora si se requieren.
- GPU.
- Modelo de IA local.
- Motor de inferencia local.
- Base de datos local.
- Interfaz de usuario.
- Herramientas de desarrollo y mantenimiento.
- ERP gratuito o de código abierto.
- Control de versiones.
- Seguridad y autenticación.

Utiliza las siguientes orientaciones, pero preséntalas como propuestas iniciales, no como requisitos definitivos:

### Configuración mínima viable

- CPU moderna de 4 núcleos o superior.
- 16 GB de RAM.
- SSD con al menos 256 GB de espacio disponible.
- Sistema operativo Linux o Windows, según compatibilidad y facilidad de soporte.
- Sin GPU dedicada obligatoria para procesos administrativos básicos.
- Modelo local pequeño cuantizado, si se implementa IA, orientado a consultas y resúmenes simples.
- Copia de seguridad local en unidad externa o NAS básico.
- Red local estable si existen varios equipos.

### Configuración recomendada

- CPU de 6 a 8 núcleos modernos.
- 32 GB de RAM para operar con mayor comodidad una base de datos local, un ERP ligero y un modelo de IA local pequeño o mediano cuantizado.
- SSD NVMe de 512 GB o superior.
- Disco externo adicional o NAS para respaldos.
- UPS para proteger el equipo principal y evitar pérdida de datos ante cortes de energía.
- Red local Gigabit si habrá más de un equipo conectado.
- GPU opcional, no obligatoria; una GPU con 6 GB a 8 GB de VRAM puede mejorar la velocidad de inferencia local, pero la solución debe poder funcionar sin GPU dedicada usando CPU y modelos cuantizados pequeños.
- Sistema de autenticación local con cuentas individuales.
- Herramienta de control de versiones local o repositorio privado.
- Mecanismo de logs o auditoría para cambios importantes.

### Tecnologías candidatas

Propón tecnologías candidatas, pero no impongas una sola como decisión definitiva:

- Backend: Python con FastAPI, Flask o alternativa equivalente.
- Base de datos: SQLite para un prototipo monousuario o PostgreSQL/MariaDB para varios usuarios.
- Interfaz: aplicación web local sencilla, por ejemplo con Streamlit, Gradio, Flask, FastAPI con frontend web u otra alternativa equivalente.
- IA local: Ollama, GPT4All, LM Studio, llama.cpp o alternativa equivalente.
- Modelo local: un modelo pequeño o mediano cuantizado, seleccionado después de pruebas de memoria, velocidad, idioma español, licencia y calidad.
- ERP: Odoo Community Edition u otro ERP gratuito/de código abierto, solo después de validar necesidades, complejidad, costos de mantenimiento y compatibilidad.
- Copias de seguridad: respaldo cifrado o protegido en disco externo, NAS local o sistema equivalente.
- Control de versiones: Git local o repositorio privado.
- Documentación: manual de usuario, README técnico, registro de versiones y bitácora de cambios.

Aclara que no se recomienda iniciar con modelos grandes, modelos multimodales pesados, entrenamiento de IA, video, imágenes generativas, 3D, integración con nube o automatizaciones autónomas de alto impacto.

---

# Reglas obligatorias de redacción

Cumple todas estas reglas:

- Escribe solamente las siete secciones solicitadas.
- Redacta en tono académico formal y profesional.
- No inventes cifras, entrevistas, nombres de personas, procesos confirmados, datos financieros, herramientas instaladas ni resultados.
- Marca con “[Pendiente de validación con la administradora]” todo elemento que dependa de la entrevista.
- No afirmes que Odoo será implementado; trátalo como alternativa a evaluar.
- No propongas nube ni arquitectura híbrida.
- No uses APIs externas de modelos de IA.
- No recomiendes que un modelo de IA tenga permisos para modificar automáticamente ventas, caja, inventario, compras, precios o datos de usuarios.
- No presentes al sistema como reemplazo de la administradora, contador(a), personal de caja o responsable de inventario.
- No prometas reducción de costos, aumento de ventas ni eliminación de errores sin evidencia.
- Considera privacidad, control de acceso, respaldo, auditoría, licencias, trazabilidad y supervisión humana.
- Mantén un alcance realista para un proyecto académico de diplomado.
- Distingue entre propuesta preliminar, aspecto por validar y requisito confirmado.
- No agregues objetivos, justificación, metodología, conclusiones o secciones adicionales.
- Entrega únicamente el documento solicitado en .md, con sus títulos, párrafos y tablas.
