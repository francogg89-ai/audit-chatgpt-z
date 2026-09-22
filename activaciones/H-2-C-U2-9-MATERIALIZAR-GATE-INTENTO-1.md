WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-9
ATTEMPT_NUMBER=1
VEREDICTO=APROBADO_H2_Y_AUTORIZADO_UNICAMENTE_MATERIALIZAR_GATE_INTENTO_1

FREEZE_AUDIT_SHA=f2ea00e4f3bcc061b6521c7db46f9bd99fa6fdfe
PARENT_WORK_SHA=a8f054c4c52ea547bc89464216ab999fef5cb405
CONTRACT_BLOB_SHA=3c416d9d790624020bd422f273d8b6f487fce939
CHECKPOINT_BLOB_SHA=05edc4e08eedfd4ff52e4f2eb82b42eea9ceca8a

RESOLUCION_HUMANA:
H2=ACTIVADA
AUTORIZACION_HUMANA=SI
AUTORIZO_UNICAMENTE_EL_INICIO_DEL_HANDSHAKE_DE_MATERIALIZACION=SI

ALCANCE_HUMANO=La autorización humana habilita únicamente el inicio del handshake de materialización. No autoriza materializar por sí sola, ejecutar gate, P0, instalar/modificar dependencias ni pasos posteriores.

SOBRE_AUDITOR_MATERIALIZAR=SI
AUTORIZACION_AUDITOR=El AUDITOR autoriza al CONSTRUCTOR exclusivamente a MATERIALIZAR un único archivo:
unidad-2-circuito-minimo/evidencia-c-u2-9/autorizaciones/gate-intento-1.md

REGLAS_DE_MATERIALIZACION:
- BASE/PARENT exacto: a8f054c4c52ea547bc89464216ab999fef5cb405
- ATTEMPT_NUMBER=1
- El commit debe agregar únicamente AUTH_PATH.
- El archivo debe contener al menos ATTEMPT_NUMBER, PARENT_WORK_SHA, CONTRACT_BLOB_SHA, CHECKPOINT_BLOB_SHA, referencia a esta autorización auditora, alcance y prohibiciones.
- No debe anticipar ni contener su propio WORK_SHA_AUTORIZACION.
- No modificar contrato, checkpoint, código, entorno ni evidencia histórica.
- No crear gate-intento-1/, comandos.txt, DETENCION.md ni p0-comandos.txt.
- No ejecutar ningún comando del gate.
- No instalar ni modificar dependencias.
- No abrir túnel.
- No usar ChatGPT real.
- Después del commit, detenerse y devolver WORK_SHA_AUTORIZACION + AUTH_BLOB_SHA al AUDITOR.
- Esta autorización se consume con una sola materialización. No habilita EJECUCION_GATE.
- La ejecución del gate requerirá una nueva verificación auditora y un sobre separado EJECUCION_GATE que referencie exactamente ATTEMPT_NUMBER=1, WORK_SHA_AUTORIZACION y AUTH_BLOB_SHA.

AUTH_PATH=unidad-2-circuito-minimo/evidencia-c-u2-9/autorizaciones/gate-intento-1.md
NEXT=CONSTRUCTOR current materializa exclusivamente AUTH_PATH y devuelve identidades.
