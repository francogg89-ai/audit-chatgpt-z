WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-9
VEREDICTO=C0_HUMANO_COMPLETADO_EVIDENCIA_NO_MATERIALIZADA_AUTORIZAR_SOLO_COMMIT_EVIDENCIA

P0_AUDIT_SHA=29f2753e06db4204e64563e11e87e96709c9bd2b
C0_AUTH_AUDIT_SHA=eb1f9443dc151d16c4323436a561753e5d12d979
BASE_WORK_SHA=04814040b03ad38868f292689735717928d3184f
P0_BLOB_SHA=c52ec76cbef45c23ba14bc505a90cb3d86ffff6e
CONTRACT_BLOB_SHA=3c416d9d790624020bd422f273d8b6f487fce939
CHECKPOINT_BLOB_SHA=05edc4e08eedfd4ff52e4f2eb82b42eea9ceca8a

REPORTE_HUMANO:
C0_COMPLETADO=SI
APPS_CIRCUITO_DESINSTALADAS=SI
LISTA_VERIFICADA_SIN_APPS_CIRCUITO=SI
P1_EJECUTADO=NO
PASOS_POSTERIORES=NO

EVIDENCE_PATH=unidad-2-circuito-minimo/evidencia-c-u2-9/c0-cuenta-sin-apps.png

VERIFICACION_GIT=La evidencia no existe todavía en BASE_WORK_SHA. El último commit de work-claude-z sigue siendo 04814040b03ad38868f292689735717928d3184f y fetch de EVIDENCE_PATH sobre ese SHA devuelve 404.

ESTADO=C0_ACCION_HUMANA_COMPLETADA_EVIDENCIA_PENDIENTE_DE_MATERIALIZAR_EN_GIT

AUTORIZACION_AUDITOR=Autorizar al CONSTRUCTOR exclusivamente a incorporar EVIDENCE_PATH en un único commit nuevo sobre BASE_WORK_SHA.

REGLAS:
- Verificar que el archivo exista localmente en EVIDENCE_PATH antes de commitear.
- El commit debe agregar únicamente EVIDENCE_PATH.
- No modificar contrato, checkpoint, gate-intento-1/comandos.txt, p0-comandos.txt, código, entorno ni ninguna otra evidencia.
- No ejecutar P1 ni ningún paso posterior.
- No repetir C0.
- No instalar/modificar dependencias o entorno.
- No abrir túnel, servidor ni exposición pública.
- Después del commit, detenerse y devolver WORK_SHA_RESULTADO_C0 + C0_BLOB_SHA al AUDITOR.

SI_ARCHIVO_NO_EXISTE=Detenerse y devolver human_need; no reconstruir ni inventar la captura.

P1_AUTORIZADO=NO
