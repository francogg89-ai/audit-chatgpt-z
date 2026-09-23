WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
CONTRATO=C-U2-10
ATTEMPT_NUMBER=1
VEREDICTO=EJECUCION_GATE_INTENTO_1_AUTORIZADA_SIN_P0

VERIFY_MATERIALIZATION_AUDIT_SHA=9500904fdf6fbae134980cbb47f5fa9cee362e8d
FREEZE_AUDIT_SHA=f81e1354f7d5356d1add72b13e3f144119da214c
WORK_SHA_AUTORIZACION=6b1b35cc1cfd226dd97e21731e854e93abc233cf
AUTH_BLOB_SHA=bc9f7cd55afc1977b60f6491854285eedbd41260
CONTRACT_BLOB_SHA=2e96c72aaf0b18cc67fccba11282f545d4025d1b
CHECKPOINT_BLOB_SHA=709595ae1cd12a46d3d432d9b6fddc79c4a596c2

RESOLUCION_HUMANA:
H2=ACTIVADA
AUTORIZACION_HUMANA=SI
AUTORIZO_EXCLUSIVAMENTE_UNA_EJECUCION_DE=gate-intento-1

ALCANCE=Autoriza exactamente UNA ejecución de gate-intento-1 de C-U2-10 sobre WORK_SHA_AUTORIZACION y AUTH_BLOB_SHA indicados.

COMANDOS_CONGELADOS_DESDE=unidad-2-circuito-minimo/sistema
1=Get-Location
2=Test-Path .\.venv\Scripts\python.exe
3=.\.venv\Scripts\python.exe -c "import sys; print(sys.executable); print(sys.version)"
4=.\.venv\Scripts\python.exe -c "from importlib.metadata import version; expected={'pytest':'9.1.1','mcp':'2.2.0','httpx':'0.28.1'}; actual={k:version(k) for k in expected}; assert actual == expected, (actual, expected); print(' '.join(f'{k}={actual[k]}' for k in ('pytest','mcp','httpx')))"
5=.\.venv\Scripts\python.exe -m pip check

EVIDENCE_PATH=unidad-2-circuito-minimo/evidencia-c-u2-10/gate-intento-1/comandos.txt
DETENCION_PATH=unidad-2-circuito-minimo/evidencia-c-u2-10/gate-intento-1/DETENCION.md

PRECONDICIONES:
- Verificar ATTEMPT_NUMBER=1.
- Verificar WORK_SHA_AUTORIZACION=6b1b35cc1cfd226dd97e21731e854e93abc233cf.
- Verificar AUTH_BLOB_SHA=bc9f7cd55afc1977b60f6491854285eedbd41260.
- Verificar CONTRACT_BLOB_SHA=2e96c72aaf0b18cc67fccba11282f545d4025d1b.
- Verificar CHECKPOINT_BLOB_SHA=709595ae1cd12a46d3d432d9b6fddc79c4a596c2.
- Verificar que evidencia-c-u2-10/gate-intento-1/ no exista antes de iniciar.

EJECUCION=Ejecutar exactamente una vez los cinco comandos, en orden, desde unidad-2-circuito-minimo/sistema. Registrar en comandos.txt cada comando literal, su salida completa y EXIT_CODE.

SI_FALLA=Detenerse inmediatamente. Agregar DETENCION.md en el mismo directorio. No ejecutar P0. C-U2-10 queda fallido y no admite un segundo gate dentro de este contrato; cualquier nueva ejecución exige propuesta sucesora separada.

SI_PASA=Detenerse inmediatamente antes de P0 y devolver la evidencia al AUDITOR. P0 NO queda autorizado por esta resolución humana ni por este sobre.

PROHIBICIONES:
- No ejecutar P0.
- No ejecutar C0.
- No ejecutar P1-P11, R0, R1-R6 ni RZ.
- No instalar/modificar dependencias o entorno.
- No abrir UI.
- No abrir servidor, túnel ni exposición pública.
- No ejecutar un segundo gate.
- No modificar AUTH_PATH ni evidencia histórica.

NO_RETROACTIVIDAD=La autorización se consume con esta única ejecución de gate-intento-1.