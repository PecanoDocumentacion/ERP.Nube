### GenerarVentaElectronica

| **Propiedad** | **Descripción** | **Condición** |
| --- | --- | --- |
| **IdVentaExterna**  <br>`obligatorio`  <br>`string` | Identificador del comprobante de venta del sistema externo. | Máximo 32 caracteres alfanuméricos. |
| **IdTipoDocumento**  <br>`obligatorio`  <br>`string` | Tipo de documento del comprobante de venta.  <br>[[Ver listado]](../Listado/TipoDocumento.md) |  |
| **Moneda**  <br>`obligatorio`  <br>`string` | Moneda del comprobante de venta.  <br>[[Ver listado]](../Listado/TipoMoneda.md) |  |
| **Fecha**  <br>`obligatorio`  <br>`date - ISO8601` | Fecha del comprobante de venta. | Formato: "YYYY-MM-DD" |
| **IdClienteExterno**  <br>`obligatorio`  <br>`string` | Identificador del cliente del sistema externo. | Máximo 32 caracteres alfanuméricos. |
| **NombreCliente**  <br>`obligatorio`  <br>`string` | Nombre completo del cliente. | Máximo 85 caracteres. |
| **CorreoCliente**  <br>`obligatorio`  <br>`string` | Correo del cliente. | Admite varias cuentas de correo separadas por puntos y comas (;) |
| **UbigeoCliente**  <br>`opcional`  <br>`string` | Ubigeo del cliente. | Solo 6 dígitos. |
| **TipoDICliente**  <br>`obligatorio`  <br>`string` | Tipo de documento de identidad del cliente.  <br>[[Ver listado]](../Listado/TipoDocumentoIdentidad.md) |  |
| **NumeroDICliente**  <br>`obligatorio`  <br>`string` | Número del documento de identidad del cliente. |  |
| **Condicion**  <br>`obligatorio`  <br>`string` | Condición de la venta.  <br>[[Ver listado]](../Listado/CondicionVenta.md) | Constante "T" para Tankea Marketplace. |
| **IdSubcondicion**  <br>`obligatorio`  <br>`string` | Subcondición de la venta. | Constante "1" para Tankea Marketplace. |
| **IdFormaPago**  <br>`obligatorio`  <br>`number` | Forma de pago.  <br>[[Ver listado]](../Listado/FormaPago.md) | Constante 2 para Tankea Marketplace. |
| **IdPagoElectronico**  <br>`condicional`  <br>`number` | Identificador del pago electrónico.  <br>[[Ver listado]](../Listado/TipoPagoElectronico.md) | Se debe ingresar cuando la forma de pago es "Pago Electrónico" (2). |
| **SubTotal**  <br>`obligatorio`  <br>`number` | Subtotal de la venta. | Numérico mayor que cero. |
| **Igv**  <br>`obligatorio`  <br>`number` | Monto del IGV de la venta. | Numérico mayor que cero. |
| **Total**  <br>`obligatorio`  <br>`number` | Importe total de la venta. | Numérico mayor que cero. |
| **TipoCambio**  <br>`condicional`  <br>`number` | Valor del tipo de cambio de la venta. |  |
| **ObservacionVenta**  <br>`opcional`  <br>`string` | Observación del comprobante de venta. | Máximo 1500 caracteres alfanumérico. |
| **DireccionCliente**  <br>`opcional`  <br>`string` | Dirección del cliente. | Máximo 200 caracteres. |
| **Items**  <br>`obligatorio`  <br>`array` | Detalles del comprobante de venta.  <br>[[Ver entidad]](../Entidad/Items.md) |  |