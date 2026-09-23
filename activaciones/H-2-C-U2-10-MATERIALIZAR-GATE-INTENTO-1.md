WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-10
ATTEMPT_NUMBER=1
VEREDICTO=APROBADO_H2_Y_AUTORIZADO_UNICAMENTE_MATERIALIZAR_GATE_INTENTO_1

FREEZE_AUDIT_SHA=f81e1354f7d5356d1add72b13e3f144119da214c
PARENT_WORK_SHA=5848d734ffd3917ee58c4b4164e93f1b022430b6
CONTRACT_BLOB_SHA=2e96c72aaf0b18cc67fccba11282f545d4025d1b
CHECKPOINT_BLOB_SHA=709595ae1cd12a46d3d432d9b6fddc79c4a596c2
AUTH_PATH=unidad-2-circuito-minimo/evidencia-c-u2-10/autorizaciones/gate-intento-1.md

RESOLUCION_HUMANA:
H2=ACTIVADA
AUTORIZACION_HUMANA=SI
AUTORIZO_UNICAMENTE_EL_INICIO_DEL_HANDSHAKE_DE_MATERIALIZACION=SI

ALCANCE_HUMANO=La autorización humana permite únicamente iniciar el handshake. No autoriza materializar por sí sola, ejecutar gate-intento-1, ejecutar P0, abrir C0 ni realizar pasos posteriores.

SOBRE_MATERIALIZAR=SI
AUTORIZACION_AUDITOR=El AUDITOR autoriza exclusivamente MATERIALIZAR el registro de autorización en AUTH_PATH.

DELTA_PERMITIDO=Un único commit nuevo sobre PARENT_WORK_SHA que agregue únicamente AUTH_PATH.

CONTENIDO_MINIMO_AUTH_PATH:
- ATTEMPT_NUMBER=1
- PARENT_WORK_SHA=5848d734ffd3917ee58c4b4164e93f1b022430b6
- CONTRACT_BLOB_SHA=2e96c72aaf0b18cc67fccba11282f545d4025d1b
- CHECKPOINT_BLOB_SHA=709595ae1cd12a46d3d432d9b6fddc79c4a596c2
- AUDIT_SHA de este sobre MATERIALIZAR
- H2=ACTIVADA
- AUTORIZACION_HUMANA=SI
- alcance exclusivo de materialización
- prohibición expresa de gate/P0/C0/P1-P11/R0/R1-R6/RZ, instalación/modificación, servidor/túnel/UI operacional
- regla de detención después de materializar y devolver WORK_SHA_AUTORIZACION + AUTH_BLOB_SHA

PROHIBICIONES:
- No incluir en AUTH_PATH el SHA futuro del commit que todavía no existe.
- No crear gate-intento-1/.
- No crear comandos.txt ni DETENCION.md.
- No crear p0-comandos.txt.
- No ejecutar ningún comando del gate.
- No ejecutar P0.
- No abrir C0 ni la UI.
- No instalar/desinstalar/conectar apps.
- No modificar entorno.
- No abrir servidor, túnel o exposición pública.
- No ejecutar ningún paso posterior.

DETENCION=Después del único commit de materialización, detenerse y devolver exclusivamente las identidades WORK_SHA_AUTORIZACION y AUTH_BLOB_SHA junto con AUTH_PATH. La autorización MATERIALIZAR queda consumida por ese commit.

EJECUCION_GATE=NO_AUTORIZADA.
P0=NO_AUTORIZADO.
C0_Y_POSTERIORES=NO_AUTORIZADOS.