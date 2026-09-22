WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-9
ATTEMPT_NUMBER=1
VEREDICTO=EJECUCION_GATE_INTENTO_1_AUTORIZADA_SIN_P0

FREEZE_AUDIT_SHA=f2ea00e4f3bcc061b6521c7db46f9bd99fa6fdfe
MATERIALIZE_AUDIT_SHA=a6ba2c5ade4b11175f80d4bc0bb74e6fbe246d54
VERIFY_MATERIALIZATION_AUDIT_SHA=6578bccea8762400f5cf268cf0711f052b966652

WORK_SHA_AUTORIZACION=f297ee6e63b969834ac5172525e7da621a593b9c
AUTH_BLOB_SHA=2ebbf75cfe00e878f3e84a8096777a034648d9fe
CONTRACT_BLOB_SHA=3c416d9d790624020bd422f273d8b6f487fce939
CHECKPOINT_BLOB_SHA=05edc4e08eedfd4ff52e4f2eb82b42eea9ceca8a

RESOLUCION_HUMANA:
H2=ACTIVADA
AUTORIZACION_HUMANA=SI
AUTORIZO_EXCLUSIVAMENTE_LA_EJECUCION_DE=gate-intento-1

ALCANCE=Autoriza exactamente UNA ejecución de gate-intento-1 de C-U2-9 sobre WORK_SHA_AUTORIZACION y AUTH_BLOB_SHA indicados.

LIMITES_HUMANOS:
- NO autoriza P0.
- NO autoriza un segundo intento del gate.
- NO autoriza instalar o modificar dependencias.
- NO autoriza modificar el entorno.
- NO autoriza C0, P1-P11, R0, R1-R6 ni RZ.
- NO autoriza abrir túnel ni usar ChatGPT real.
- Si gate-intento-1 falla, detenerse y devolver control con human_need.
- Si gate-intento-1 pasa, detenerse igualmente antes de P0 y devolver evidencia al AUDITOR; P0 requerirá una nueva autorización humana explícita.

SOBRE_EJECUCION_GATE=SI
AUTORIZACION_AUDITOR=El AUDITOR autoriza al CONSTRUCTOR a ejecutar una sola vez gate-intento-1 conforme al contrato/checkpoint congelados y a preservar su evidencia exclusivamente en:
unidad-2-circuito-minimo/evidencia-c-u2-9/gate-intento-1/comandos.txt
y, si el gate falla, DETENCION.md dentro del mismo directorio.

PRECONDICIONES:
- Verificar desde Git ATTEMPT_NUMBER=1.
- Verificar WORK_SHA_AUTORIZACION=f297ee6e63b969834ac5172525e7da621a593b9c.
- Verificar AUTH_BLOB_SHA=2ebbf75cfe00e878f3e84a8096777a034648d9fe.
- Verificar CONTRACT_BLOB_SHA=3c416d9d790624020bd422f273d8b6f487fce939.
- Verificar CHECKPOINT_BLOB_SHA=05edc4e08eedfd4ff52e4f2eb82b42eea9ceca8a.
- Verificar que evidencia-c-u2-9/gate-intento-1/ no exista antes de iniciar.
- Ejecutar desde unidad-2-circuito-minimo/sistema los cinco comandos literales congelados.
- Registrar comando literal, salida y EXIT_CODE en comandos.txt.

DETENCION=Después de completar gate-intento-1, PASA o FALLA, detenerse antes de P0. No ejecutar ningún paso adicional. Devolver WORK_SHA_RESULTADO, blob de comandos.txt y, si existe, blob de DETENCION.md al AUDITOR.

NO_RETROACTIVIDAD=Esta autorización es específica de ATTEMPT_NUMBER=1 y se consume con esa única ejecución.
