# Cómo modificar una addenda para cargar XML en portales de clientes

## 1. Consigue la especificación vigente del cliente

El portal del cliente o su área de cuentas por pagar publica la guía de la addenda, a veces con su XSD: qué nodos pide, cuáles son obligatorios, en qué orden y con qué formato. Trabaja siempre con la versión vigente: las especificaciones cambian y una guía vieja es la causa más común de rechazos.

## 2. Compara qué cambió

Revisa contra la versión anterior o contra tu plantilla actual:

- Nodos nuevos o eliminados.
- Campos que ahora son obligatorios.
- Nombres de nodos o namespaces distintos.
- Formatos: fechas, decimales, longitudes máximas.

## 3. Modifica la plantilla en tu sistema de facturación

La addenda se arma con un mapeo: cada dato de la factura se asigna a un nodo de la addenda. Modifica ese mapeo en tu sistema (Pegaso o el ERP donde generas el CFDI):

- Número de orden de compra → nodo que pida el cliente.
- Número de entrega o remisión.
- Tienda / sucursal / departamento.
- Cualquier dato adicional que el cliente exija.

Verifica que los campos de origen existan en la factura: si un dato no está en el documento, la addenda saldrá vacía y el portal la rechazará.

## 4. Genera un XML de prueba y valídalo

Genera un CFDI de prueba con la addenda modificada y valídalo:

- Contra el XSD del cliente, si lo proporciona.
- Con el validador del portal, si tiene uno.
- Revisa que el CFDI siga siendo válido ante el SAT (la addenda no debe romper la estructura del comprobante).

## 5. Súbelo al portal en pruebas y corrige los errores

Sube el XML de prueba al portal y corrige lo que marque. Errores típicos:

- Namespace mal puesto o faltante.
- Nodo obligatorio faltante.
- Fecha o decimales en formato incorrecto.
- Número de orden de compra que no coincide con el del cliente.
- Addenda de otro cliente pegada por error.
- Caracteres especiales sin escapar (&, <, >).

## 6. Carga los XML reales

Una vez que el portal acepta el XML de prueba, ya puedes cargar los XML reales. Guarda la versión de la plantilla y la especificación del cliente con la fecha, para saber con cuál se generó cada carga.

## Errores que bloquean el pago

Un XML rechazado en el portal no se cobra: el cliente no lo registra como recibido. Si un lote se rechaza, revisa el mensaje del portal, corrige la plantilla y vuelve a cargar. No reenvíes el mismo XML sin cambios: el portal lo rechazará de nuevo.
