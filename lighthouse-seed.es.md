> Traducción comunitaria (borrador) — Política P2-002 de NTARI, Difusión Multilingüe Global. Fuente: lighthouse-seed.md (original en inglés, instantánea del 2026-07-29). Borrador comunitario asistido por máquina, pendiente de revisión por mantenedores regionales conforme a P2-002 §3.1. Las especificaciones técnicas centrales permanecen en inglés conforme a §2.2.
>
> ¿Encontraste un error en esta traducción? Tu corrección es una contribución
> bienvenida y valorada: haz un fork del repositorio y abre un pull request en
> https://github.com/NTARI-RAND/lighthouse.

# La Red Lighthouse — Documento Semilla

**Una aplicación de Janus-Facing Architecture: un bien común de conocimiento atestiguado, sostenido por hubs cívicos.**

Network Theory Applied Research Institute

Este documento se rige plenamente por Janus-Facing Architecture. Nombra roles y mecanismos, nunca el software que los ocupa; cada invariante de la arquitectura madre es vinculante aquí sin necesidad de reformulación, y donde este documento y JFA discrepen, o se corrige este documento o se enmienda JFA a la vista de todos. Su compañero normativo es **lighthouse-weight-tiers.md**, la especificación completa de niveles; este documento resume los niveles y no los duplica — un espejo es una segunda fuente de verdad, que nace ya a la deriva.

**Vocabulario, mapeado a los roles de JFA.** Un **hub** es una institución cívica — una biblioteca, una escuela o cualquier organización que ejecute el software — que sostiene dos roles de JFA en un solo paquete desplegable: el **orquestador** (el rol de coordinador/operador de JFA: la aplicación de cara a los miembros, la bitácora de solo adición del propio hub, sus deberes de resolución de disputas) y el **testigo** (que contrafirma los checkpoints de *otros* hubs). **LBTAS** es la escala de evaluación del pacto — orientada a hacer visibles los daños, derivada de Leveson; su expansión está pendiente de definición (problema abierto 2). Un **ancla** es un compromiso de hechos estructurales y hashes en el registro atestiguado. Una **atestación** es la afirmación firmada de un hub de que una ejecución ocurrió físicamente en sus instalaciones — ocurrencia, nunca verdad. Una **unidad-hub** es la unidad del conteo de corroboración: el hub, nunca la cuenta. Una **etiqueta de suplencia** (stand-in) marca cualquier garantía que opere por debajo de su piso estructural.

---

## Parte I — qué es Lighthouse

Lighthouse es un bien común de conocimiento en el que los hechos empíricos se capturan **junto con los procedimientos que los ponen a prueba**, provenientes de declarantes de origen académico y no académico por igual, anclados a un registro atestiguado a través de hubs locales donde el público puede discutir, replicar y disputar en comunidad. Instancia la Parte VI de JFA: un registro atestiguado puede anclar cualquier afirmación empírica o comercial; una vez anclada, una afirmación se vuelve citable, y el pacto califica al declarante de la misma manera que califica a un socio comercial. Los mismos rieles que hacen confiable el comercio hacen confiable el conocimiento.

El nombre es la disciplina. Un faro no certifica una ruta segura; hace visible el peligro y deja la navegación al barco. Lighthouse ilumina las afirmaciones — sus procedimientos, sus replicaciones, sus disputas, la reputación de sus declarantes — y nunca emite un veredicto sobre la verdad. Señalar, nunca dictaminar; anclar, nunca certificar.

Lo que no debe llegar a ser, heredado textualmente: una agencia calificadora de la verdad, un mercado publicitario donde la visibilidad se compra, un monopolio de acreditación. El descubrimiento permanece federado, citado y disputable.

## Parte II — el modelo de afirmaciones

El objeto atómico de conocimiento es una tripleta vinculada: **afirmación de hecho, procedimiento, resultado**, anclada como afirmación, nunca aseverada como hecho.

- El libro mayor solo consigna hechos estructurales y referencias — los hashes de contenido de los tres artefactos, el tipo de afirmación, el identificador de versión del procedimiento, la marca de tiempo, la referencia seudónima del declarante, la referencia del hub. **Nada de PII en los bienes comunes**, jamás.
- Los artefactos en sí — el texto del procedimiento, los datos — entran al bien común de contribuciones bajo AGPL, direccionados por contenido, servidos por los hubs. La procedencia es entrante = saliente; una contribución no puede retirarse.
- Las afirmaciones de conocimiento, las replicaciones y sus disputas son **relaciones tipadas**, distintas de las señales de comercio y de resolución de disputas. Ningún lector puede colapsarlas.
- Las replicaciones se vinculan a la **versión del procedimiento** que ejecutaron. Un refinamiento es un ancla nueva que cita a la antigua; la reputación se acumula por versión con la cadena visible.
- Toda ancla es interpelable; las impugnaciones son aristas de primera clase; el silencio de un declarante acumula dwell (tiempo de permanencia) — legible, nunca resuelto automáticamente. Un artefacto que deja de ser recuperable se muestra como artefacto-oscuro (artifact-dark); el ancla nunca se borra.

## Parte III — el pacto aplicado

LBTAS califica a **los declarantes, nunca las afirmaciones**. Una afirmación acumula reputación solo a través de la estructura de corroboración de la Parte V; una persona acumula reputación solo a través de su conducta.

- Se publica la distribución completa, nunca un promedio; la calificación más baja es el incumplimiento mismo. Una fabricación nunca se disuelve en un volumen cómodo de buen trabajo.
- **La concordancia es dato; el incumplimiento es conducta.** Una replicación inconsistente es un hecho de concordancia — consistente, inconsistente, no concluyente — nunca una acusación, y jamás se encauza como reclamo de daño. Solo la conducta entra al canal del pacto: la fabricación, la tergiversación de lo que se ejecutó, una atestación falsa. **El desacuerdo nunca es incumplimiento.** Esta separación de canales es lo que impide que los reclamos de daño se conviertan en el arma de la disputa científica.
- El pacto es simétrico: toda afirmación es interpelable, las desestimaciones dejan anotación, y un incumplimiento posterior anota las anclas de un declarante sin borrarlas — un fabricador puede haber dicho algo cierto, y las replicaciones de sus afirmaciones se sostienen sobre su propio historial.
- No hay autoridad de verdad en ninguna parte: ningún "verificado como cierto" de ningún hub, ningún centro, ningún escaneo, ningún modelo. Una ayuda de lectura automatizada explica; nunca certifica.

## Parte IV — la arquitectura de hubs

Un paquete, dos roles, dos claves, **siempre apuntando hacia afuera**.

- Todo hub ejecuta el orquestador y el testigo, pero **ninguna institución atestigua su propia bitácora**. Los checkpoints de la Biblioteca A son contrafirmados por la Escuela B y la Biblioteca C; A devuelve el favor con los de ellas. Las claves de testigo son distintas por pareja y nunca son las del propio operador — un orquestador-testigo fusionado en una sola institución es el operador que se atestigua a sí mismo, exactamente aquello que la capa de registro existe para impedir.
- Un reclamo de daño contra un hub **se presenta ante el testigo de un hub vecino**, aguas arriba, con el operador ausente del nacimiento del reclamo que lo afecta. Dondequiera que dos hubs se federen, la brecha de liveness en la presentación se cierra.
- **Piso de lanzamiento: dos hubs independientes.** Un piloto de un solo hub es conforme solo bajo la etiqueta de suplencia; no puede presentarse como federación.
- **Sede, nunca puerta.** El registro y el mercado viven en el protocolo, por debajo de la aplicación de cualquier hub. Un miembro rechazado o maltratado en la Biblioteca A entra a la aplicación de la Escuela B con su reputación y liquidez intactas. Esa portabilidad — no la buena voluntad de ningún hub — es lo que hace de los hubs sedes y no guardianes de acceso.
- La independencia de los hubs se lee estructuralmente: control distinto por pareja, quedando excluidos el operador común, el controlador común y la matriz administrativa compartida. **Las diez sucursales de un sistema bibliotecario de condado son una sola unidad.** La relación de testigo *no* es una relación de control — los hubs que contrafirman mutuamente sus bitácoras siguen siendo corroboradores independientes, o las federaciones pequeñas se estrangularían al nacer.
- Mercado objetivo: bibliotecas y escuelas, con miembros que inician sesión en la aplicación móvil o web de su hub. Bajo AGPL-3.0, cualquier institución puede entrar al mercado de orquestación del bien común de conocimiento; el copyleft más la escalera de legibilidad mantienen ese mercado contestable, no meramente abierto.

## Parte V — niveles de peso, por referencia

El texto normativo vive en la especificación complementaria. La forma: **T0 Anclado** (la existencia es el piso, nunca evidencia) → **T1 Citado** (renderiza el grafo de descubrimiento; los conteos de citas no dimensionan nada, permanentemente) → **T2 Replicado en el mismo hub** (ejecutabilidad; todas las replicaciones dentro del mismo hub colapsan en una sola unidad-hub) → **T3 Replicado entre hubs** (corroboración contada en unidades de hubs independientes, mantenida por categoría de concordancia — "consistente en cuatro hubs, inconsistente en uno" se publica exactamente así) → **T4 Atestado** (la clave institucional de un hub compromete su reputación sobre la *ocurrencia, nunca la verdad*; el costo de acuñación es cuerpos y tardes, lineal).

Cuatro disciplinas rigen a través de los niveles: la vinculación de versiones; la-concordancia-es-dato-el-incumplimiento-es-conducta; **elegibilidad, nunca dimensionamiento** — el estatus de nivel condiciona si una afirmación puede entrar al flujo de entrada de la economía, y nunca dimensiona un pago; y sin renderizado colapsado — sin puntaje, sin estrellas, sin insignia de verificado, cada nivel publicado con su recibo.

## Parte VI — la postura ante Sybil

Se gestiona hasta que deje de ser rentable, nunca se resuelve: las dos herramientas que podrían resolverlo — una autoridad global de identidad y un muro de compra — son las dos cosas que la arquitectura rechaza. Cuatro movimientos:

1. **La corroboración cuenta hubs, no cuentas.** Exclusión por controlador común en todos los niveles; diez cuentas títere en una biblioteca colapsan en la estructura equivalente a un solo hub.
2. **La presencia física es el costo por unidad.** La atestación hace que el nivel más fuerte cueste cuerpos y tardes, linealmente, sin economías de escala — la deshonestidad se tarifa por encima de su rendimiento, no se previene.
3. **El escaneo de lo demasiado limpio.** Los subgrafos de citas cerrados, los anillos de admiración mutua y la concordancia sospechosamente libre de dispersión entre hubs "independientes" son material de señalamiento — una marca impugnable, nunca una eliminación, porque los falsos positivos caen sobre comunidades de nicho pequeñas y honestas, y la sede natural de impugnación es el propio piso del hub.
4. **Las recompensas se secuencian detrás del interruptor.** Al lanzamiento, el peso no dimensiona nada: sin clasificaciones, sin flujo de entrada. El grafo se acumula en el registro atestiguado — los anillos construidos temprano son esfuerzo desperdiciado y permanentemente visibles para el escaneo retroactivo. El peso se activa después como un cambio de política gobernado y atestiguado, solo para los niveles entre hubs y atestados. Sybil-antes-que-el-peso-de-citas, satisfecho por ordenamiento y no por perfección.

Residuo nombrado: un humano que genuinamente asiste a N hubs (el costo lineal es la defensa); anillos de colusión de humanos reales que abarcan varios hubs (fraude — territorio del pacto, cada caso resuelto es un incumplimiento que nunca se promedia); el alcance de niveles de los miembros remotos (problema abierto 3); la escasez de corroboración en el arranque en frío (las etiquetas de suplencia portan la honestidad).

## Parte VII — el flujo de entrada a la economía

El conocimiento anclado y corroborado se convierte en insumo de I+D para productos y servicios en las economías JFA — el rendimiento de un cultivar, el modo de falla de una herramienta, la curva de costos de un método, fluyendo desde el bien común hacia el intercambio real.

- El estatus de nivel condiciona la **elegibilidad** para el flujo de entrada; el umbral — T3 o superior, o solo T4 en la activación — es política gobernada y atestiguada, no definición de nivel. El dimensionamiento de los pagos pertenece al intercambio real que financia, el cual carga con la fricción comercial que los niveles no pueden cargar.
- **Nunca colocación pagada.** Las afirmaciones de un proveedor sobre sus propios productos se anclan, se replican y se disputan como las de cualquiera; el pacto y el escaneo las vigilan, nunca una tarifa de listado.
- Los invariantes económicos de JFA rigen en su totalidad: la unidad se gana, nunca se compra; no es redimible; la denominación no es redención; y una lectura regulatoria completada antes de cualquier fase de crédito.

## Parte VIII — orden de desarrollo

Constrúyase de abajo hacia arriba; el orden es el argumento. Cada etapa se publica con sus etiquetas de suplencia honestas.

1. **Etapa 0 — el registro federado.** Piloto de dos hubs: bitácoras de solo adición por hub, checkpoints monotónicos con testigos cruzados, pruebas de consistencia, presentación-ante-el-vecino. Esta es la construcción de mayor apalancamiento de la propia JFA (problema abierto 2) vistiendo la ropa de Lighthouse; nada por encima de ella se lee con honestidad hasta que sea real.
2. **Etapa 1 — anclaje y descubrimiento.** T0 y T1: la tripleta de afirmación, el grafo de citas tipado, el servicio de artefactos desde el bien común AGPL. Sin dimensionar nada.
3. **Etapa 2 — replicación y concordancia.** T2 y T3: el conteo por unidad-hub, las distribuciones de concordancia, el renderizado de dwell. Los recibos y las reglas-como-datos-de-política-comparables-por-diff se publican *aquí*, como características de lanzamiento — la legibilidad es un entregable de construcción, no un pulido final.
4. **Etapa 3 — atestación.** T4: claves institucionales de hub, la disciplina de ocurrencia, la regla de exclusión del personal, la atestación falsa alimentando la lectura de conducta del operador.
5. **Etapa 4 — el interruptor del flujo de entrada.** Solo después de la lectura regulatoria y solo para los niveles entre hubs y atestados, como un cambio de política gobernado y atestiguado.

## Parte IX — problemas abiertos

1. **La interfaz de examen del registro está sin diseñar.** Que los miembros examinen el registro a través de la aplicación de su hub hereda la escalera de legibilidad completa — decisiones que se explican en el punto de uso, reglas que viven como datos comparables por diff, versiones de política atestiguadas, ayudas de lectura automatizadas que nunca se convierten en oráculos. Esta es la próxima conversación de diseño, y se nombra aquí en lugar de esquivarse.
2. **LBTAS espera su definición.** Este documento la trata como la escala de evaluación del pacto, orientada a hacer visibles los daños y derivada de Leveson; la expansión y cualquier adaptación específica de Lighthouse de los niveles de la escala están sin escribir.
3. **Exclusión geográfica.** Una comunidad sin hub participante no puede alcanzar T4 y alcanza T3 solo mediante registro a distancia. Las jornadas itinerantes de atestación y los acuerdos con hubs asociados son soluciones de diseño candidatas; la aceptación silenciosa no lo es.
4. **La captura de hubs más allá del escaneo.** Las instituciones reales pueden coludirse; la respuesta es la resolución de disputas más la lectura de conducta del operador, ambas dependientes de que la federación sea real — este problema descansa sobre la Etapa 0 exactamente como el problema 4 de JFA descansa sobre su problema 2.
5. **Todo lo de la Parte VII de JFA rige aquí.** Los problemas 2, 4, 7 y 8 en especial. El diseño de hub-como-testigo de Lighthouse es una palanca propuesta sobre el problema 8 — instituciones cívicas como testigos longevos, públicamente responsables y mutuamente independientes — a demostrarse en el despliegue, no a asumirse.

## El estándar

Un sistema es Lighthouse solo si las siete condiciones se cumplen; si falla una, es otro software vistiendo el vocabulario.

1. Las afirmaciones se anclan como afirmaciones; ningún centro, escaneo, hub o modelo posee un veredicto sobre la verdad.
2. Los hubs son sedes, nunca puertas: el registro y el mercado viven por debajo de la aplicación de cualquier hub, y un miembro deja un hub por otro con su reputación y liquidez intactas.
3. Ninguna institución atestigua su propia bitácora; dos hubs independientes es el piso de la federación, y cualquier cosa menor porta la etiqueta de suplencia.
4. La corroboración se cuenta en unidades de hubs independientes, nunca en cuentas; los conteos de citas no dimensionan nada, permanentemente.
5. Las distribuciones se publican enteras — la concordancia junto al volumen, el daño junto al elogio — nunca un puntaje colapsado ni una insignia de verificado, y todo renderizado porta su recibo.
6. La concordancia es dato y el incumplimiento es conducta; el desacuerdo nunca es incumplimiento.
7. El peso condiciona la elegibilidad y nunca dimensiona los pagos; toda recompensa se sitúa detrás de un interruptor gobernado y atestiguado, secuenciado con Sybil primero.

---

Durante la implementación, el protocolo de tensiones está en vigor: al notar que una restricción se está reformulando por conveniencia, que un sustituto se publica sin etiqueta o que un problema abierto se está esquivando — deténgase, nombre la tensión, adjúntela al invariante o al problema, y proponga el movimiento mínimo conforme. Hágala visible; no la absorba.

*Este documento es documentación libre bajo el bien común AGPL-3.0 del proyecto; está hecho para ser leído, reimplementado y disputado.*
