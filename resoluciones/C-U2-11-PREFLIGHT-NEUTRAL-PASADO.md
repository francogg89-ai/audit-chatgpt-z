TARGET_WORK_SHA=82b49de2a191e1a409d3f1511fd8b6fbe2fe1b03
PREFLIGHT_ACTIVATION_AUDIT_SHA=92371c082d2f5b4d71c6b0bd5ee7bfe9e8433810
FREEZE_AUDIT_SHA=3647aa6d2c87967437fa40cbc361adf4f7df038c
PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION
VEREDICTO=PREFLIGHT_NEUTRAL_C_U2_11_PASADO_C0_NO_AUTORIZADO

CONTRATO=C-U2-11
CONTRACT_BLOB_SHA=05d903d95635273449a31c1f22fa14dcc651713a
CHECKPOINT_BLOB_SHA=ff405cc11af02d53fb853432259a3211b3ad3066

PREFLIGHT_EJECUTADO=SI
PREFLIGHT_RESULTADO=PASA
PREFLIGHT_CONSUMIDO=SI
C0_EJECUTADO=NO
C0_AUTORIZADO=NO

PNG_PATH_LOCAL=unidad-2-circuito-minimo/evidencia-c-u2-11/preflight/guardado-png-prueba.png
PNG_SIZE_BYTES_REPORTADO=106031
PNG_SIGNATURE_REPORTADA=89-50-4E-47-0D-0A-1A-0A
PNG_DECODE_REPORTADO=OK
PNG_DIMENSIONS_REPORTADAS=1919x973
RESULT_PATH_LOCAL=unidad-2-circuito-minimo/evidencia-c-u2-11/preflight/resultado.md
RESULT_FILE_SIZE_BYTES_REPORTADO=380
METODO_REPORTADO=Captura de pantalla de Windows mediante FN+PrtSc
REAPERTURA_REPORTADA=EXITOSA
LECTURA_REPORTADA=LEGIBLE_Y_NO_VACIA

BASE_PROBATORIA=La persona reporto una unica ejecucion neutral, guardado y reapertura exacta desde disco. El CONSTRUCTOR reporto verificacion local posterior de existencia/tamano, firma PNG valida, decodificacion y dimensiones, y confirmo resultado.md. El sobre autorizador exigia evidencia local no versionada y prohibia commit/push; por ello el AUDITOR no inspecciona directamente los bytes de esos artefactos.

LIMITACION_AUDITORIA=La acreditacion del preflight se basa en reporte humano + verificacion local del CONSTRUCTOR conforme al mecanismo congelado. No es una verificacion byte-a-byte independiente del AUDITOR. Esta limitacion no se proyecta a C0: la suficiencia de las capturas y matriz de C0 debera ser revisada despues mediante un mecanismo de materializacion separado antes de cualquier continuidad.

DECLARACION_HUMANA_ESTADO=Se conserva como contexto que las apps fueron eliminadas/desconectadas. No es evidencia C0 y no sustituye texto explicito visible asociado a cada app.

ESTADO_C_U2_11=CONGELADO_PREFLIGHT_PASADO_DETENIDO_ANTES_DE_C0

NEXT_HUMAN=Autorizar explicitamente UNA UNICA EJECUCION DE C0 sobre TARGET_WORK_SHA=82b49de2a191e1a409d3f1511fd8b6fbe2fe1b03, CONTRACT_BLOB_SHA=05d903d95635273449a31c1f22fa14dcc651713a, CHECKPOINT_BLOB_SHA=ff405cc11af02d53fb853432259a3211b3ad3066 y PREFLIGHT_AUDIT_SHA de esta resolucion. Alcance exclusivo: abrir una sola vez las vistas de lectura necesarias para Sonda propuestas U1, Sonda propuestas U1 v2 y Circuito propuestas C-U2-5, mas cualquier app inequívocamente del circuito; no pulsar controles de accion; exigir texto explicito visible ligado al nombre exacto; guardar PNG secuenciales sin editar en evidencia-c-u2-11/c0-estado-apps-NN.png y crear c0-matriz-estados.md. Si aparece solo +, boton sin etiqueta, ausencia/lista vacia, texto no ligado inequívocamente, app instalada/conectada, afiliacion incierta o problema de captura, detenerse y marcar C0_NO_ACREDITADO. Cero reintentos. No P1 ni pasos posteriores.

NO_AUTORIZADO=No abrir UI de apps hasta nueva autorizacion humana; no ejecutar C0/P1; no tocar estado/configuracion de apps; no instalar/conectar/desconectar/desinstalar/eliminar; no ejecutar servicios/tunel; no materializar/committear evidencia C0 hasta sobre auditor posterior.