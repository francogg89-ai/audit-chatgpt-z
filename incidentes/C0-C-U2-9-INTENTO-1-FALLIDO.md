WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-9
VEREDICTO=C0_INTENTO_1_FALLIDO_NO_ACREDITADO_REINTENTO_NO_AUTORIZADO

BASE_WORK_SHA=04814040b03ad38868f292689735717928d3184f
P0_AUDIT_SHA=29f2753e06db4204e64563e11e87e96709c9bd2b
C0_AUTH_AUDIT_SHA=eb1f9443dc151d16c4323436a561753e5d12d979
C0_EVIDENCE_MATERIALIZATION_AUDIT_SHA=e8663ddbf3329113220ae789ee1232c797118cf0

CONSTRUCTOR_REPORT=DETENIDO_ANTES_DE_COMMIT
EVIDENCE_LOCAL_PATH=unidad-2-circuito-minimo/evidencia-c-u2-9/c0-cuenta-sin-apps.png
EVIDENCE_COMMITTED=NO
WORK_HEAD_VERIFICADO=04814040b03ad38868f292689735717928d3184f

HALLAZGO_REPORTADO=La inspección local de la captura contradice C0_COMPLETADO. La vista ChatGPT > Plugins > Personal > Created by me muestra tres entradas del circuito todavía visibles:
- Sonda propuestas U1
- Sonda propuestas U1 v2
- Circuito propuestas C-U2-5

ALCANCE_DE_VERIFICACION=El AUDITOR no dispone de la captura en Git y por tanto no realiza verificación visual independiente del PNG. Se acepta como señal de detención el reporte del CONSTRUCTOR, que es suficiente para NO acreditar C0 y evitar materializar evidencia inválida.

RESULTADO_C0=FALLIDO_NO_ACREDITADO.
MOTIVO=No se cumple la condición congelada 'que no quede ninguna app del circuito visible'.
CAPTURA_INVALIDA=No debe incorporarse como evidencia de C0 exitoso.
P1_EJECUTADO=NO.
P1_AUTORIZADO=NO.

AUTORIDAD=La autorización humana de C0 anterior habilitó una única ejecución y prohibió reintentos. Ese intento quedó consumido por la acción humana realizada. No existe autorización vigente para repetir C0.

NEXT_HUMAN=Autorizar explícitamente UN REINTENTO de C0 sobre BASE_WORK_SHA=04814040b03ad38868f292689735717928d3184f. El reintento deberá limitarse a: (1) abrir la lista de apps del modo desarrollador; (2) desinstalar las tres entradas reportadas y cualquier otra app del circuito que siga visible; (3) verificar que no quede ninguna app del circuito; (4) tomar una NUEVA captura y reemplazar únicamente el archivo local aún no versionado c0-cuenta-sin-apps.png con la nueva evidencia; (5) detenerse antes de P1. Si alguna app no puede desinstalarse, detenerse y reportar cuál. La autorización de reintento no habilitará materialización en Git automáticamente; tras el reintento, el AUDITOR volverá a verificar el reporte antes de autorizar el commit de evidencia.

NO_AUTORIZADO_HASTA_ENTONCES=Reintentar C0, materializar la captura actual, ejecutar P1-P11, R0, R1-R6, RZ, instalar/modificar dependencias o entorno, abrir servidor/túnel/exposición pública o ampliar alcance.
