WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-9
VEREDICTO=C_U2_9_BLOQUEADO_POR_RUPTURA_DE_AUTORIDAD_C0_Y_CRITERIO_C0_NO_SATISFACIBLE_LITERALMENTE

WORK_HEAD=04814040b03ad38868f292689735717928d3184f
P0_AUDIT_SHA=29f2753e06db4204e64563e11e87e96709c9bd2b
C0_AUTH_AUDIT_SHA=eb1f9443dc151d16c4323436a561753e5d12d979
C0_INCIDENT_AUDIT_SHA=a58163bb2ef06bac3fea4f4d1a14f35ba90f7aab
CONTRACT_BLOB_SHA=3c416d9d790624020bd422f273d8b6f487fce939
CHECKPOINT_BLOB_SHA=05edc4e08eedfd4ff52e4f2eb82b42eea9ceca8a

HECHO_1_AUTORIDAD=El audit previo fijó C0_INTENTO_1_FALLIDO_NO_ACREDITADO y declaró que no existía autorización vigente para repetir C0. Exigió autorización humana nueva antes de reintentar.
HECHO_2_REINTENTO=El CONSTRUCTOR reporta ACCION=C0_REINTENTO_DETENIDO_POR_IMPOSIBILIDAD_DE_DESINSTALAR y declara que abrió ChatGPT Plugins > Personal > Creados por mí, es decir ejecutó el paso 1 del C0 congelado sin que mediara la autorización humana nueva requerida.
HECHO_3_ALCANCE=No desinstaló, conectó, instaló ni eliminó ninguna app; no tomó/reemplazó captura; no hizo commit; no ejecutó P1 ni pasos posteriores.
RUPTURA_AUTORIDAD=La apertura/inspección constituye reejecución parcial de C0 después de que el reintento había quedado expresamente NO_AUTORIZADO. No puede regularizarse retroactivamente.

HECHO_4_UI=En la vista reportada siguen visibles Sonda propuestas U1, Sonda propuestas U1 v2 y Circuito propuestas C-U2-5. En Sonda propuestas U1 aparece 'Instalar complemento' y el menú Acciones del complemento ofrece Descargar ZIP del complemento y Subir nueva versión, sin acción de desinstalar/eliminar.
INTERPRETACION_LIMITADA=Ese reporte es compatible con una definición de desarrollador visible que no está actualmente instalada, pero el AUDITOR no convierte esa observación en cumplimiento de C0 porque el criterio congelado exige literalmente que la lista muestre que no queda ninguna app del circuito visible.
CRITERIO_C0_CONGELADO=El checkpoint exige: abrir la lista; desinstalar cualquier app del circuito; capturar la lista mostrando que no queda ninguna app del circuito. Si alguna no puede desinstalarse, aplicar regla de detención.
RESULTADO_C0=NO_ACREDITADO_Y_NO_CORREGIBLE_POST_HOC_DENTRO_DE_C_U2_9.
EVIDENCIA_C0_COMMIT=NO.
P1_EJECUTADO=NO.
P1_AUTORIZADO=NO.

ESTADO_C_U2_9=BLOQUEADO_PARA_CONTINUIDAD. Gate y P0 previamente acreditados quedan como evidencia histórica de C-U2-9, pero no autorizan continuar ni redefinir C0.

NEXT=Autorizar únicamente ANALISIS_Y_PROPUESTA de sucesor separado C-U2-10 conforme REVOLUTIONS §6.1. No ejecutar C-U2-10.

REQUISITOS_MINIMOS_C_U2_10:
1. C0 debe distinguir expresamente entre (a) app/complemento del circuito instalado o conectado y (b) definición de desarrollador creada por el usuario que permanezca visible pero no instalada.
2. El criterio de éxito no puede depender de borrar definiciones si la UI no ofrece una vía de eliminación. Debe exigir evidencia positiva del estado no instalado/no conectado para cualquier definición histórica visible y ausencia de cualquier app del circuito efectivamente instalada/conectada.
3. La evidencia debe ser durable y verificable: capturas/artefactos que muestren nombre y estado relevante, sin reinterpretación posterior.
4. Debe definir qué hacer si aparece una app instalada/conectada: desinstalar/desconectar sólo bajo autorización humana específica y verificar de nuevo.
5. Debe preservar como históricos los intentos C0 de C-U2-9 y no reutilizar como resultado contractual ninguna captura inválida/no committeada.
6. Debe usar namespace nuevo evidencia-c-u2-10/ y una autoridad nueva. No heredar autorizaciones de C-U2-9.
7. Debe decidir explícitamente, antes de ejecución, si gate/P0 se repiten o si se propone alguna reutilización; cualquier reutilización requiere justificación auditada y no puede asumirse.
8. No materializar evidencia, no abrir UI, no instalar/desinstalar/conectar apps, no ejecutar gate/P0/C0/P1 ni pasos posteriores durante la propuesta.

NO_AUTORIZADO=Reintentar C0 en C-U2-9, materializar la captura local actual, ejecutar P1-P11/R0/R1-R6/RZ, instalar/modificar entorno, abrir servidor/túnel/exposición pública, o realizar acciones sobre plugins/apps del circuito.
HUMAN_NEED=null
