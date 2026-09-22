WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
TIPO=POSTMORTEM_TRAZABILIDAD_ENTORNO
CONTRATO_CERRADO=C-U2-6
CLOSED_WORK_SHA=9dacc395fd90e4c78ef3fde462d0a7f69993f54a
CLOSED_AUDIT_SHA=c417201985a9dc7a7a75332d097cd99a279da43d

ESTADO_C_U2_6=EJECUTADO_HASTA_P0_AGOTADO_FALLIDO
REABRIR_C_U2_6=NO
REINTENTAR_C_U2_6=NO

HECHOS_VERIFICADOS_EN_GIT:
- CHECKPOINT_HUMANO-C-U2-6 exigía Python 3.12 con unidad-2-circuito-minimo/sistema/requirements.txt instalado en su entorno virtual y dos terminales con ese entorno virtual activo.
- requirements.txt contiene pytest==9.1.1.
- evidencia-c-u2-6/p0-comandos.txt preserva C:\Python312\python.exe: No module named pytest.

OBSERVACION_LOCAL_REPORTADA_EN_POSTMORTEM:
INTERPRETER_USED=C:\Python312\python.exe
PYTHON_COMMAND_RESOLUTION=C:\Python312\python.exe
EXPECTED_ENVIRONMENT=unidad-2-circuito-minimo/sistema/.venv/Scripts/python.exe
VENV_EXECUTABLE=C:\FRANCO_PERSONAL\Ideas_streaming\work-claude-z\unidad-2-circuito-minimo\sistema\.venv\Scripts\python.exe
VENV_PYTEST=AVAILABLE
VENV_PYTEST_VERSION=9.1.1
Esta observación local se registra como reporte posterior y no modifica ni completa retroactivamente la evidencia de C-U2-6.

INTERPRETACION=La causa queda refinada como discrepancia de selección de intérprete/precondición de terminal: P0 se consumió con el Python global, no con el intérprete del .venv previsto. Esto no cambia el veredicto contractual de C-U2-6 ni demuestra fallo del parser.

DECISION=Corresponde sucesor separado C-U2-7, no corrección ni nueva corrida de C-U2-6.

REQUISITO_C_U2_7=El sucesor debe eliminar la dependencia implícita de 'activar' el entorno. Antes del P0 discriminante debe existir una fase de preparación de entorno no discriminante que identifique de forma objetiva el intérprete y pytest disponibles. El contrato/checkpoint debe fijar un único mecanismo inequívoco para todos los comandos Python de la corrida, preferentemente invocando explícitamente el intérprete del repositorio (por ejemplo .\.venv\Scripts\python.exe) en vez de depender de cómo resuelva 'python' en PATH. Debe preservar evidencia del ejecutable real usado y de la versión de pytest antes de consumir P0. Si el entorno requerido no existe o no satisface requirements, se detiene antes de abrir la corrida discriminante; instalar o modificar dependencias requiere autorización humana separada.

ACCION_HUMANA_AHORA=NINGUNA. No hay que instalar, activar, reintentar ni ejecutar nada ahora. El CONSTRUCTOR ya está autorizado únicamente a proponer C-U2-7 conforme REVOLUTIONS §6.1. Tras su evaluación y congelamiento, la siguiente acción humana será una H-2/autorización de ejecución NUEVA ligada a las identidades exactas de C-U2-7; cualquier instalación o modificación del entorno, si resultara necesaria, deberá pedirse explícitamente antes de ejecutar.

NEXT=CONSTRUCTOR current: preparar candidato/CONTRATO-C-U2-7.md/CHECKPOINT_HUMANO-C-U2-7.md como un único commit autoritativo, preservando F-01..F-04, D-11, D-12 y toda evidencia histórica. No ejecutar, no instalar, no abrir túnel, no usar ChatGPT real.