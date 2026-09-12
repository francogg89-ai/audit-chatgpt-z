# Auditoría — corrección D-05/D-06/D-07 y congelamiento de C-U2-3

TARGET_WORK_REPO=francogg89-ai/work-claude-z
TARGET_WORK_SHA=3bc4bbd204cf9ad7f1059f64ef5ccf00afd6ba72
WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
PREVIOUS_AUDIT_SHA=265b07b6cffa71fd7624d04eb059ecd0d456679e
PREVIOUS_AUDIT_PATH=auditorias/130fdb3db72dd17d9e919ba6ffc1d5ab005835e1.md
PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION
VEREDICTO=C_U2_3_CONGELADO_CHECKPOINT_REQUIERE_CORRECCION
D_05=CERRADO
D_06=CERRADO
D_07=CERRADO
CONTRATO_C_U2_3_CONGELADO=SI
CONTRATO_C_U2_3_EJECUTADO=NO
CONTRATO_C_U2_3_PATH=unidad-2-circuito-minimo/EVENTO.md
CONTRATO_C_U2_3_BLOB_SHA=a769509cecfd1aa0b6081bda19f8a7a55fd2446c
CHECKPOINT_PATH=unidad-2-circuito-minimo/CHECKPOINT_HUMANO.md
CHECKPOINT_BLOB_SHA=f2fef129e25b3aeceeb1e056da2dafcf6ebddf32
CHECKPOINT_APTO_PARA_EJECUCION=NO
HUMAN_NEED_REAL_ACTUAL=NO
U2_CERRADA=NO

## Identidad y delta

Git confirma un único commit entre `130fdb3db72dd17d9e919ba6ffc1d5ab005835e1` y TARGET_WORK_SHA. El delta queda dentro de `unidad-2-circuito-minimo/`; no modifica `evidencia/`, `evidencia-c-u2-2/`, `RESULTADO-LOCAL.md`, `PLAN.md`, U1, manifiesto ni perímetro. No se ejecutó C-U2-3, túnel ni ChatGPT real.

## D-05 — cerrado

El consentimiento OAuth ya no entrega la capacidad del panel a un tercero. `CreatorAuthorization.authorize()` redirige a `/conectar?solicitud=...`, sin capacidad, token ni testigo. El acceso a `/conectar` queda ligado a una sesión de creador abierta previamente al alcanzar el panel con su capacidad. Sin esa sesión la ruta responde 403, no revela la aplicación solicitante y no permite aprobar. La capacidad sigue existiendo únicamente en la URL privada del panel y el contrato prohíbe entregarla a terceros.

La prueba de construcción cubre tanto ausencia de capacidad en la URL entregada al agente como imposibilidad de ver o aprobar sin sesión. Esto no demuestra todavía interoperabilidad real; esa propiedad queda correctamente reservada a C-U2-3.

## D-06 — cerrado

`cmd_exportar()` incorpora `conexiones` y `tokens`. `conexiones` conserva solicitud y `approved_at`; `tokens` usa un ledger sin valores accionables, con huella, tipo, cliente, creación, expiración y `revoked_at`. El panel permite revocar una conexión y revoca los tokens vivos del cliente. Las pruebas de construcción verifican que la exportación muestra aprobación/revocación y que ningún valor de token aparece en `evidencia.json`.

Por tanto la transición de autorización y el control R4 quedan observables después de la corrida sin depender del relato humano.

## D-07 — cerrado

La segunda propuesta de C-U2-3 fija antes de ejecutar M1, M2, M5 y M6 literalmente, exige el mismo mensaje en las dos repeticiones de cada caso y permite únicamente sustituir `<BASE>`. Para C2.11 fija un baseline previo: la idea es solamente `que hablen de música` y el participante declara no tener ejemplo, dato ni experiencia. El criterio de fallo enumera las clases de información que no pueden agregarse.

Con esto la comparación de entrada/salida ya no puede redefinirse después de observar el modelo.

## Congelamiento C-U2-3

La propuesta reemplaza íntegramente la versión nunca congelada. Sobre TARGET_WORK_SHA, `unidad-2-circuito-minimo/EVENTO.md` blob `a769509cecfd1aa0b6081bda19f8a7a55fd2446c` contiene antes de toda ejecución: candidato exacto, propiedad, entorno, secuencia, estímulos, cantidad de corridas, evidencia durable, criterios binarios de éxito/fallo, controles negativos y limitaciones para C2.6, C2.7, C2.8, C2.10 y C2.11.

Se congela durablemente como `C-U2-3`. No se autoriza cambiar su texto, candidato, estímulos, baseline, cantidad de corridas ni criterios después de este punto. Toda ejecución futura se interpreta contra este blob.

## CHECKPOINT_HUMANO — todavía no apto

El checkpoint está correctamente condicionado a que el AUDITOR congele este mismo contrato y no contiene secretos escritos. Sin embargo no es todavía un procedimiento autocontenido y fiel al contrato congelado por tres propiedades concretas:

1. **No es autocontenido.** Para R1–R6 remite a `EVENTO.md` para obtener M1, M2, M5 y M6. Un checkpoint material debe contener literalmente los estímulos ya congelados y todos los pasos que el humano necesita, sin depender de abrir otro archivo para reconstruir la ejecución.
2. **Permite sustituir una corrida interrumpida.** Indica que si una conversación se corta o debe reiniciarse, se anota y se empieza otra conversación. C-U2-3 fija exactamente dos corridas por caso y declara fallo si la secuencia no puede completarse. Después del congelamiento no se puede descartar una tentativa observada y reemplazarla por una tercera. Una interrupción de una de las dos corridas previstas debe preservarse y resolverse conforme al criterio de fallo; no debe autorizar un retry que cambie la muestra.
3. **Permite reemplazar una captura que contiene un secreto.** El checkpoint dice que, si una captura contiene capacidad/token/testigo, se reemplace por otra que no lo muestre. El contrato declara precisamente como fallo que una corrida pida o exponga un secreto o que una URL entregada a un tercero lo contenga. El procedimiento no puede borrar esa observación después de verla. Debe evitar distribuir el secreto, pero preservar durablemente el hecho de que la exposición ocurrió, mediante una representación redactada/derivada que no altere el veredicto ni una recaptura que haga desaparecer el fallo.

Estas correcciones son del checkpoint; no requieren ni autorizan modificar el contrato congelado ni el candidato.

## Necesidad humana

`HUMAN_NEED_REAL_ACTUAL=NO` en este pase, por instrucción de no activar todavía H-2 y porque el checkpoint que materializaría la ejecución no es aún apto. No se debe abrir exposición, usar la cuenta real ni ejecutar C-U2-3.

## Próxima acción

CONSTRUCTOR current: modificar únicamente lo necesario para que `CHECKPOINT_HUMANO.md` sea autocontenido y fiel a C-U2-3 ya congelado: incluir literalmente M1/M2/M5/M6 y baseline; eliminar cualquier retry/reemplazo de corridas que altere las dos observaciones fijadas; y reemplazar la regla de recaptura de secretos por una preservación redactada que conserve el hecho del fallo sin divulgar el secreto. No modificar `EVENTO.md`, candidato, contrato, evidencias históricas, PLAN, manifiesto ni perímetro. No ejecutar C-U2-3, túnel ni ChatGPT real y no activar H-2. Cerrar con un único commit autoritativo y devolverlo al AUDITOR.