TARGET_WORK_SHA=ce89a58c0862abced634224dea1dc42a27505b6a
BASE_WORK_SHA=8e90a91b7ea374516b901a6fc2b9a03149f8718b
P0_ACTIVATION_AUDIT_SHA=662ca8e0224bf64103d565cbfa670b1d37248be3
PRIOR_TRANSPORT_AUDIT_SHA=1697ff6a87b29af8519bdf587aa324aaceec961f
PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION
VEREDICTO=P0_C_U2_10_VALIDO_Y_PASADO_C0_NO_AUTORIZADO

CONTRATO=C-U2-10
WORK_SHA_RESULTADO_P0=ce89a58c0862abced634224dea1dc42a27505b6a
P0_PATH=unidad-2-circuito-minimo/evidencia-c-u2-10/p0-comandos.txt
P0_BLOB_SHA=00ff48dc02ea8564ec8e35a69bf951d88caa355a
CONTRACT_BLOB_SHA=2e96c72aaf0b18cc67fccba11282f545d4025d1b
CHECKPOINT_BLOB_SHA=709595ae1cd12a46d3d432d9b6fddc79c4a596c2

DELTA=Git confirma exactamente un commit sobre BASE_WORK_SHA y agrega únicamente P0_PATH.
P0_COMMAND=.\.venv\Scripts\python.exe -m pytest -q tests/test_comandos_literales.py
P0_OUTPUT=13 passed in 2.10s
P0_EXIT_CODE=0
P0=PASO
P0_CONSUMIDO=SI

C0_EJECUTADO=NO
C0_AUTORIZADO=NO
P1_AUTORIZADO=NO
ESTADO_C_U2_10=CONGELADO_P0_PASADO_CONTINUIDAD_DETENIDA_ANTES_DE_C0

NOTA_HUMANA_PREVIA=El humano informó que las aplicaciones están desconectadas y que el símbolo + permite volver a instalarlas. Esa nota permanece como contexto, no como evidencia contractual y no sustituye una ejecución C0 autorizada.

NEXT_HUMAN=Autorizar explícitamente UNA ejecución de C0 sobre WORK_SHA_RESULTADO_P0=ce89a58c0862abced634224dea1dc42a27505b6a, P0_BLOB_SHA=00ff48dc02ea8564ec8e35a69bf951d88caa355a, CONTRACT_BLOB_SHA=2e96c72aaf0b18cc67fccba11282f545d4025d1b y CHECKPOINT_BLOB_SHA=709595ae1cd12a46d3d432d9b6fddc79c4a596c2.

ALCANCE_C0_A_AUTORIZAR=Inspeccionar únicamente el estado instalado/conectado de las definiciones del circuito; incluir como mínimo Sonda propuestas U1, Sonda propuestas U1 v2 y Circuito propuestas C-U2-5, además de cualquier otra app inequívocamente del circuito visible. Registrar evidencia positiva de NO INSTALADA/NO CONECTADA mediante señales inequívocas como + con contexto de agregar/conectar o Instalar complemento. Guardar capturas sin editar como c0-estado-apps-01.png, -02.png, etc. y c0-matriz-estados.md con referencia exacta por fila. Si cualquier estado es ambiguo o aparece una app instalada/conectada, detenerse.

PROHIBIDO_EN_C0=No instalar, conectar, reconectar, desinstalar ni eliminar apps; no ejecutar P1 ni pasos posteriores; no abrir servidor/túnel/exposición pública; no modificar entorno.

NO_AUTORIZADO_HASTA_ENTONCES=No abrir ni inspeccionar UI para C0, no crear evidencia C0 y no ejecutar P1-P11/R0/R1-R6/RZ.