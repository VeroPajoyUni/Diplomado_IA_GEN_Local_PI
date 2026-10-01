# Diseño de una matriz institucional de riesgos de inteligencia artificial y checklist de privacidad para proyectos académicos de IA local, RAG, agentes y sistemas multimodales

## Resumen

La incorporación de inteligencia artificial generativa en procesos académicos y de ingeniería de sistemas introduce oportunidades para automatizar tareas, consultar conocimiento, generar contenidos y construir soluciones multimodales; simultáneamente, plantea riesgos relacionados con privacidad, seguridad, propiedad intelectual, trazabilidad, uso de herramientas, transferencia de información y confiabilidad de los resultados. El diplomado **Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab** plantea una formación orientada no solo al uso de modelos, sino a su diseño, despliegue, evaluación y gobernanza, con especial énfasis en arquitecturas locales y reproducibles. 

En este contexto, y particularmente en relación con el apartado **8.4 Gobierno académico**, se propone el diseño de un instrumento académico compuesto por una matriz de riesgos de inteligencia artificial y un checklist de privacidad. El instrumento permitirá estructurar la identificación de actores, activos, datos, amenazas, controles, responsables y evidencias, relacionando los riesgos con las funciones **Govern, Map, Measure y Manage** del NIST AI Risk Management Framework. El proyecto tendrá un alcance de formulación y especificación, acompañado de una aplicación demostrativa a un caso académico controlado, sin pretender constituirse en una plataforma institucional productiva ni en una certificación de cumplimiento jurídico.

La propuesta se desarrollará mediante una metodología académica de carácter aplicado, que comprende diagnóstico del contexto, identificación de activos y datos, diseño del instrumento, aplicación controlada, revisión y documentación de limitaciones. Como resultado esperado se obtendrá un formato reproducible, una guía de diligenciamiento y evidencias que permitan valorar su utilidad para proyectos académicos de IA local-first, RAG, agentes y sistemas multimodales.

**Palabras clave:** Inteligencia artificial; gestión de riesgos; NIST AI RMF; privacidad; gobernanza de IA; IA local; proyectos académicos.

---

# 1. Introducción

La inteligencia artificial generativa se ha consolidado como una tecnología transversal para la ingeniería de software, el análisis de información, la automatización, la investigación aplicada y la producción de contenidos digitales. Esta transformación exige superar una aproximación centrada exclusivamente en el consumo de modelos como servicios remotos y avanzar hacia una comprensión integral de su arquitectura, datos, modelos, herramientas, restricciones computacionales, evaluación y riesgos. El documento base del diplomado plantea precisamente esta perspectiva: la inteligencia artificial debe comprenderse como una infraestructura programable, evaluable y gobernable. 

El enfoque **local-first** adquiere especial importancia dentro de esta perspectiva. El documento del diplomado señala que la ejecución local puede permitir mayor control sobre datos, versiones, dependencias y recursos computacionales, además de facilitar escenarios con conectividad limitada. Al mismo tiempo, aclara que el enfoque local no implica rechazar la nube, sino desarrollar criterios de ingeniería para decidir qué información debe procesarse localmente, qué puede utilizar infraestructura compartida y qué información no debería abandonar un entorno controlado. 

Esta orientación se extiende a los sistemas RAG, agentes y aplicaciones multimodales. Un agente puede consultar conocimiento, interactuar con archivos, invocar funciones y ejecutar herramientas; por ello, el diplomado plantea controles relacionados con permisos, aislamiento, validación de entradas, supervisión humana, auditoría y mínimo privilegio. 

De manera transversal, la propuesta curricular incorpora privacidad, propiedad intelectual, trazabilidad, transparencia, supervisión humana, sostenibilidad y gestión de riesgos. En particular, el Módulo 1 establece como actividades la caracterización de casos de uso, identificación de actores y datos, clasificación de sensibilidad, elaboración de mapas de flujo de datos, análisis de procesamiento local, híbrido o remoto y construcción de una primera matriz de riesgos. 

En este marco se encuentra el apartado **8.4 Gobierno académico**, que contempla expresamente un **“Formato de matriz de riesgos de IA y checklist de privacidad”**, junto con otros instrumentos como fichas de modelo y datos, inventarios de licencias y rúbricas.  El presente proyecto toma dicho elemento como objeto específico de desarrollo académico.

La propuesta busca, por tanto, transformar esa necesidad curricular en una especificación estructurada que permita documentar riesgos y condiciones de privacidad durante el ciclo de vida de proyectos académicos de inteligencia artificial, manteniendo una perspectiva de ingeniería y evitando que la gobernanza se limite a declaraciones generales.

---

# 2. Contextualización

## 2.1 Contexto del diplomado

El diplomado **Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab** tiene como propósito formar profesionales capaces de diseñar, desplegar y gobernar soluciones de inteligencia artificial que puedan operar localmente, integrar sistemas RAG y agentes, generar y validar código y producir contenidos multimodales. Su orientación busca que las herramientas tecnológicas funcionen como medios de aprendizaje y no como fines dependientes de una plataforma específica.  

La estructura curricular contempla ocho módulos, de los cuales el primero corresponde a **“Fundamentos, soberanía tecnológica y gobernanza de IA”**, con contenidos relacionados con arquitectura de IA, gobernanza de datos, riesgos, privacidad, propiedad intelectual, trazabilidad, transparencia, supervisión humana y ciclo de vida de los sistemas. 

El Módulo 1 establece una competencia práctica particularmente relacionada con este proyecto: caracterizar casos de uso, identificar actores y datos, clasificar la sensibilidad de la información, elaborar mapas de flujo de datos, determinar qué puede procesarse localmente y construir una primera matriz de riesgos. 

## 2.2 IA local-first

El enfoque local-first constituye uno de los elementos diferenciadores del diplomado. El documento establece que los laboratorios nucleares estarán diseñados para ejecutarse sin conexión una vez preparado el entorno y que la información de casos que requiera confidencialidad o control no deberá abandonar la infraestructura de práctica. 

Este principio tiene implicaciones directas para la gestión de riesgos. Una decisión aparentemente técnica —por ejemplo, utilizar un modelo local, un servicio externo o una arquitectura híbrida— puede modificar la exposición de los datos, las dependencias, la trazabilidad y las responsabilidades asociadas al sistema.

## 2.3 RAG, agentes y herramientas

El diplomado incorpora sistemas RAG para trabajar con documentos y bases de conocimiento, así como agentes capaces de utilizar herramientas controladas. El material establece que los documentos utilizados para RAG deben tratarse como activos de información, mientras que los agentes deben contar con permisos explícitos, controles y, cuando corresponda, sandboxing y aprobación humana para acciones sensibles. 

En consecuencia, una matriz de riesgos académica debe considerar no solamente el modelo de IA, sino también los documentos, embeddings, herramientas, permisos, integraciones, fuentes externas y personas involucradas.

## 2.4 Sistemas multimodales y contenido sintético

El diplomado incluye generación y análisis de imagen, visión, audio, voz, video y 3D. Estas capacidades incorporan riesgos particulares relacionados con identidad, consentimiento, procedencia, derechos de autor y contenido sintético. El documento establece que las piezas sintéticas deben identificarse cuando puedan inducir a error y que no deben clonarse voces, rostros o estilos identificables sin consentimiento y análisis de derechos. 

Por ello, el checklist propuesto debe extender la privacidad más allá de los datos textuales e incluir imágenes, voz, rostro y contenido generado.

## 2.5 Protección de datos y responsabilidad humana

El documento base establece que, cuando los laboratorios o proyectos tratan datos personales, deben considerarse finalidad, autorización cuando corresponda, seguridad, confidencialidad, circulación restringida y derechos de los titulares. Asimismo, se plantea priorizar datos públicos, sintéticos, anonimizados o autorizados en las actividades académicas. 

La ejecución local puede reducir transferencias innecesarias, pero no elimina las obligaciones relacionadas con la protección de los datos. De igual manera, la generación de contenido mediante IA no elimina la responsabilidad humana sobre su verificación y uso. 

## 2.6 Diferenciación entre información establecida y propuesta

Los siguientes elementos se consideran **establecidos en el documento base**:

* El enfoque de ingeniería aplicado al diplomado.
* El énfasis local-first.
* La incorporación de RAG, agentes y sistemas multimodales.
* La gestión de privacidad, seguridad, licenciamiento y trazabilidad.
* El uso del NIST AI RMF.
* Las funciones Govern, Map, Measure y Manage.
* La existencia de un formato de matriz de riesgos de IA y checklist de privacidad dentro del apartado 8.4.

Por otra parte, los siguientes elementos corresponden a la **propuesta específica de este proyecto**:

* La estructura detallada de campos de la matriz.
* La escala preliminar de probabilidad e impacto.
* La organización concreta del checklist.
* Los criterios de diligenciamiento.
* El esquema de evidencias.
* El caso académico controlado que se utilice para probar el instrumento.

La existencia de procedimientos institucionales adicionales, formatos actualmente vigentes o responsables institucionales específicos deberá confirmarse antes de plantear una adopción formal:

**[Pendiente de validación institucional]**: verificar si actualmente existe una matriz institucional de riesgos de IA, un checklist de privacidad, procedimientos de aprobación de proyectos de IA, responsables formales o instrumentos equivalentes que deban integrarse o evitar duplicarse.

---

# 3. Planteamiento del problema

## 3.1 Situación actual

Los proyectos académicos de inteligencia artificial pueden involucrar múltiples componentes técnicos y diferentes categorías de información. Un proyecto puede utilizar documentos para RAG, conjuntos de datos, modelos locales o externos, APIs, herramientas, repositorios de código, agentes, contenido multimodal y mecanismos de almacenamiento.

El propio diplomado contempla proyectos que deben integrar arquitectura, datos, integración, evaluación, seguridad, privacidad, licencias y documentación. Además, exige que los proyectos incorporen una matriz de riesgos y medidas de seguridad. 

Desde esta perspectiva, el riesgo no se encuentra exclusivamente en el modelo. También puede surgir de los datos utilizados, la procedencia de un modelo o dataset, una licencia incompatible, una transferencia de información hacia un servicio externo, un agente con permisos excesivos, una herramienta vulnerable o una salida que no haya sido verificada.

## 3.2 Situación problemática

En el contexto académico analizado se observa la necesidad de contar con un mecanismo estructurado que facilite la identificación y documentación homogénea de estos elementos. El documento base establece la necesidad de formatos de gobierno académico, incluyendo específicamente una matriz de riesgos de IA y un checklist de privacidad. 

Sin embargo, **[Pendiente de validación institucional]** si ya existe actualmente un instrumento formal con el nivel de detalle requerido para proyectos que incorporen IA local, RAG, agentes, herramientas y sistemas multimodales.

En ausencia de un mecanismo estandarizado o cuando los instrumentos existentes resulten insuficientes, podrían presentarse diferencias entre equipos en aspectos como:

* Identificación y clasificación de datos.
* Registro de actores y responsables.
* Evaluación de modelos y dependencias.
* Documentación de licencias y procedencia.
* Identificación de transferencias hacia servicios externos.
* Análisis de riesgos de agentes y herramientas.
* Registro de controles y medidas de mitigación.
* Evidencia de pruebas de seguridad.
* Seguimiento del riesgo residual.
* Documentación de decisiones de arquitectura.

La situación no implica afirmar que estos controles no existan; plantea la necesidad de determinar si pueden ser sistematizados mediante un instrumento académico común.

## 3.3 Consecuencias potenciales

La ausencia o dispersión de criterios homogéneos podría dificultar:

* La protección adecuada de información personal, institucional o empresarial.
* La identificación de transferencias no autorizadas hacia servicios externos.
* La determinación clara de responsabilidades.
* El control de licencias y procedencia de modelos y datasets.
* La evaluación de resultados generados por IA.
* La identificación de riesgos de prompt injection y fuga de información.
* La delimitación de permisos otorgados a agentes.
* La comparación entre proyectos.
* La reproducibilidad de las decisiones técnicas.
* La sustentación de controles ante docentes, asesores o instancias académicas.

Estos riesgos son coherentes con las preocupaciones de seguridad y gobernanza contempladas en el diplomado, particularmente prompt injection, fuga de datos, tool misuse, dependencias, permisos excesivos y supply chain de modelos. 

## 3.4 Necesidad de intervención

Ante esta situación resulta pertinente formular un instrumento que permita:

1. Identificar los activos, datos, actores y procesos involucrados.
2. Clasificar los riesgos de manera estructurada.
3. Relacionar cada riesgo con las funciones Govern, Map, Measure y Manage.
4. Registrar controles, responsables y evidencias.
5. Incorporar verificaciones específicas de privacidad.
6. Documentar decisiones relacionadas con procesamiento local, híbrido o remoto.
7. Facilitar la trazabilidad de modelos, datasets, herramientas y dependencias.
8. Establecer una base común para la revisión académica de proyectos.

El instrumento deberá entenderse como un mecanismo de apoyo a la ingeniería responsable y no como sustituto de la revisión humana, jurídica o institucional.

## 3.5 Pregunta orientadora

**¿Cómo diseñar una matriz de riesgos de inteligencia artificial y un checklist de privacidad, alineados con el NIST AI RMF, que permitan identificar, evaluar, mitigar y documentar los riesgos de proyectos académicos de IA local, RAG, agentes y sistemas multimodales dentro del diplomado IA 5.0 Lab?**

---

# 4. Justificación

## 4.1 Justificación académica

El proyecto se encuentra directamente relacionado con el Módulo 1, cuyo propósito es introducir una perspectiva de ingeniería sobre gobernanza, datos, riesgos y arquitectura de IA. Entre sus actividades se encuentra precisamente la construcción de una primera matriz de riesgos y la toma de decisiones sobre procesamiento local, híbrido o remoto. 

La creación de un instrumento estructurado permitiría convertir conocimientos conceptuales en una evidencia práctica y reutilizable. Asimismo, el documento base establece que las competencias deben evidenciarse mediante configuraciones reproducibles, repositorios, pruebas, prototipos, bitácoras y sustentaciones técnicas. 

El resultado podría servir como referencia para otros proyectos académicos, siempre sujeto a la validación y adaptación institucional correspondiente.

## 4.2 Justificación técnica

Desde el punto de vista técnico, la propuesta permite integrar diferentes dimensiones de una solución de IA:

* Datos.
* Modelos.
* Herramientas.
* Arquitectura.
* Integraciones.
* Dependencias.
* Seguridad.
* Privacidad.
* Evaluación.
* Trazabilidad.

El instrumento permitirá documentar decisiones técnicas que normalmente podrían quedar dispersas en código, notebooks, repositorios o documentos de proyecto.

También permitirá incorporar el principio de reproducibilidad planteado en el diplomado, que considera versiones, modelos, parámetros, prompts críticos y dependencias. 

## 4.3 Justificación ética y de privacidad

La gobernanza de IA requiere considerar las posibles afectaciones a personas cuyos datos, imágenes, voces o información puedan ser procesados. El documento base incorpora privacidad, transparencia, responsabilidad, supervisión humana y no discriminación como elementos transversales. 

El checklist propuesto permitirá llevar estos principios a preguntas concretas y verificables, evitando que la privacidad se trate únicamente como una declaración general.

## 4.4 Justificación territorial e institucional

El diplomado reconoce la pertinencia de la IA local para el Cauca debido a la heterogeneidad de capacidades tecnológicas y conectividad existente en el territorio. Se mencionan específicamente Popayán y Santander de Quilichao como contextos con ecosistemas educativos, empresariales, industriales, comerciales y de servicios. 

En este contexto, un instrumento que permita decidir qué información debe permanecer localmente y qué información podría procesarse mediante servicios externos resulta pertinente para proyectos desarrollados en organizaciones con diferentes capacidades de infraestructura.

La propuesta no presupone que todas las organizaciones del territorio tengan las mismas necesidades o restricciones. **[Pendiente de validación institucional y territorial]**: establecer posteriormente, mediante los mecanismos académicos que correspondan, si las necesidades del instrumento coinciden con los procesos específicos de las instituciones o grupos que eventualmente lo utilicen.

---

# 5. Objetivos

## 5.1 Objetivo general

**Diseñar una matriz institucional de riesgos de inteligencia artificial y un checklist de privacidad, alineados con el NIST AI RMF y adaptados al contexto académico del diplomado IA 5.0 Lab, con el fin de fortalecer la identificación, evaluación, mitigación y documentación de riesgos en proyectos de IA local, RAG, agentes y sistemas multimodales.**

## 5.2 Objetivos específicos

1. **Diagnosticar** el contexto de los proyectos académicos de IA mediante la identificación de actores, activos de información, datos, procesos, dependencias y riesgos asociados.

2. **Diseñar** una matriz de riesgos de IA alineada con las funciones Govern, Map, Measure y Manage del NIST AI RMF, incorporando criterios de valoración, controles, responsables y evidencias.

3. **Elaborar** un checklist académico de privacidad, seguridad, licenciamiento, trazabilidad y protección de datos aplicable a proyectos de IA local, RAG, agentes y sistemas multimodales.

4. **Validar** la aplicabilidad del instrumento mediante un caso académico controlado, revisión técnica o ejercicio piloto, documentando observaciones, limitaciones y oportunidades de mejora.

---

# 6. Alcance

El proyecto comprende la formulación y especificación de un instrumento académico para la gestión inicial de riesgos y privacidad en proyectos de inteligencia artificial.

El alcance contempla:

* Identificación de actores y responsables.
* Identificación de activos de información.
* Clasificación básica de datos.
* Identificación de riesgos técnicos, éticos, legales, de seguridad y privacidad.
* Diseño de la matriz de riesgos.
* Relación de riesgos con Govern, Map, Measure y Manage.
* Definición de campos de riesgo.
* Criterios de probabilidad e impacto.
* Nivel de riesgo.
* Medidas de tratamiento.
* Responsable del control.
* Evidencia requerida.
* Estado del riesgo.
* Checklist de privacidad.
* Reglas de uso para proyectos académicos de IA.
* Aplicación demostrativa a un caso controlado.
* Documentación de limitaciones y supuestos.
* Recomendaciones para futuras validaciones institucionales.

El instrumento se diseñará procurando independencia respecto de una herramienta tecnológica particular, en coherencia con el principio del diplomado de enseñar capacidades permanentes y no depender de una plataforma específica. 

## 6.1 Estructura propuesta de la matriz de riesgos

| Campo                         | Descripción                                                                  |
| ----------------------------- | ---------------------------------------------------------------------------- |
| Identificador del riesgo      | Código único del riesgo                                                      |
| Activo afectado               | Información, modelo, herramienta, infraestructura, repositorio u otro activo |
| Categoría                     | Tipo de riesgo                                                               |
| Descripción                   | Descripción concreta del riesgo                                              |
| Fuente o causa                | Condición que origina o favorece el riesgo                                   |
| Evento de riesgo              | Situación que puede materializarse                                           |
| Consecuencia                  | Efecto potencial                                                             |
| Usuarios o terceros afectados | Personas, grupos u organizaciones potencialmente afectados                   |
| Probabilidad                  | Valoración propuesta de ocurrencia                                           |
| Impacto                       | Valoración propuesta de consecuencia                                         |
| Nivel inherente               | Resultado antes de controles                                                 |
| Controles existentes          | Medidas actualmente disponibles                                              |
| Medidas de mitigación         | Acciones propuestas para reducir el riesgo                                   |
| Responsable                   | Persona o rol encargado del tratamiento                                      |
| Evidencia                     | Documento, prueba, registro o artefacto verificable                          |
| Riesgo residual               | Riesgo después de aplicar controles                                          |
| Estado                        | Abierto, en tratamiento, aceptado, cerrado u otro estado validado            |
| Función NIST AI RMF           | Govern, Map, Measure o Manage                                                |
| Fecha de revisión             | Fecha de actualización                                                       |

## 6.2 Criterios preliminares de valoración

Se propone una escala sencilla:

* **Probabilidad:** 1 = baja, 2 = media, 3 = alta.
* **Impacto:** 1 = bajo, 2 = medio, 3 = alto.
* **Nivel de riesgo:** Probabilidad × Impacto.

| Resultado | Nivel |
| --------: | ----- |
|       1–2 | Bajo  |
|       3–4 | Medio |
|       6–9 | Alto  |

Esta escala constituye una **propuesta metodológica inicial** y deberá validarse durante la aplicación del instrumento.

## 6.3 Mapa básico de flujo de información

De manera preliminar, el flujo del proyecto puede representarse así:

**Fuentes de datos → clasificación y autorización → almacenamiento/repositorio → modelo local, RAG o herramienta → procesamiento/generación → evaluación → usuario → registro de evidencias y controles**

Cuando intervengan servicios externos:

**Datos autorizados → evaluación de transferencia → servicio externo → procesamiento → resultado → verificación humana → registro**

La decisión de transferir información deberá documentarse en función de la sensibilidad de los datos, autorización, necesidad técnica y controles disponibles.

## 6.4 Decisiones de arquitectura

El instrumento deberá permitir registrar si cada proyecto utiliza:

* Arquitectura local.
* Arquitectura híbrida.
* Arquitectura remota.

La decisión deberá acompañarse de una justificación relacionada con datos, modelos, recursos, conectividad, privacidad, seguridad, licenciamiento y necesidades de procesamiento.

---

# 7. Fuera de alcance

El proyecto no contempla:

* Desarrollar un sistema institucional completo de gestión de riesgos.
* Sustituir la revisión jurídica de la institución.
* Constituir una certificación de cumplimiento legal.
* Garantizar que un proyecto sea completamente seguro.
* Realizar auditorías formales a terceros.
* Entrenar modelos fundacionales.
* Construir modelos de IA desde cero.
* Implementar un SOC, SIEM o plataforma empresarial de ciberseguridad.
* Procesar datos personales reales sin autorización expresa.
* Utilizar información empresarial confidencial no anonimizada.
* Medir impactos sociales a gran escala.
* Reemplazar la revisión humana.
* Determinar por sí sola la aprobación institucional definitiva de un proyecto.
* Desarrollar una aplicación productiva de alta disponibilidad.
* Cubrir todas las normas internacionales existentes.

El resultado será un **instrumento académico y técnico inicial**, susceptible de validación, ampliación y eventual adopción institucional.

---

# 8. Usuarios y partes interesadas

## 8.1 Identificación general

| Parte interesada                                           | Interés                                  | Responsabilidad o necesidad                      | Interacción con el instrumento          | Riesgo si no lo utiliza                           |
| ---------------------------------------------------------- | ---------------------------------------- | ------------------------------------------------ | --------------------------------------- | ------------------------------------------------- |
| Estudiantes del diplomado                                  | Desarrollar proyectos de IA responsables | Identificar y gestionar riesgos de sus proyectos | Diligenciamiento y actualización        | Omisión de riesgos o controles                    |
| Docentes                                                   | Evaluar competencias                     | Revisar evidencias y criterios técnicos          | Revisión y retroalimentación            | Evaluación heterogénea                            |
| Asesores de proyectos                                      | Orientar decisiones                      | Apoyar arquitectura, riesgos y documentación     | Consulta y validación                   | Decisiones técnicas insuficientemente sustentadas |
| Coordinación académica                                     | Gestionar el diplomado                   | Definir o validar lineamientos                   | Administración o revisión institucional | Falta de estandarización                          |
| Responsables de laboratorios                               | Mantener condiciones de práctica         | Apoyar controles técnicos                        | Consulta de requisitos                  | Exposición de información o recursos              |
| Equipos de desarrollo                                      | Construir soluciones                     | Implementar controles                            | Aplicación durante desarrollo           | Riesgos incorporados al sistema                   |
| Responsables de datos                                      | Gestionar información                    | Revisar procedencia, acceso y uso                | Validación de datos                     | Uso inadecuado de información                     |
| Organizaciones aliadas, cuando aplique                     | Obtener soluciones pertinentes           | Definir condiciones de información               | Consulta y validación                   | Transferencias o usos no autorizados              |
| Usuarios o titulares de datos                              | Protección de su información             | Ejercer derechos cuando corresponda              | Indirecta, mediante controles           | Afectación de privacidad                          |
| Instancia institucional que eventualmente revise proyectos | Gobierno académico                       | Revisar condiciones de proyectos                 | Consulta de evidencias                  | Decisiones sin trazabilidad                       |

La existencia, denominación y funciones específicas de instancias institucionales deberán confirmarse:

**[Pendiente de validación institucional]**: determinar qué dependencias o comités tendrán formalmente responsabilidades sobre revisión, aprobación, privacidad o gobierno de proyectos de IA.

---

# 9. Requisitos del proyecto

## 9.1 Requisitos funcionales

| Código | Tipo      | Requisito                                                    | Prioridad | Evidencia de cumplimiento  |
| ------ | --------- | ------------------------------------------------------------ | --------- | -------------------------- |
| RF-01  | Funcional | Registrar la información general del proyecto                | Alta      | Formato diligenciado       |
| RF-02  | Funcional | Identificar actores y responsables                           | Alta      | Registro de actores        |
| RF-03  | Funcional | Registrar activos de información                             | Alta      | Inventario                 |
| RF-04  | Funcional | Clasificar los datos utilizados                              | Alta      | Clasificación documentada  |
| RF-05  | Funcional | Registrar modelos, datasets, herramientas y proveedores      | Alta      | Inventario técnico         |
| RF-06  | Funcional | Identificar riesgos del proyecto                             | Alta      | Matriz                     |
| RF-07  | Funcional | Registrar probabilidad e impacto                             | Alta      | Matriz diligenciada        |
| RF-08  | Funcional | Obtener un nivel de riesgo                                   | Alta      | Valoración documentada     |
| RF-09  | Funcional | Asociar controles y mitigaciones                             | Alta      | Registro de controles      |
| RF-10  | Funcional | Relacionar riesgos con Govern, Map, Measure y Manage         | Alta      | Campo NIST diligenciado    |
| RF-11  | Funcional | Registrar evidencias                                         | Alta      | Repositorio o anexos       |
| RF-12  | Funcional | Completar el checklist de privacidad                         | Alta      | Checklist diligenciado     |
| RF-13  | Funcional | Registrar decisiones de arquitectura local, híbrida o remota | Alta      | Ficha de arquitectura      |
| RF-14  | Funcional | Registrar transferencias a servicios externos                | Alta      | Registro de transferencias |
| RF-15  | Funcional | Aplicar la matriz a un caso académico controlado             | Alta      | Caso de aplicación         |
| RF-16  | Funcional | Generar una versión reproducible del instrumento             | Media     | Archivo/versionado         |
| RF-17  | Funcional | Registrar estado y fecha de revisión de los riesgos          | Media     | Historial de revisión      |

## 9.2 Requisitos no funcionales

| Código | Tipo         | Requisito                                                  | Prioridad | Evidencia de cumplimiento |
| ------ | ------------ | ---------------------------------------------------------- | --------- | ------------------------- |
| RNF-01 | No funcional | El instrumento debe ser claro para usuarios académicos     | Alta      | Revisión de comprensión   |
| RNF-02 | No funcional | Debe permitir reproducir el diligenciamiento               | Alta      | Guía y versión controlada |
| RNF-03 | No funcional | Debe mantener trazabilidad de cambios                      | Alta      | Control de versiones      |
| RNF-04 | No funcional | Debe preservar la confidencialidad de la información       | Alta      | Reglas de manejo          |
| RNF-05 | No funcional | Debe mantener integridad de registros                      | Alta      | Versionado y controles    |
| RNF-06 | No funcional | Debe tener disponibilidad razonable                        | Media     | Acceso al instrumento     |
| RNF-07 | No funcional | Debe poder utilizarse localmente cuando sea posible        | Media     | Versión local             |
| RNF-08 | No funcional | Debe requerir bajo costo computacional                     | Media     | Evaluación técnica        |
| RNF-09 | No funcional | Debe ser mantenible y actualizable                         | Alta      | Estructura editable       |
| RNF-10 | No funcional | Debe facilitar accesibilidad y comprensión                 | Media     | Revisión                  |
| RNF-11 | No funcional | Debe ser independiente de una plataforma específica        | Alta      | Diseño neutral            |
| RNF-12 | No funcional | Debe permitir incorporación de nuevas categorías de riesgo | Media     | Estructura extensible     |

## 9.3 Requisitos de privacidad y seguridad

| Código | Tipo           | Requisito                                     | Prioridad | Evidencia de cumplimiento |
| ------ | -------------- | --------------------------------------------- | --------- | ------------------------- |
| RPS-01 | Privacidad     | No almacenar claves API o secretos            | Alta      | Revisión del repositorio  |
| RPS-02 | Privacidad     | No utilizar datos sensibles sin autorización  | Alta      | Evidencia de autorización |
| RPS-03 | Privacidad     | Aplicar minimización de datos                 | Alta      | Justificación de datos    |
| RPS-04 | Privacidad     | Definir responsables del tratamiento          | Alta      | Registro                  |
| RPS-05 | Privacidad     | Registrar transferencias externas             | Alta      | Registro de servicios     |
| RPS-06 | Seguridad      | Controlar permisos de herramientas y agentes  | Alta      | Configuración y pruebas   |
| RPS-07 | Licenciamiento | Documentar procedencia de modelos y datasets  | Alta      | Inventario                |
| RPS-08 | Seguridad      | Evaluar prompt injection                      | Alta      | Evidencias de pruebas     |
| RPS-09 | Seguridad      | Evaluar fuga de información                   | Alta      | Evidencias de pruebas     |
| RPS-10 | Seguridad      | Registrar incidentes o excepciones            | Media     | Bitácora                  |
| RPS-11 | Gobernanza     | Mantener supervisión humana                   | Alta      | Registro de revisión      |
| RPS-12 | Seguridad      | Registrar versiones de modelos y dependencias | Alta      | Manifiesto o inventario   |

Estos requisitos se fundamentan en las recomendaciones de seguridad y privacidad del documento base, que incluyen control de agentes, protección de secretos, clasificación de documentos RAG, pruebas de prompt injection y fuga de datos, así como registro de versiones y procedencia de modelos. 

---

# 10. Matriz preliminar de riesgos NIST AI RMF

El NIST AI RMF se utiliza en el diplomado como referente operativo para organizar la gestión de riesgos mediante **Govern, Map, Measure y Manage**. Estas funciones se traducen en responsabilidades, contexto, pruebas, métricas, controles y decisiones de aceptación o mitigación. 

La siguiente matriz corresponde a una **valoración preliminar académica propuesta** para el diseño del instrumento. No representa resultados de una evaluación institucional ni riesgos medidos sobre un sistema real. Los responsables concretos y el riesgo residual deberán validarse durante la aplicación.

| ID   | Función NIST  | Categoría            | Riesgo / causa / consecuencia                                                 | Activo afectado       | Usuarios afectados     |  P |  I |   Nivel | Control o mitigación propuesta                                       | Responsable            | Evidencia                 | Riesgo residual | Estado  |
| ---- | ------------- | -------------------- | ----------------------------------------------------------------------------- | --------------------- | ---------------------- | -: | -: | ------: | -------------------------------------------------------------------- | ---------------------- | ------------------------- | --------------- | ------- |
| R-01 | Govern        | Privacidad           | Tratamiento de datos personales sin autorización o finalidad documentada      | Datos personales      | Titulares              |  2 |  3 |  6 Alto | Clasificación, autorización, minimización y revisión previa          | [Pendiente de validar] | Checklist y autorización  | Pendiente       | Abierto |
| R-02 | Govern        | Privacidad/seguridad | Transferencia involuntaria de información a servicios externos                | Datos y documentos    | Titulares/organización |  2 |  3 |  6 Alto | Identificar servicios externos y decidir qué información puede salir | [Pendiente de validar] | Mapa de flujo             | Pendiente       | Abierto |
| R-03 | Map           | Datos                | Falta de clasificación de información utilizada en RAG o datasets             | Documentos/datasets   | Usuarios/titulares     |  3 |  3 |  9 Alto | Clasificación por sensibilidad y procedencia                         | [Pendiente de validar] | Inventario de datos       | Pendiente       | Abierto |
| R-04 | Govern        | Licenciamiento       | Uso de modelos, datasets o contenidos con licencia incompatible o desconocida | Modelos/datasets      | Equipo/organización    |  2 |  3 |  6 Alto | Inventario de licencias y procedencia                                | [Pendiente de validar] | Registro de licencias     | Pendiente       | Abierto |
| R-05 | Map           | Supply chain         | Procedencia desconocida de modelos o dependencias                             | Modelos/dependencias  | Proyecto               |  2 |  3 |  6 Alto | Registrar fuente, versión, licencia e identificador                  | [Pendiente de validar] | Manifiesto                | Pendiente       | Abierto |
| R-06 | Measure       | Seguridad            | Prompt injection que altera instrucciones o induce acciones no previstas      | RAG/agente            | Proyecto/usuarios      |  2 |  3 |  6 Alto | Pruebas adversariales, validación de entradas y aislamiento          | [Pendiente de validar] | Casos de prueba           | Pendiente       | Abierto |
| R-07 | Manage        | Seguridad            | Fuga de información durante consultas, respuestas o herramientas              | Datos/contexto        | Titulares/organización |  2 |  3 |  6 Alto | Control de contexto, permisos y pruebas de fuga                      | [Pendiente de validar] | Informe de pruebas        | Pendiente       | Abierto |
| R-08 | Govern/Manage | Agentes              | Permisos excesivos permiten ejecutar acciones no necesarias                   | Herramientas/sistema  | Proyecto/terceros      |  2 |  3 |  6 Alto | Mínimo privilegio, sandboxing y aprobación humana                    | [Pendiente de validar] | Matriz de permisos        | Pendiente       | Abierto |
| R-09 | Measure       | Calidad              | Respuestas no verificadas o alucinaciones utilizadas como información factual | Salidas del modelo    | Usuarios               |  3 |  2 |  6 Alto | Grounding, citas, pruebas y verificación humana                      | [Pendiente de validar] | Batería de evaluación     | Pendiente       | Abierto |
| R-10 | Measure       | Equidad              | Sesgos o resultados discriminatorios no identificados                         | Modelo/salidas        | Personas afectadas     |  2 |  3 |  6 Alto | Pruebas, revisión de casos y documentación de limitaciones           | [Pendiente de validar] | Informe de evaluación     | Pendiente       | Abierto |
| R-11 | Govern/Map    | Contenido sintético  | Contenido generado presentado sin identificación cuando pueda inducir a error | Imagen/audio/video/3D | Usuarios/terceros      |  2 |  2 | 4 Medio | Identificación de contenido sintético y metadatos                    | [Pendiente de validar] | Registro de procedencia   | Pendiente       | Abierto |
| R-12 | Govern        | Trazabilidad         | Falta de registro de modelos, datos, parámetros, decisiones y cambios         | Proyecto              | Equipo/docentes        |  3 |  2 |  6 Alto | Versionado, fichas, bitácora y evidencias                            | [Pendiente de validar] | Repositorio/documentación | Pendiente       | Abierto |

### 10.1 Interpretación metodológica

Los valores anteriores constituyen una **propuesta inicial para estructurar el instrumento**, no una medición empírica. La probabilidad y el impacto deberán revisarse cuando se aplique la matriz a un caso concreto.

La función **Govern** se relaciona principalmente con políticas de uso, roles, inventarios, licencias, supervisión y documentación. **Map** permite contextualizar usuarios, datos, impactos, amenazas y dependencias. **Measure** concentra pruebas, evaluación y medición de calidad y seguridad. **Manage** aborda mitigaciones, límites de autonomía, controles, monitoreo y mejora. Esta correspondencia sigue la aplicación establecida en el documento base del diplomado. 

---

# 11. Checklist preliminar de privacidad

El checklist se plantea como un instrumento de verificación y no como certificación jurídica. Su aplicación deberá adaptarse al tipo de proyecto, datos utilizados y condiciones institucionales.

## 11.1 Definición del caso de uso

| Código  | Pregunta de verificación                             |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ---------------------------------------------------- | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-01 | ¿El propósito del proyecto está claramente definido? |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-02 | ¿Se ha identificado quiénes utilizarán la solución?  |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-03 | ¿Se han identificado posibles personas afectadas?    |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-04 | ¿Se ha justificado la necesidad de utilizar IA?      |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.2 Identificación y clasificación de datos

| Código  | Pregunta de verificación                                                             |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ------------------------------------------------------------------------------------ | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-05 | ¿Se han identificado todas las fuentes de datos?                                     |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-06 | ¿Los datos han sido clasificados según su sensibilidad?                              |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-07 | ¿Se ha determinado si existen datos personales?                                      |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-08 | ¿Se ha justificado la necesidad de cada categoría de dato?                           |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-09 | ¿Se utilizan preferentemente datos públicos, sintéticos, anonimizados o autorizados? |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.3 Recolección y autorización

| Código  | Pregunta de verificación                              |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ----------------------------------------------------- | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-10 | ¿Se ha definido la finalidad del tratamiento?         |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-11 | ¿Se ha verificado la autorización cuando corresponda? |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-12 | ¿Se ha documentado la procedencia de los datos?       |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-13 | ¿Se ha evitado recolectar información innecesaria?    |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.4 Preparación y almacenamiento

| Código  | Pregunta de verificación                                     |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ------------------------------------------------------------ | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-14 | ¿Los datos se almacenan en un entorno controlado?            |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-15 | ¿Se han definido permisos de acceso?                         |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-16 | ¿Se ha definido una política de conservación y eliminación?  |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-17 | ¿Se han realizado copias o respaldos cuando sean necesarios? |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.5 Modelos, herramientas y licencias

| Código  | Pregunta de verificación                            |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | --------------------------------------------------- | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-18 | ¿Se conoce la procedencia del modelo utilizado?     |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-19 | ¿Se conoce su licencia y condición de uso?          |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-20 | ¿Se conoce la procedencia de datasets y contenidos? |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-21 | ¿Se han documentado las dependencias relevantes?    |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.6 Procesamiento local, híbrido o remoto

| Código  | Pregunta de verificación                                         |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ---------------------------------------------------------------- | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-22 | ¿Se ha definido dónde se procesan los datos?                     |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-23 | ¿Se ha justificado el procesamiento local, híbrido o remoto?     |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-24 | ¿Se han identificado transferencias hacia servicios externos?    |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-25 | ¿Se ha evitado transferir información sensible sin autorización? |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.7 RAG, agentes y herramientas

| Código  | Pregunta de verificación                                               |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ---------------------------------------------------------------------- | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-26 | ¿Los documentos utilizados en RAG han sido clasificados y autorizados? |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-27 | ¿Los agentes tienen únicamente los permisos necesarios?                |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-28 | ¿Las herramientas disponibles están delimitadas?                       |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-29 | ¿Se han probado escenarios de prompt injection?                        |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-30 | ¿Se han evaluado posibles fugas de información?                        |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-31 | ¿Las acciones sensibles requieren supervisión humana?                  |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.8 Contenido sintético e identidad

| Código  | Pregunta de verificación                                                 |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ------------------------------------------------------------------------ | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-32 | ¿Se identifica el contenido sintético cuando puede inducir a error?      |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-33 | ¿Existe consentimiento para utilizar imágenes, voz o rostro de personas? |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-34 | ¿Se ha documentado la procedencia de los insumos multimodales?           |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-35 | ¿Se han revisado las condiciones de uso de los contenidos?               |  ☐  |  ☐  |  ☐  |           |             |               |

## 11.9 Evaluación y operación

| Código  | Pregunta de verificación                                                             |  Sí |  No | N/A | Evidencia | Responsable | Observaciones |
| ------- | ------------------------------------------------------------------------------------ | :-: | :-: | :-: | --------- | ----------- | ------------- |
| PRIV-36 | ¿Las salidas generadas son verificadas antes de utilizarse como información factual? |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-37 | ¿Se han documentado limitaciones conocidas?                                          |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-38 | ¿Existe registro de incidentes o excepciones?                                        |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-39 | ¿Se conserva trazabilidad de cambios y versiones?                                    |  ☐  |  ☐  |  ☐  |           |             |               |
| PRIV-40 | ¿Existe supervisión humana durante el uso del sistema?                               |  ☐  |  ☐  |  ☐  |           |             |               |

La estructura anterior toma como referencia las recomendaciones del documento base sobre protección de datos, documentos RAG, agentes, contenido sintético, licenciamiento, procedencia y supervisión humana. 

---

# 12. Criterios de éxito

Los siguientes criterios se plantean como metas de evaluación del proyecto, no como resultados ya obtenidos:

| Criterio                                                                         | Evidencia esperada         |
| -------------------------------------------------------------------------------- | -------------------------- |
| La matriz contiene todos los campos definidos                                    | Versión final de la matriz |
| Los riesgos se relacionan con Govern, Map, Measure y Manage                      | Matriz diligenciada        |
| El checklist cubre privacidad, seguridad, licencias y trazabilidad               | Checklist final            |
| El instrumento puede aplicarse a un caso académico controlado                    | Caso de aplicación         |
| Los usuarios pueden comprender cómo diligenciarlo                                | Guía y revisión            |
| Se identifican datos, activos, responsables y controles                          | Caso diligenciado          |
| Se documentan supuestos y limitaciones                                           | Documento de aplicación    |
| El instrumento utiliza datos públicos, sintéticos, anonimizados o autorizados    | Evidencia de datos         |
| Existe una versión reproducible y documentada                                    | Archivo versionado         |
| Se registran observaciones de revisión académica o piloto, si se realiza         | Informe de revisión        |
| El diseño no depende de una plataforma específica                                | Formato independiente      |
| El diseño puede operar preferiblemente de forma local o con mínima transferencia | Ficha de arquitectura      |

Las métricas concretas de aceptación, si fueran necesarias, deberán definirse y validarse durante la fase de evaluación.

**[Pendiente de validación institucional]**: establecer quién realizará formalmente la revisión del instrumento y cuáles serán los criterios institucionales de aceptación.

---

# 13. Limitaciones

El desarrollo del proyecto presenta las siguientes limitaciones:

1. **Tiempo limitado del diplomado.** El instrumento debe mantenerse dentro de un alcance académico viable y no convertirse en una plataforma institucional completa.

2. **Disponibilidad de participantes.** La validación puede depender del número de estudiantes, docentes o asesores disponibles.

3. **Ausencia de datos reales autorizados.** La aplicación inicial deberá priorizar datos públicos, sintéticos, anonimizados o autorizados.

4. **Evolución tecnológica.** Los modelos, herramientas, dependencias y mecanismos de IA cambian con rapidez, por lo que el instrumento debe mantenerse independiente de tecnologías específicas.

5. **Diferencias de hardware.** Las capacidades locales pueden variar entre equipos, aspecto que el propio diplomado contempla mediante diferentes rutas de hardware. 

6. **Dependencia parcial de software de terceros.** Aunque el enfoque sea local, los proyectos pueden utilizar modelos, paquetes y herramientas externas cuya procedencia y licencia deberán documentarse.

7. **Ausencia de revisión jurídica formal.** El instrumento no sustituirá la revisión de especialistas jurídicos ni determinará por sí mismo el cumplimiento legal.

8. **Cobertura limitada de escenarios.** No será posible probar todas las posibles amenazas, vulnerabilidades o situaciones de uso.

9. **Subjetividad en la valoración de riesgos.** La probabilidad e impacto pueden variar según el contexto y deberán revisarse con criterios consistentes.

10. **Impactos de largo plazo.** El proyecto no contempla una evaluación de impactos sociales a gran escala.

11. **Adaptación institucional posterior.** Los campos, responsables y procedimientos deberán ajustarse si la institución cuenta con políticas o instrumentos propios.

---

# 14. Consideraciones éticas, legales y de privacidad

El proyecto deberá adoptar una postura de ingeniería responsable y considerar los siguientes principios.

## 14.1 Protección de datos personales

Los proyectos deberán priorizar datos públicos, sintéticos, anonimizados o expresamente autorizados. Cuando se traten datos personales deberán considerarse finalidad, autorización cuando corresponda, seguridad, confidencialidad, circulación restringida y derechos de los titulares. 

La **Ley 1581 de 2012** se utilizará como referente colombiano para la protección de datos personales, sin que el presente instrumento constituya una certificación de cumplimiento jurídico.

## 14.2 Procesamiento local

La ejecución local puede constituir una medida técnica para reducir transferencias innecesarias, pero no elimina las obligaciones jurídicas o éticas sobre los datos. 

Por tanto, “procesamiento local” no deberá interpretarse como sinónimo automático de “procesamiento seguro”.

## 14.3 Propiedad intelectual y licenciamiento

Los modelos, datasets, imágenes, audios y otros insumos deberán contar con procedencia y condiciones de uso conocidas. El documento base establece además la necesidad de diferenciar el uso académico de la explotación comercial y conservar créditos, atribuciones y metadatos cuando corresponda. 

## 14.4 Identidad y contenido sintético

El uso de imágenes, voces o rostros de personas deberá contar con consentimiento y propósito legítimo. Asimismo, los productos sintéticos deberán identificarse cuando su naturaleza pueda inducir a error. 

## 14.5 Supervisión humana

La automatización no deberá eliminar la responsabilidad humana. El diplomado establece que las acciones sensibles realizadas por agentes requieren controles y aprobación humana cuando corresponda. 

## 14.6 Verificación de resultados

Las salidas generadas por IA no deberán presentarse como hechos verificados sin comprobación independiente. Esta condición es particularmente importante en sistemas RAG, generación de contenido y aplicaciones que produzcan información destinada a terceros. 

---

# 15. Metodología preliminar

Se propone una metodología aplicada, progresiva y orientada a producto, coherente con el enfoque del diplomado, que conecta cada concepto con una decisión, práctica o evidencia verificable. 

| Fase                     | Actividades principales                                                      | Entregable                     |
| ------------------------ | ---------------------------------------------------------------------------- | ------------------------------ |
| 1. Revisión del contexto | Analizar el documento base, Módulo 1 y apartado 8.4                          | Documento de contextualización |
| 2. Diagnóstico           | Identificar actores, activos, datos, procesos y riesgos                      | Mapa de actores e inventario   |
| 3. Revisión conceptual   | Analizar NIST AI RMF, privacidad y referentes indicados en el documento base | Marco conceptual de trabajo    |
| 4. Diseño de matriz      | Definir campos, categorías, valoración y relación NIST                       | Matriz preliminar              |
| 5. Diseño del checklist  | Definir preguntas de privacidad, seguridad, licenciamiento y trazabilidad    | Checklist preliminar           |
| 6. Aplicación            | Utilizar el instrumento en un caso académico controlado                      | Caso diligenciado              |
| 7. Revisión              | Analizar dificultades, observaciones y posibles ajustes                      | Informe de revisión            |
| 8. Documentación         | Consolidar versión final, limitaciones y recomendaciones                     | Instrumento reproducible       |

La metodología seguirá el principio de que la práctica debe generar evidencia verificable y no limitarse a demostraciones o capturas de pantalla. 

---

# 16. Entregables

Los entregables propuestos son:

1. Documento de planteamiento del problema.
2. Objetivo general y objetivos específicos.
3. Mapa de actores.
4. Inventario de activos y datos.
5. Mapa básico de flujo de datos.
6. Matriz de riesgos de IA.
7. Checklist de privacidad.
8. Guía breve de diligenciamiento.
9. Caso de aplicación.
10. Informe de revisión o validación.
11. Registro de limitaciones.
12. Versión reproducible del instrumento.
13. Presentación o sustentación técnica.

Estos entregables son coherentes con la orientación del diplomado hacia productos documentados, reproducibles y sustentables técnicamente. El proyecto integrador debe contener problema, usuarios, alcance, requisitos, arquitectura, datos, evaluación, seguridad, privacidad, licencias y documentación. 

---

# 17. Conclusión del planteamiento

La incorporación de inteligencia artificial generativa en proyectos académicos requiere una perspectiva que supere el uso instrumental de modelos y considere los datos, modelos, herramientas, arquitectura, riesgos, controles, licencias, privacidad y responsabilidad humana como componentes integrales de la solución.

El diplomado IA 5.0 Lab establece esta orientación mediante su enfoque de ingeniería aplicada, local-first, sistemas RAG, agentes, aplicaciones multimodales y gobernanza tecnológica. Dentro de este marco, el apartado **8.4 Gobierno académico** identifica expresamente la necesidad de un formato de matriz de riesgos de IA y checklist de privacidad. 

El proyecto propuesto busca concretar esta necesidad mediante un instrumento académico estructurado que permita identificar y documentar riesgos, relacionarlos con las funciones Govern, Map, Measure y Manage del NIST AI RMF y verificar condiciones básicas de privacidad, seguridad, licenciamiento y trazabilidad.

Su alcance se limita deliberadamente a la formulación, especificación y aplicación controlada del instrumento. De esta manera, no se pretende sustituir las responsabilidades institucionales, jurídicas o humanas, sino proporcionar una herramienta que facilite la toma de decisiones informadas, la documentación técnica y la evaluación de proyectos académicos de inteligencia artificial.

La validación posterior permitirá determinar si la estructura propuesta responde adecuadamente a las necesidades del contexto institucional y qué ajustes serían necesarios para una eventual adopción más amplia.

---

# Verificación de coherencia del documento

| Comprobación                                                                   | Estado     | Observación                                                                                                            |
| ------------------------------------------------------------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------- |
| El problema corresponde al tema de matriz de riesgos y checklist de privacidad | **Cumple** | El problema se centra en la necesidad de estructurar ambos instrumentos.                                               |
| El objetivo general responde al problema                                       | **Cumple** | El objetivo propone diseñar la matriz y el checklist para fortalecer la gestión de riesgos.                            |
| Existen solo tres o cuatro objetivos específicos                               | **Cumple** | Se formularon cuatro objetivos específicos.                                                                            |
| Cada objetivo específico contribuye al objetivo general                        | **Cumple** | Los objetivos cubren diagnóstico, diseño y validación.                                                                 |
| El alcance es académico y viable                                               | **Cumple** | Se excluye explícitamente una plataforma institucional productiva.                                                     |
| Se identifican usuarios y partes interesadas                                   | **Cumple** | Se incluyen estudiantes, docentes, asesores, coordinación y demás actores relevantes.                                  |
| Se incluyen requisitos funcionales y no funcionales                            | **Cumple** | Se presentan requisitos funcionales, no funcionales y de privacidad/seguridad.                                         |
| Se incluye una matriz preliminar NIST AI RMF                                   | **Cumple** | Se presentan 12 riesgos asociados a Govern, Map, Measure y Manage.                                                     |
| Se incluye un checklist de privacidad                                          | **Cumple** | Se incluyen 40 verificaciones organizadas por etapas.                                                                  |
| Se incluyen criterios de éxito                                                 | **Cumple** | Se definieron criterios como metas a verificar, sin inventar resultados.                                               |
| Se incluyen limitaciones y fuera de alcance                                    | **Cumple** | Ambos apartados delimitan expresamente el proyecto.                                                                    |
| No se inventan resultados                                                      | **Cumple** | Las valoraciones de riesgo se presentan como propuestas preliminares y los resultados de validación quedan pendientes. |
| Se distingue entre información confirmada y pendiente de validar               | **Cumple** | Se utiliza “[Pendiente de validación institucional]” cuando corresponde.                                               |
| El documento es coherente con el Módulo 1                                      | **Cumple** | Se incorporan caracterización, actores, datos, flujos, arquitectura y matriz de riesgos.                               |
| El documento se relaciona con el apartado 8.4 “Gobierno académico”             | **Cumple** | El formato de matriz de riesgos y checklist de privacidad constituye el eje central del proyecto.                      |
| Se mantiene el proyecto como instrumento y no como plataforma institucional    | **Cumple** | La plataforma productiva queda explícitamente fuera del alcance.                                                       |
| Se evita presentar el instrumento como certificación legal                     | **Cumple** | Se establece expresamente que no sustituye la revisión jurídica.                                                       |
| Se evita incluir entrenamiento de modelos fundacionales                        | **Cumple** | No se contempla dentro del alcance ni de los entregables.                                                              |
| Se contempla procesamiento local, híbrido y remoto                             | **Cumple** | Se incorpora en el mapa de flujo, requisitos y criterios de arquitectura.                                              |
| Se considera supervisión humana                                                | **Cumple** | Se incorpora en riesgos, requisitos, checklist y consideraciones éticas.                                               |
| Se considera trazabilidad de modelos, datos y decisiones                       | **Cumple** | Se incluye en requisitos, matriz, checklist y criterios de éxito.                                                      |

**Aspectos que permanecen pendientes de validación institucional:** existencia de instrumentos previos equivalentes, responsables institucionales específicos, procedimiento formal de revisión o aprobación de proyectos de IA y criterios institucionales definitivos para la validación del instrumento.
