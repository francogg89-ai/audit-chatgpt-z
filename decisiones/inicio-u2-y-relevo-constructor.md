# Decisión humana — inicio de Unidad 2 y relevo de CONSTRUCTOR

WORK_ID=ideas-audiencia-ia
CARRIL=Z
UNIDAD_ANTERIOR=unidad-1-viabilidad-ia-contratada
UNIDAD_NUEVA=unidad-2-circuito-minimo
INCOMING_TURN_ID_DE_REANUDACION=19

TARGET_WORK_REPO=francogg89-ai/work-claude-z
TARGET_WORK_SHA=5830b23583e353ac5294b40bba66e256f473a48d
AUDIT_PREVIO_SHA=0ee22beb58779a29b649e534272ea0e4a0a9a4ac
CIERRE_U1_PATH=decisiones/cierre-u1-5830b23583e353ac5294b40bba66e256f473a48d.md

PERIMETRO_ULTIMA_MODIFICACION=CONSTITUCION
HUMAN_RESOLUTION_LITERAL=AUTORIZAR_INICIO_U2 Agregar: RELEVO CONSTRUCTOR
U1_CERRADA=SI
TERMINACION_U1=OPCION_DEMOSTRADA
U2_AUTORIZADA=SI
RELEVO_CONSTRUCTOR_SOLICITADO=SI
NEXT_CONSTRUCTOR_INSTANCE=fresh
MODIFICA_PERIMETRO=NO

## Resolución preservada

El humano autorizó explícitamente iniciar `unidad-2-circuito-minimo` después del cierre aprobado de U1 y, en el mismo mensaje, agregó explícitamente `RELEVO CONSTRUCTOR`.

Son dos decisiones separables y ambas quedan preservadas. La autorización de U2 satisface la segunda decisión humana reservada por la constitución en la frontera U1 -> U2. El relevo del CONSTRUCTOR está también autorizado por la política constitutiva `POLITICA_RELEVO_CONSTRUCTOR=solo a demanda humana`.

## Suficiencia para el relevo

No existe entrega pendiente de U1 sin auditar. `work-claude-z @ 5830b23583e353ac5294b40bba66e256f473a48d` fue auditado y luego aprobado por el humano como cierre de U1 con terminación `OPCION_DEMOSTRADA`. El material durable del constructor saliente es suficiente para que una instancia fresca rederive desde Git: `PLAN.md`, `unidad-1-viabilidad-ia-contratada/RESULTADO.md`, el `EVENTO.md` de U1, el bootstrap del CONSTRUCTOR y las decisiones/auditorías aplicables del repositorio de auditoría.

Por tanto el método permite emitir directamente `next_actor=CONSTRUCTOR` y `next_instance=fresh`, sin una ronda artificial del constructor saliente y sin checkpoint de relevo.

## Alcance de U2

U2 queda autorizada conforme al `PLAN.md` aprobado. El CONSTRUCTOR fresco debe rederivar desde Git y construir únicamente `unidad-2-circuito-minimo`, tomando como dependencia cerrada el resultado de U1. No se autoriza modificar manifiesto, PLAN.md ni perímetro por esta decisión.

Las limitaciones de U1 permanecen condicionantes, en particular: M2 demostrado sólo en la cuenta ChatGPT Plus personal probada; texto libre del modelo no literal; vista MCP Apps como canal fiel observado; escritura sin confirmación de ChatGPT; extremo HTTPS público requerido; Quick Tunnel sólo de prueba; autenticación de producto aún no resuelta; otras cuentas/planes, datos reales, concurrencia y producción no demostrados.

## Próxima acción

Abrir U2 con un CONSTRUCTOR fresco. El nuevo CONSTRUCTOR recibe la cabecera canónica completa, rederiva desde Git y comienza la ejecución de `unidad-2-circuito-minimo` conforme a PLAN.md y al manifiesto, sin reabrir U1. Toda verificación discriminante nueva debe seguir REVOLUTIONS §6.1 y ser propuesta antes de ejecutarse.
