# 1. Planteamiento del problema

La gestión de una cafetería implica un flujo continuo de información: productos ofrecidos, pedidos atendidos, ventas, consumo de insumos, compras a proveedores, gastos e ingresos. De manera preliminar, se presume que el establecimiento objeto de estudio registra buena parte de esta información de forma manual en cuadernos físicos. Esta práctica es habitual en negocios pequeños por su bajo costo y familiaridad, pero puede limitar la capacidad de consulta, consolidación y análisis a medida que crece el volumen de operaciones. **El tipo de información registrada, su estructura y su frecuencia deben validarse mediante entrevista [Pendiente de validación con la administradora].**

Entre los problemas potenciales del registro exclusivamente manual podría encontrarse la dificultad para consultar información histórica y para buscar datos específicos, pues la localización de un registro depende de la revisión página por página. Asimismo, podría presentarse demora en consolidar ventas, compras, gastos o inventario, lo que dificultaría generar reportes oportunos y apoyar decisiones sobre qué productos mantener, qué insumos reponer o cuándo comprar. Estas son hipótesis iniciales, no hallazgos confirmados.

También podrían existir riesgos asociados a la calidad y la integridad de los registros: errores de transcripción, omisiones, duplicación de anotaciones o cálculos manuales inconsistentes. A ello se suma la posible falta de trazabilidad sobre los cambios realizados, pues en un cuaderno físico resulta difícil determinar quién modificó un dato, cuándo y por qué. **Se presume que estas situaciones pueden darse, pero su existencia, frecuencia e impacto deben verificarse con la administradora [Pendiente de validación con la administradora].**

Desde la perspectiva de la continuidad operativa, el conocimiento contenido en los cuadernos podría depender de una sola persona, lo que generaría vulnerabilidad ante ausencias, rotación o cambios de responsabilidades. Adicionalmente, los registros físicos están expuestos a pérdida, deterioro, humedad o daño accidental, y podrían carecer de copia de respaldo. Finalmente, el acceso a los cuadernos podría no estar controlado, lo que plantea un riesgo de consulta o alteración no autorizada de información comercial. Todas estas condiciones son **hipótesis iniciales que deben validarse mediante entrevista con la administradora de la cafetería.**

Frente a este escenario, se propone explorar una solución **local y de fácil uso** que permita digitalizar y organizar gradualmente la información que la cafetería priorice, manteniendo el control de los datos dentro de su propia infraestructura. La propuesta no depende de servicios en la nube ni de APIs externas de inteligencia artificial, y debería poder operar sin conexión permanente a Internet. Dado que los usuarios podrían tener conocimientos tecnológicos limitados, la interfaz deberá ser sencilla, con lenguaje claro y procesos guiados.

Como componente complementario, se contempla evaluar el uso de un modelo de lenguaje local pequeño o mediano para apoyar consultas en lenguaje natural, resúmenes y borradores de reportes sobre información previamente registrada y autorizada. La inteligencia artificial no sustituirá a la administradora, al control de caja ni a la contabilidad profesional, y no modificará información sensible sin validación humana explícita. De forma paralela, se evaluará la viabilidad de adoptar o integrar un ERP gratuito o de código abierto, como Odoo Community Edition u otra alternativa, lo cual constituye una opción por validar. La decisión entre construir una solución propia, adaptar un ERP o integrar ambos enfoques dependerá del levantamiento de información, los requisitos, los costos, el hardware disponible, la facilidad de uso y la capacidad de mantenimiento.

**Pregunta orientadora del proyecto:**

¿Cómo diseñar una solución local de automatización para una cafetería que permita digitalizar, organizar, consultar y apoyar el seguimiento de sus procesos operativos y administrativos, reduciendo la dependencia de registros manuales en cuadernos, manteniendo el control local de la información y garantizando la supervisión humana de las operaciones relevantes?

---

# 2. Matriz preliminar de riesgos NIST AI RMF

La siguiente matriz es una **versión preliminar, elaborada antes de la entrevista con la administradora**. Los riesgos se formulan como eventos potenciales o condiciones por validar, no como hechos ocurridos. La matriz deberá ajustarse cuando se conozcan los procesos reales, los datos tratados, los usuarios y la infraestructura de la cafetería.

El NIST AI Risk Management Framework (AI RMF 1.0) organiza la gestión de riesgos de sistemas de IA en cuatro funciones: **Govern** (cultura, políticas, roles y responsabilidades), **Map** (contexto, usuarios y riesgos potenciales), **Measure** (análisis, evaluación y seguimiento de riesgos) y **Manage** (priorización y tratamiento). Aquí se emplean como eje de organización de los riesgos del sistema completo, incluyendo los componentes no basados en IA.

## Escala preliminar

| Dimensión | Valores |
|---|---|
| Probabilidad | Baja, Media, Alta |
| Impacto | Bajo, Medio, Alto |
| Nivel de riesgo | Bajo, Medio, Alto, Crítico |
| Estado | Por validar, Pendiente de mitigación, Mitigado parcialmente, Aceptado con control |

*Criterio orientativo del nivel:* Alta probabilidad con impacto Alto se considera Crítico; combinaciones Alta–Medio o Media–Alto, Alto; combinaciones Media–Medio, Baja–Alto o Alta–Bajo, Medio; las demás, Bajo. Esta asignación es una estimación académica inicial, no una medición.

## Matriz

| ID | Función NIST AI RMF | Categoría | Riesgo | Causa o condición | Consecuencia potencial | Probabilidad | Impacto | Nivel | Control o mitigación inicial | Responsable propuesto | Estado |
|---|---|---|---|---|---|---|---|---|---|---|---|
| R-01 | Govern | Gobernanza y responsabilidades | Ausencia de responsables definidos para registrar información y aprobar cambios | Podría no existir una asignación formal de roles sobre ventas, caja, inventario y compras [Pendiente de validación con la administradora] | Cambios sin autorización, registros contradictorios, imposibilidad de atribuir responsabilidades | Media | Alto | Alto | Definir matriz de roles y aprobaciones; registrar usuario, fecha y motivo de cada cambio | Administradora (con equipo académico) | Por validar |
| R-02 | Govern | Datos y privacidad | Registro de datos personales de clientes o empleados sin finalidad o autorización clara | Podrían existir registros de clientes o turnos sin criterios de tratamiento [Pendiente de validación con la administradora] | Incumplimiento de normativa de protección de datos; pérdida de confianza | Media | Alto | Alto | Clasificar la información; registrar solo datos necesarios; documentar finalidad; usar datos sintéticos o anonimizados en la fase académica | Administradora / Propietario(a) | Por validar |
| R-03 | Govern | Datos y privacidad | Exposición de información por uso no autorizado de servicios externos (nube, APIs de IA, mensajería) | Usuarios podrían compartir datos con herramientas externas por comodidad | Fuga de información comercial o personal; incumplimiento del enfoque local-first | Media | Alto | Alto | Política de no envío a servicios externos; bloquear conexiones de salida de la aplicación; capacitación | Equipo académico / Administradora | Pendiente de mitigación |
| R-04 | Manage | Seguridad de la información | Acceso no autorizado a ventas, gastos, inventario o datos de empleados; contraseñas débiles o cuentas compartidas | Podría usarse un equipo compartido o una sola cuenta [Pendiente de validación con la administradora] | Consulta o alteración indebida; imposibilidad de auditar acciones | Alta | Alto | Crítico | Cuentas individuales, roles con mínimo privilegio, política de contraseñas, bloqueo de sesión, registro de auditoría | Equipo académico (diseño) / Administradora (gestión de cuentas) | Pendiente de mitigación |
| R-05 | Measure | Calidad e integridad de datos | Errores de digitación y registros incompletos, inconsistentes o desactualizados | Digitación manual, falta de validaciones, captura tardía de datos | Reportes y consultas incorrectas; decisiones basadas en datos erróneos | Alta | Medio | Alto | Validaciones de formato y rango, campos obligatorios, mecanismo de corrección con trazabilidad, revisión periódica | Personal operativo / Administradora | Pendiente de mitigación |
| R-06 | Manage | Operación y continuidad | Pérdida o alteración de información al pasar del cuaderno al sistema | Transcripción parcial, interpretación de caligrafía, omisión de páginas | Series históricas incompletas; discrepancias entre cuaderno y sistema | Media | Medio | Medio | Migración acotada a un conjunto de prueba autorizado; conciliación por muestreo; conservar los cuadernos originales | Equipo académico con apoyo de la administradora | Por validar |
| R-07 | Manage | Operación y continuidad | Falta de respaldo de la información digitalizada | Podría no existir cultura ni procedimiento de copias de seguridad [Pendiente de validación con la administradora] | Pérdida irrecuperable de datos por falla de disco, borrado o incidente | Media | Alto | Alto | Respaldos locales periódicos, protegidos y con prueba de restauración; asignar responsable de revisión | Responsable técnico designado / Administradora | Pendiente de mitigación |
| R-08 | Measure | Modelo de IA local | Respuestas o resúmenes erróneos, incompletos o inventados por el modelo local | Limitaciones de modelos pequeños cuantizados, calidad del español, ausencia de contexto suficiente | Interpretaciones equivocadas sobre ventas, inventario o compras | Alta | Medio | Alto | Restringir el asistente a datos autorizados; mostrar las fuentes consultadas; pruebas con casos de verificación; pruebas del modelo antes de seleccionarlo | Equipo académico | Pendiente de mitigación |
| R-09 | Measure | Modelo de IA local | Confianza excesiva de los usuarios en reportes generados por IA | Percepción de que la salida automatizada es siempre correcta | Decisiones de compra, precio o caja sin verificación | Media | Alto | Alto | Advertencias visibles; los reportes de IA se etiquetan como borradores sujetos a verificación humana | Administradora / Equipo académico | Pendiente de mitigación |
| R-10 | Manage | Riesgos de automatización | Modificación automática de datos (ventas, caja, inventario, precios, usuarios) sin aprobación humana | Concesión de permisos de escritura a la IA o a herramientas automatizadas | Alteraciones no detectadas, errores en cadena, pérdida de trazabilidad | Baja | Alto | Medio | Permisos de solo lectura para la IA; confirmación humana explícita para cualquier creación, edición o eliminación | Equipo académico (diseño) / Administradora (aprobación) | Pendiente de mitigación |
| R-11 | Map | Integración con ERP o sistema administrativo | Integración inadecuada con un ERP gratuito o con Odoo Community Edition | Incompatibilidades, módulos no disponibles en la edición evaluada, complejidad de configuración [Por validar] | Retrabajo, datos duplicados, sistema difícil de mantener | Media | Medio | Medio | Evaluación comparativa previa y prueba de concepto acotada; documentar decisión; no asumir selección | Equipo académico / Docente asesor | Por validar |
| R-12 | Govern | Integración con ERP o sistema administrativo | Crecimiento del alcance hacia una implementación completa de ERP no viable en el tiempo académico | Ampliación progresiva de requisitos (contabilidad, nómina, facturación) | Proyecto inconcluso o de baja calidad; incumplimiento del cronograma | Alta | Medio | Alto | Definir alcance incremental, lista de exclusiones y control formal de cambios | Equipo académico / Docente asesor | Pendiente de mitigación |
| R-13 | Manage | Infraestructura y hardware | Equipo insuficiente, fallas de almacenamiento, cortes de energía o falta de mantenimiento | Hardware de capacidad limitada o sin protección eléctrica [Pendiente de validación con la administradora] | Lentitud, corrupción de datos, interrupciones | Media | Alto | Alto | Dimensionamiento tras pruebas; SSD; UPS recomendada; plan básico de mantenimiento | Equipo académico / Administradora | Por validar |
| R-14 | Map | Dependencias, licencias y software | Licencias, módulos o dependencias incompatibles con uso comercial o académico | Modelos de IA, bibliotecas o ERP con condiciones de uso distintas o cambiantes | Restricciones legales o necesidad de rediseñar componentes | Media | Medio | Medio | Inventariar licencias y procedencia; verificar condiciones de uso comercial antes de adoptar | Equipo académico | Por validar |
| R-15 | Govern | Usuarios y experiencia de uso | Falta de capacitación y dependencia de una única persona para operar el sistema | Usuarios con conocimientos tecnológicos limitados; conocimiento concentrado | Uso incorrecto, abandono del sistema, interrupción si la persona no está disponible | Alta | Medio | Alto | Interfaz guiada, manual básico, sesiones de capacitación, al menos un suplente capacitado | Administradora / Equipo académico | Pendiente de mitigación |
| R-16 | Manage | Riesgos económicos y de control de caja | Discrepancias de caja o decisiones financieras apoyadas solo en reportes del sistema | Digitalización incompleta, errores de registro o interpretación de reportes como sustituto del arqueo | Diferencias monetarias no detectadas; decisiones de compra mal fundamentadas | Media | Alto | Alto | Mantener arqueo y validación humana; el sistema se presenta como apoyo, no como contabilidad certificada | Personal de caja / Administradora | Por validar |

## Interpretación preliminar

Los riesgos que parecen prioritarios para investigar en la entrevista son los relacionados con **control de acceso y responsabilidades (R-01, R-04)**. Conviene averiguar quién registra y quién autoriza cambios, cuántas personas acceden a los cuadernos o al equipo, y si existen cuentas o dispositivos compartidos. De estas respuestas depende el diseño de roles y de la auditoría.

Un segundo grupo se refiere a **continuidad y calidad de los datos (R-05, R-06, R-07, R-13)**. Debe indagarse cómo se registran hoy las operaciones, cuáles cuadernos son críticos, si existe algún respaldo y cuál es el equipo y las condiciones de energía disponibles. Esto permitirá definir el conjunto mínimo de datos a digitalizar y el esquema de copias de seguridad.

Un tercer grupo corresponde a los **riesgos específicos de la IA local (R-08, R-09, R-10)** y a la **protección de datos personales (R-02, R-03)**. Es necesario conocer si se registran datos de clientes o empleados, qué tipo de consultas haría realmente útil un asistente y qué decisiones no deberían apoyarse en él. También conviene identificar la actitud de los usuarios hacia herramientas de IA, para calibrar advertencias y límites.

Finalmente, la entrevista debe aclarar las **expectativas de alcance (R-11, R-12, R-14, R-15, R-16)**: qué procesos desea priorizar la administradora, si el ERP es realmente una necesidad o una expectativa, qué nivel de capacitación es viable y cómo se maneja hoy el control de caja. Esto evitará un alcance desproporcionado respecto al tiempo académico.

---

# 3. Usuarios y partes interesadas

La siguiente identificación es preliminar. No se presumen nombres ni cargos no confirmados.

| Grupo o usuario | Rol preliminar | Necesidad o interés | Interacción esperada con la solución | Información o permisos que podría requerir | Aspectos pendientes de validar |
|---|---|---|---|---|---|
| Administradora de la cafetería | Responsable principal de la operación y fuente prioritaria de información | Consultar información consolidada, apoyar el control y obtener reportes | Consulta, revisión, aprobación de cambios y uso del asistente local | Acceso amplio de consulta; aprobación de cambios; gestión de usuarios [Pendiente de validación con la administradora] | Procesos que gestiona, volumen de información, nivel de familiaridad tecnológica |
| Personal de atención o ventas | Posible registro de pedidos y ventas | Registrar rápido y sin errores | Captura sencilla de ventas o pedidos | Registro de ventas; consulta limitada de productos [Pendiente de validación con la administradora] | Si existe este rol, cómo registra hoy y con qué frecuencia |
| Personal responsable de caja, si existe | Posible control de ingresos y cierres | Cuadrar caja y disponer de soportes | Registro de movimientos y consulta de cierres | Registro y consulta de caja; sin permisos de eliminación | Si existe el rol, y quién autoriza correcciones |
| Personal responsable de inventario o compras, si existe | Posible control de insumos y pedidos a proveedores | Conocer existencias y planificar compras | Registro de entradas y salidas; consulta de existencias | Gestión de inventario y compras [Pendiente de validación con la administradora] | Quién decide compras, qué insumos se controlan |
| Propietario(a) o responsable del negocio, si existe | Posible decisor estratégico | Visión general del negocio y control de la información | Consulta de reportes | Reportes de alto nivel [Pendiente de validación con la administradora] | Si es persona distinta de la administradora y qué información requiere |
| Proveedores (solo si se registran compras o pedidos) | Contrapartes externas | Pedidos y pagos claros | Sin acceso directo; se registran como entidades | Datos básicos de contacto y productos | Si es necesario registrarlos y con qué datos personales |
| Equipo académico desarrollador | Diseño, desarrollo, pruebas y documentación | Entregar una solución viable y documentada | Desarrollo, configuración y mantenimiento durante el proyecto | Acceso técnico limitado a datos de ejemplo, anonimizados o autorizados | Distribución de roles, tiempos, acuerdos de confidencialidad |
| Docente o asesor del proyecto | Orientación académica y evaluación | Rigor técnico y alineación con el diplomado | Revisión de entregables y retroalimentación | Acceso a documentación y demostraciones | Criterios de evaluación y calendario |
| Personal externo de soporte técnico, si llega a requerirse | Apoyo en mantenimiento posterior | Contar con documentación para dar soporte | Intervención excepcional | Acceso temporal y controlado, bajo supervisión | Si será necesario y quién asumirá el costo y la autorización |

La administradora será una **fuente prioritaria de levantamiento de información**. La entrevista permitirá validar roles, permisos, procesos, vocabulario propio del negocio y necesidades reales, y con ello ajustar esta tabla y los requisitos posteriores.

---

# 4. Alcance

El alcance se define como una propuesta académica, incremental y viable. Su definición final dependerá del levantamiento de información.

## 4.1 Incluye

- Levantamiento inicial de información mediante entrevista con la administradora.
- Identificación de procesos prioritarios y de los registros manuales más relevantes.
- Diseño de una solución local para digitalizar información seleccionada.
- Gestión básica de usuarios y roles.
- Registro y consulta de información priorizada, sujeto a validación.
- Inventario básico, ventas, compras, gastos o caja, únicamente si la entrevista lo confirma [Pendiente de validación con la administradora].
- Generación de reportes básicos.
- Copias de seguridad locales.
- Asistente de IA local para consultas y resúmenes, sin modificar registros automáticamente.
- Documentación técnica y manual básico de uso.
- Matriz de riesgos, controles iniciales y recomendaciones.
- Evaluación preliminar de viabilidad de un ERP gratuito, como Odoo Community Edition u otra alternativa de código abierto.
- Pruebas con datos de ejemplo, sintéticos, anonimizados o expresamente autorizados.

## 4.2 Fuera de alcance

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

| Supuesto o dependencia | Estado inicial | Acción requerida para validarlo |
|---|---|---|
| Disponibilidad de un computador local | Por validar | Consultar qué equipo existe, sus características y quién lo usa |
| Electricidad y condiciones básicas de seguridad física | Por validar | Verificar estabilidad eléctrica, ubicación del equipo y control de acceso al espacio |
| Acceso autorizado a registros de ejemplo | Por validar | Acordar con la administradora qué registros pueden usarse, anonimizados o sintéticos |
| Tiempo de la administradora para entrevista y validación | Por validar | Programar entrevista y sesiones breves de validación |
| Disposición del personal para aprender a usar el sistema | Por validar | Explorar actitudes y disponibilidad en la entrevista |
| Existencia de procesos repetitivos que puedan digitalizarse | Por validar | Documentar procesos actuales y priorizarlos |
| Compatibilidad de Odoo Community Edition u otra alternativa con el entorno disponible | Por validar | Revisar requisitos técnicos oficiales y realizar prueba de concepto acotada |
| Disponibilidad de respaldo local | Por validar | Verificar si existe unidad externa o NAS, o si debe adquirirse |
| Información clara sobre quién autoriza cambios en ventas, caja, inventario y compras | Por validar | Levantar el flujo de autorización en la entrevista |

---

# 5. Requisitos

Los requisitos son **preliminares**. Los que dependen de la entrevista se marcan como [Pendiente de validación].

## 5.1 Requisitos funcionales

| Código | Requisito funcional | Prioridad | Estado de validación | Evidencia de aceptación |
|---|---|---|---|---|
| RF-01 | Permitir registrar y consultar información operativa priorizada de la cafetería | Alta | [Pendiente de validación] | Registro y consulta exitosa de datos de ejemplo del flujo priorizado |
| RF-02 | Permitir crear cuentas de usuario con roles básicos | Alta | Propuesta preliminar | Creación de usuarios con distintos permisos y verificación de restricciones |
| RF-03 | Permitir registrar cambios con fecha, usuario responsable y motivo cuando aplique | Alta | Propuesta preliminar | Bitácora de cambios consultable |
| RF-04 | Permitir registrar productos e insumos | Media | [Pendiente de validación] | Alta, consulta y edición de productos o insumos de ejemplo |
| RF-05 | Permitir registrar entradas y salidas de inventario | Media | [Pendiente de validación] | Movimientos registrados y existencias consistentes con datos de prueba |
| RF-06 | Permitir registrar ventas básicas | Media | [Pendiente de validación] | Registro de ventas de ejemplo y consulta por fecha |
| RF-07 | Permitir registrar compras, gastos o proveedores | Media | [Pendiente de validación] | Registro y consulta de compras o gastos de ejemplo |
| RF-08 | Permitir consultar registros históricos mediante filtros básicos | Alta | Propuesta preliminar | Consultas por fecha, tipo o producto con resultados verificables |
| RF-09 | Permitir generar reportes simples de la información registrada | Media | Propuesta preliminar | Reporte diario o semanal generado y contrastado con los datos de origen |
| RF-10 | Permitir realizar copias de seguridad locales | Alta | Propuesta preliminar | Copia generada y verificada |
| RF-11 | Permitir al asistente de IA local responder consultas basadas únicamente en información autorizada | Media | Propuesta preliminar | Respuestas contrastadas con los datos y rechazo de consultas fuera de permisos |
| RF-12 | Exigir confirmación humana antes de que una herramienta automatizada cree, modifique o elimine registros | Alta | Propuesta preliminar | Prueba que demuestre que ninguna escritura se ejecuta sin confirmación explícita |
| RF-13 | Permitir registrar incidencias, observaciones o correcciones | Media | Propuesta preliminar | Corrección registrada con trazabilidad del dato original |
| RF-14 | Permitir exportar información básica a un formato local, como CSV o PDF | Baja | [Pendiente de validación] | Archivo exportado legible y coherente con los datos |
| RF-15 | Permitir evaluar de manera comparativa la viabilidad de un ERP gratuito, como Odoo Community Edition, frente a una solución propia o simplificada | Media | Propuesta preliminar | Informe comparativo con criterios de costo, complejidad, hardware y mantenimiento |

## 5.2 Requisitos no funcionales

| Código | Requisito no funcional | Prioridad | Criterio verificable |
|---|---|---|---|
| RNF-01 | Operar localmente sin depender de la nube | Alta | Funcionamiento de las funciones básicas con la red externa desconectada |
| RNF-02 | Ofrecer una interfaz sencilla y comprensible para usuarios no técnicos | Alta | Un usuario de prueba completa el flujo priorizado con instrucciones básicas |
| RNF-03 | Mantener un bajo consumo de recursos | Media | Medición de CPU, RAM y disco durante operaciones habituales |
| RNF-04 | Proteger el acceso mediante cuentas y contraseñas individuales | Alta | Inexistencia de cuentas compartidas y verificación de autenticación |
| RNF-05 | Registrar auditoría de cambios relevantes | Alta | Bitácora con usuario, fecha y acción |
| RNF-06 | Realizar respaldos locales periódicos | Alta | Procedimiento documentado y copia reciente verificable |
| RNF-07 | Permitir recuperación básica ante fallos | Alta | Restauración de una copia en entorno de prueba |
| RNF-08 | Ser mantenible | Media | Código estructurado y documentado |
| RNF-09 | Contar con documentación | Media | Manual de usuario y README técnico entregados |
| RNF-10 | Usar control de versiones del código | Media | Repositorio con historial de cambios |
| RNF-11 | Ofrecer un tiempo de respuesta adecuado en operaciones básicas | Media | Tiempos medidos y registrados en el equipo de prueba (umbral por definir) |
| RNF-12 | Ser compatible con equipos de recursos moderados | Alta | Pruebas en el hardware disponible |
| RNF-13 | Permitir actualización controlada de software y modelos | Media | Procedimiento documentado, con registro de versiones |
| RNF-14 | Garantizar la seguridad de los datos locales | Alta | Permisos de archivos y protección de la base de datos y de los respaldos |
| RNF-15 | No almacenar claves dentro del código ni de repositorios | Alta | Revisión del repositorio sin credenciales |
| RNF-16 | Asegurar la trazabilidad de los resultados generados por IA | Media | Registro de consulta, fecha, modelo utilizado y fuentes de datos |
| RNF-17 | Restringir los permisos del modelo de IA y de cualquier agente o herramienta | Alta | Pruebas que confirmen acceso de solo lectura a datos autorizados |

## 5.3 Requisitos de privacidad, seguridad y gobierno de IA

| Código | Requisito de seguridad, privacidad o gobierno | Evidencia esperada | Estado |
|---|---|---|---|
| RPG-01 | Clasificar la información antes de registrarla en el sistema | Esquema de clasificación documentado | Propuesta preliminar |
| RPG-02 | Registrar la finalidad de los datos personales, si estos llegan a tratarse | Registro de finalidad por tipo de dato | [Pendiente de validación con la administradora] |
| RPG-03 | Usar datos de ejemplo, anonimizados o autorizados durante la fase académica | Constancia de origen de los datos de prueba | Propuesta preliminar |
| RPG-04 | Restringir accesos según el rol | Matriz de roles y pruebas de acceso | Propuesta preliminar |
| RPG-05 | Mantener copias de seguridad locales protegidas | Procedimiento y verificación de acceso a respaldos | Propuesta preliminar |
| RPG-06 | Evitar enviar datos a servicios externos | Configuración documentada sin conexiones salientes de la aplicación | Propuesta preliminar |
| RPG-07 | Registrar la versión del modelo local utilizado | Ficha de modelo con nombre y versión | Propuesta preliminar |
| RPG-08 | Documentar licencia y procedencia del modelo, ERP, bibliotecas y dependencias | Inventario de licencias | Propuesta preliminar |
| RPG-09 | No permitir que la IA modifique registros sin aprobación humana | Pruebas de confirmación obligatoria | Propuesta preliminar |
| RPG-10 | Validar resultados o reportes de IA antes de usarlos para decisiones | Etiquetado de borrador y registro de revisión | Propuesta preliminar |
| RPG-11 | Mantener un mecanismo para corregir información | Procedimiento de corrección con trazabilidad | Propuesta preliminar |
| RPG-12 | Proteger las credenciales de acceso | Almacenamiento seguro (hash) y política de contraseñas | Propuesta preliminar |
| RPG-13 | Contar con un procedimiento básico para reportar incidentes o pérdida de información | Documento de procedimiento | Propuesta preliminar |
| RPG-14 | Definir un responsable de revisar respaldos, permisos y cambios importantes | Designación formal documentada | [Pendiente de validación con la administradora] |

---

# 6. Criterios de éxito

Las metas se formulan como acciones por comprobar. No se presumen resultados.

| Código | Criterio de éxito | Indicador o evidencia | Meta propuesta | Estado inicial |
|---|---|---|---|---|
| CE-01 | Entrevista realizada con la administradora | Acta o guion con hallazgos | Realizar una entrevista semiestructurada y documentar hallazgos | Pendiente |
| CE-02 | Procesos prioritarios identificados y documentados | Descripción de procesos | Documentar al menos un flujo operativo prioritario | Pendiente |
| CE-03 | Usuarios y permisos definidos | Matriz de roles y permisos | Definir roles básicos y validarlos con la administradora | Pendiente |
| CE-04 | Registros manuales prioritarios identificados | Inventario de cuadernos y datos | Identificar los registros de mayor relevancia para la fase inicial | Pendiente |
| CE-05 | Prototipo o solución local funcional | Demostración | Demostrar el flujo priorizado de extremo a extremo con datos de ejemplo | Pendiente |
| CE-06 | Registro y consulta de información priorizada | Pruebas de registro y consulta | Verificar el registro y consulta de los datos del flujo priorizado | Pendiente |
| CE-07 | Copia de seguridad local probada | Evidencia de ejecución | Ejecutar una copia de seguridad local y verificar su disponibilidad | Pendiente |
| CE-08 | Restauración o verificación de integridad del respaldo | Informe de prueba | Restaurar la copia en un entorno de prueba o verificar su integridad | Pendiente |
| CE-09 | Asistente de IA local limitado a consultas autorizadas | Pruebas de consulta y de restricción | Comprobar que responde solo con datos autorizados y sin permisos de escritura | Pendiente |
| CE-10 | Confirmación humana para cambios críticos | Casos de prueba | Verificar que ninguna modificación crítica se ejecuta sin confirmación | Pendiente |
| CE-11 | Matriz de riesgos elaborada, revisada y con controles documentados | Matriz actualizada | Aplicar la matriz a la propuesta tecnológica y documentar controles de los riesgos prioritarios | Preliminar elaborada |
| CE-12 | Pruebas con datos autorizados, sintéticos o anonimizados | Registro de pruebas | Ejecutar pruebas únicamente con datos de estas categorías | Pendiente |
| CE-13 | Manual básico de usuario y documentación técnica | Documentos entregados | Entregar manual básico, README técnico y registro de versiones | Pendiente |
| CE-14 | Evaluación preliminar de viabilidad de Odoo Community Edition u otra alternativa, y retroalimentación de la administradora o usuario principal | Informe comparativo y comentarios cualitativos | Documentar la evaluación y obtener retroalimentación cualitativa de al menos un usuario clave, si está disponible | Pendiente |

---

# 7. Tecnología e infraestructura requerida

La infraestructura se plantea como **local-first**, general y escalable. No se afirma que exista actualmente. Las especificaciones son propuestas iniciales; la definición final dependerá de:

- La cantidad de usuarios simultáneos.
- El volumen de registros.
- El uso real de IA local.
- La implementación o no de un ERP como Odoo Community Edition.
- El sistema operativo disponible.
- La disponibilidad de respaldo local.
- La entrevista con la administradora.
- Las pruebas de rendimiento.

| Componente | Mínimo viable | Recomendado | Justificación | Pendiente de validar |
|---|---|---|---|---|
| Procesador | CPU moderna de 4 núcleos o superior | CPU moderna de 6 a 8 núcleos | La inferencia en CPU y los servicios locales requieren capacidad de cómputo | Equipo existente |
| Memoria RAM | 16 GB | 32 GB | Convivencia de base de datos, aplicación, posible ERP ligero y modelo pequeño o mediano cuantizado | Uso real de IA y ERP |
| Almacenamiento principal | Al menos 256 GB disponibles | 512 GB o superior | Sistema, datos, modelos y registros | Volumen de datos y tamaño de modelos |
| Tipo de almacenamiento | SSD | SSD NVMe | Velocidad y fiabilidad frente a discos mecánicos | Disponibilidad |
| Sistema operativo | Linux o Windows, según compatibilidad y soporte | Igual, priorizando el de mejor soporte local | Facilidad de mantenimiento y compatibilidad de herramientas | SO disponible y habilidades del equipo |
| Red local | Red estable si hay varios equipos | Red Gigabit si hay más de un equipo conectado | Acceso a la aplicación local desde otros equipos | Cantidad de equipos |
| Equipo cliente | Navegador moderno en equipo existente | Equipo dedicado a caja o atención, si se requiere | Interfaz web local | Equipos y número de usuarios |
| Servidor local o equipo principal | Un único equipo que aloja aplicación y datos | Equipo principal dedicado | Centralizar datos bajo control del negocio | Ubicación y seguridad física |
| Sistema de respaldo | Unidad externa o NAS básico | Disco externo adicional o NAS, con copia protegida | Evitar pérdida por falla de disco | Responsable y frecuencia |
| Fuente de energía o UPS | Protección básica si es posible | UPS para el equipo principal | Evitar corrupción por cortes de energía | Estabilidad eléctrica |
| Seguridad física | Ubicación con acceso controlado | Equipo en espacio restringido | Reducir acceso físico no autorizado | Distribución del local |
| Monitor, teclado, mouse e impresora | Periféricos básicos; impresora solo si se requiere | Periféricos adecuados al puesto de trabajo | Operación cotidiana | Necesidad de impresión |
| GPU | No obligatoria | Opcional; 6 a 8 GB de VRAM pueden acelerar la inferencia | La solución debe funcionar con CPU y modelos pequeños cuantizados | Rendimiento medido en CPU |
| Modelo de IA local | Modelo pequeño cuantizado para consultas y resúmenes simples | Modelo pequeño o mediano cuantizado, tras pruebas | Equilibrio entre calidad, memoria y velocidad | Idioma español, licencia, memoria y calidad |
| Motor de inferencia local | Ollama, GPT4All, LM Studio, llama.cpp o equivalente | Igual, según pruebas | Ejecución local sin servicios externos | Facilidad de instalación y mantenimiento |
| Base de datos local | SQLite para prototipo monousuario | PostgreSQL o MariaDB para varios usuarios | Simplicidad frente a concurrencia y robustez | Número de usuarios simultáneos |
| Interfaz de usuario | Aplicación web local sencilla | Interfaz web con flujos guiados | Facilidad de uso para personal no técnico | Preferencias de los usuarios |
| Herramientas de desarrollo y mantenimiento | Python y entorno de desarrollo básico | Entornos virtuales, pruebas y registro de dependencias | Reproducibilidad y mantenimiento | Conocimientos del equipo |
| ERP gratuito o de código abierto | No incluido por defecto | Odoo Community Edition u otro, solo si se valida | Evaluar frente a la solución propia sin asumir selección | Necesidades, complejidad, licencia, compatibilidad y mantenimiento |
| Control de versiones | Git local | Git local o repositorio privado | Trazabilidad del código y la documentación | Política de acceso |
| Seguridad y autenticación | Cuentas individuales y contraseñas protegidas | Autenticación local, roles y registro de auditoría | Control de acceso y trazabilidad | Número de usuarios y roles |

## Tecnologías candidatas

No se impone una única decisión; la selección final dependerá de pruebas y del levantamiento de información.

- **Backend:** Python con FastAPI, Flask o alternativa equivalente.
- **Base de datos:** SQLite para un prototipo monousuario; PostgreSQL o MariaDB para varios usuarios.
- **Interfaz:** aplicación web local sencilla, por ejemplo con Streamlit, Gradio, Flask, FastAPI con frontend web u otra alternativa equivalente.
- **IA local:** Ollama, GPT4All, LM Studio, llama.cpp o alternativa equivalente.
- **Modelo local:** modelo pequeño o mediano cuantizado, seleccionado tras pruebas de memoria, velocidad, calidad en español y licencia.
- **ERP:** Odoo Community Edition u otro ERP gratuito o de código abierto, únicamente después de validar necesidades, complejidad, costos de mantenimiento, condiciones de licencia y compatibilidad. Una implementación completa de ERP puede exceder el alcance académico inicial, por lo que debe distinguirse de la automatización operativa básica.
- **Copias de seguridad:** respaldo cifrado o protegido en disco externo, NAS local o sistema equivalente.
- **Control de versiones:** Git local o repositorio privado.
- **Documentación:** manual de usuario, README técnico, registro de versiones y bitácora de cambios.

**Aclaración:** no se recomienda iniciar con modelos grandes, modelos multimodales pesados, entrenamiento de IA, video, imágenes generativas, 3D, integración con nube ni automatizaciones autónomas de alto impacto. La conexión a Internet solo se contempla de forma excepcional para la instalación inicial o la descarga de actualizaciones, paquetes o modelos, y no como requisito del funcionamiento cotidiano.
