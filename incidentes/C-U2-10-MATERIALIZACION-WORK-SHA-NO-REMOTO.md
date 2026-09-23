WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-10
ATTEMPT_NUMBER=1
VEREDICTO=MATERIALIZACION_NO_VERIFICABLE_WORK_SHA_NO_PRESENTE_EN_REMOTO

PARENT_WORK_SHA=5848d734ffd3917ee58c4b4164e93f1b022430b6
DECLARED_WORK_SHA_AUTORIZACION=6b1b35cc1cfd226dd97e21731e854e93abc233cf
DECLARED_AUTH_BLOB_SHA=bc9f7cd55afc1977b60f6491854285eedbd41260
AUTH_PATH=unidad-2-circuito-minimo/evidencia-c-u2-10/autorizaciones/gate-intento-1.md
MATERIALIZE_AUDIT_SHA=cc8dc0639755a5689832433475b3206e3b1c359c

VERIFICACION_REMOTA:
- GitHub no resuelve DECLARED_WORK_SHA_AUTORIZACION; fetch del archivo en ese ref devuelve 404.
- El historial remoto visible mantiene PARENT_WORK_SHA=5848d734ffd3917ee58c4b4164e93f1b022430b6 como commit más reciente.

CONCLUSION=La materialización declarada no puede auditarse todavía. No se verifica delta, AUTH_BLOB_SHA ni contenido. No se declara válida ni inválida por contenido.

ESTADO_C_U2_10=CONGELADO_NO_EJECUTADO_NO_AGOTADO.
MATERIALIZACION=NO_VERIFICABLE_HASTA_PUBLICACION_REMOTA.
EJECUCION_GATE=NO_AUTORIZADA.
P0=NO_AUTORIZADO.
C0_Y_POSTERIORES=NO_AUTORIZADOS.

NEXT=CONSTRUCTOR current debe únicamente: (A) pushear/publicar al remoto el commit exacto 6b1b35cc1cfd226dd97e21731e854e93abc233cf sobre PARENT_WORK_SHA; o (B) si ya existe remoto con otro SHA, devolver WORK_SHA_AUTORIZACION remoto correcto y AUTH_BLOB_SHA exacto. No modificar AUTH_PATH ni crear ningún otro archivo.

NO_AUTORIZADO=No ejecutar gate/P0/C0/P1-P11/R0/R1-R6/RZ; no abrir UI; no instalar/desinstalar/conectar apps; no modificar entorno; no abrir servidor/túnel/exposición pública; no materializar una segunda autorización.