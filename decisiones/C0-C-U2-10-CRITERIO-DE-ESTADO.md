WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD=unidad-2-circuito-minimo
DECISION=C0_C_U2_10_CRITERIO_DE_ESTADO_NO_DE_VISIBILIDAD
BASE_AUDIT_SHA=55028412a5ffba81cb836712812f5c75acf80ecd

ACLARACION_HUMANA:
- Sonda propuestas U1, Sonda propuestas U1 v2 y Circuito propuestas C-U2-5 ya están desinstaladas/desconectadas.
- Siguen visibles porque son definiciones/apps disponibles.
- Cada una muestra símbolo '+' para agregarlas/conectarlas nuevamente.
- El detalle observado de Sonda propuestas U1 muestra 'Instalar complemento'.
- No se ejecutó un segundo intento de C0, no se modificó estado, no se tomó nueva captura, no hubo commit y no se ejecutó P1.

DECISION_AUDITOR=Para C-U2-10, C0 debe verificar ESTADO, no ausencia visual absoluta.

CRITERIO_DE_EXITO_C0_C_U2_10:
1. No debe existir ninguna app/complemento del circuito efectivamente instalada o conectada.
2. Una definición histórica del circuito puede seguir visible en 'Created by me' y aun así cumplir C0 si la evidencia positiva demuestra que está NO INSTALADA/NO CONECTADA.
3. La mera visibilidad NO es fallo.
4. La mera ausencia visual tampoco basta por sí sola si no permite verificar el estado relevante.
5. Evidencia positiva aceptable debe mostrar, para cada definición del circuito visible, una señal inequívoca de estado no instalado/no conectado. Ejemplos observados que C-U2-10 puede congelar como indicadores: símbolo '+' de agregar/conectar y/o acción 'Instalar complemento'. El contrato debe preferir texto explícito cuando exista y documentar exactamente qué señal se considera probatoria.
6. Para evitar ambigüedad, la propuesta debe definir una matriz de evidencia por app conocida: nombre exacto + señal de estado. Si una sola captura muestra inequívocamente varios nombres y sus '+' correspondientes, puede bastar para esos nombres; si no, requerir detalle individual.
7. Si aparece cualquier señal de estado instalado/conectado, C0 NO pasa. Cualquier desinstalación/desconexión requerirá autorización humana específica previa y una nueva verificación.
8. Si aparece una definición cuyo estado no puede inferirse inequívocamente de la UI, detenerse; no asumir desconexión por ausencia de botones.
9. C-U2-9 permanece cerrado/bloqueado; sus intentos C0 y captura local no committeada son históricos y no se consumen como evidencia de C-U2-10.

AUTORIDAD_Y_EJECUCION:
- Esta decisión autoriza únicamente ANALISIS_Y_PROPUESTA de C-U2-10.
- No autoriza abrir la UI, tomar capturas, instalar/desinstalar/conectar apps, materializar evidencia, ejecutar gate/P0/C0/P1 ni pasos posteriores.
- C-U2-10 debe usar namespace evidencia-c-u2-10/ y autoridad nueva.
- No heredar autorizaciones de C-U2-9.
- Debe decidir expresamente si gate/P0 se repiten o se reutilizan; no asumir reutilización.

RECOMENDACION_DE_DISENO=En la propuesta C-U2-10, expresar C0 como 'cuenta sin ninguna app del circuito instalada/conectada', no 'lista sin ninguna app del circuito visible'. Preservar la posibilidad de definiciones Created by me visibles y exigir evidencia positiva de su estado no instalado/no conectado.
