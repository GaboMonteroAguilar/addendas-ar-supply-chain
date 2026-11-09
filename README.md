# Modificación de addendas para AR Supply Chain

Guía y plantillas para modificar las addendas de los CFDI y cargar los XML en los portales de los clientes.

## Qué es una addenda

La addenda es un nodo opcional del XML del CFDI donde se incluye información adicional que pide el cliente receptor. No afecta la validez fiscal del comprobante ante el SAT, pero el portal del cliente sí la valida con su propia especificación: si está mal, el portal rechaza la carga y el cliente no paga.

## Contenido

- [Guía — Cómo modificar una addenda](guides/modificacion-addendas.md): el proceso paso a paso.
- [Ejemplo — Addenda genérica](examples/addenda-ejemplo.xml): fragmento XML de ejemplo, con valores de muestra para adaptar a cada cliente.

## El proceso en resumen

1. Consigue la especificación vigente del cliente.
2. Compara qué cambió.
3. Modifica la plantilla en tu sistema de facturación (Pegaso o ERP).
4. Genera un XML de prueba y valídalo.
5. Súbelo al portal en pruebas y corrige los errores.
6. Carga los XML reales una vez aceptado.

## Nota

Cada cliente tiene su propia especificación de addenda. No hay una sola para todos: adapta siempre la plantilla a la guía del cliente que corresponda.
