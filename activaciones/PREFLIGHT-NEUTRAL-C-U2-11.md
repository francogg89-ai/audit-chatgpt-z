WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-11
VEREDICTO=PREFLIGHT_NEUTRAL_DE_PERSISTENCIA_AUTORIZADO_SIN_C0

FREEZE_AUDIT_SHA=3647aa6d2c87967437fa40cbc361adf4f7df038c
TARGET_WORK_SHA=82b49de2a191e1a409d3f1511fd8b6fbe2fe1b03
CONTRACT_BLOB_SHA=05d903d95635273449a31c1f22fa14dcc651713a
CHECKPOINT_BLOB_SHA=ff405cc11af02d53fb853432259a3211b3ad3066

RESOLUCION_HUMANA:
H2=ACTIVADA
AUTORIZACION_HUMANA=SI
AUTORIZO_EXCLUSIVAMENTE_UNA_EJECUCION_DE=PREFLIGHT_NEUTRAL_DE_PERSISTENCIA

ALCANCE=En una pagina neutral que no muestre lista, detalle, nombre, configuracion ni estado de apps del circuito, probar una vez un mecanismo ya disponible de captura Windows, guardar el PNG de prueba en `unidad-2-circuito-minimo/evidencia-c-u2-11/preflight/guardado-png-prueba.png`, reabrir ese mismo archivo desde disco y documentar localmente persistencia/lectura en `unidad-2-circuito-minimo/evidencia-c-u2-11/preflight/resultado.md`.

RESULTADO_MD_DEBE_INCLUIR=ruta exacta, nombre exacto, metodo usado, tamano no nulo y resultado de reapertura/lectura.

SI_PASA=Detenerse inmediatamente. No abrir lista/detalle de apps. Reportar al AUDITOR que el preflight paso y los dos archivos locales creados. C0 permanece NO AUTORIZADO y requerira autorizacion separada.
SI_FALLA_O_ES_INCIERTO=Detenerse inmediatamente antes de C0. Documentar localmente la limitacion sin fabricar evidencia y reportar al AUDITOR. No remediar instalando software ni cambiando configuracion.

DECLARACION_HUMANA_DE_ESTADO=El humano declara que las apps del circuito ya fueron eliminadas/desconectadas de su cuenta y que su presencia visual con `+` no implica por si sola instalacion/conexion.
VALOR_DE_LA_DECLARACION=CONTEXTO_HUMANO_NO_EVIDENCIA_C0. C-U2-11 congelado exige para C0 texto explicito visible asociado inequívocamente al nombre exacto de cada app. La declaracion humana no sustituye ese criterio ni autoriza C0.

PROHIBICIONES:
- No abrir ni inspeccionar la lista o detalle de apps del circuito.
- No ejecutar C0.
- No instalar, conectar, reconectar, desconectar, desinstalar, eliminar ni modificar apps.
- No cambiar configuracion.
- No ejecutar gate, P0, P1 ni pasos posteriores.
- No abrir servidor, tunel ni exposicion publica.
- No hacer commit ni push de los artefactos del preflight.
- No materializar evidencia operacional en Git.
- No repetir el preflight.

NO_RETROACTIVIDAD=La autorizacion se consume con esta unica ejecucion del preflight neutral.