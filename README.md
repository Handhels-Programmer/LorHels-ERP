# LorHels-ERP
🚀 1. Panel Principal (Dashboard Interactivo)
Métricas en Tiempo Real: Muestra el total facturado, egresos (compras + gastos), ganancias aproximadas y flujo de caja (pagos recibidos).

Control de Deudas: Indicadores de Cuentas por Cobrar (CXC), Cuentas por Pagar (CXP) y Comisiones pendientes.

Gráfico de Actividad: Un gráfico de líneas interactivo que compara ventas vs egresos de los últimos 7 días.

Acciones Rápidas: Botones superiores para crear facturas, gastos o clientes con un solo clic.

Cobros Pendientes: Una mini-tabla que te avisa qué facturas urgentes faltan por cobrar, con acceso directo a ellas.

💰 2. Módulo de Ventas (Facturas y Cotizaciones)
Numeración Inteligente: Las facturas y cotizaciones se auto-incrementan (ej. FAC-0001, FAC-0002) usando prefijos personalizables.

Ciclo de Cotizaciones: Creas una cotización y, si el cliente acepta, un botón la convierte en Factura automáticamente, restando el inventario.

Abonos y Saldos: Permite registrar pagos parciales a una factura. El sistema calcula matemáticamente la deuda restante y cambia el estado (Pendiente, Parcial, Pagada).

Botón de WhatsApp: Envía un resumen profesional de la factura/cotización directamente al WhatsApp del cliente con un clic.

📦 3. Compras e Inventario
Ciclo de Compras: Puedes hacer Órdenes de Compra y convertirlas a Compras reales cuando llega la mercancía.

Cuentas por Pagar: Registras compras a crédito y el sistema te avisa cuánto le debes a tus proveedores.

Devoluciones: Permite devolver mercancía a proveedores, recalculando la deuda y ajustando el stock.

Control de Stock: Los productos suman o restan cantidades automáticamente al facturar o comprar.

Alertas de Inventario: Avisa visualmente cuando un producto cae por debajo del nivel mínimo establecido.

Ajustes Manuales: Módulo para registrar entradas, salidas o hacer "Toma Física" (inventario manual) dejando un historial de quién y por qué se ajustó.

👥 4. Gestión de Contactos y Productos (Soft Delete)
Directorio Unificado: Maneja tanto clientes como proveedores, estableciendo límites de crédito.

Catálogo de Productos/Servicios: Con control de costo, precio de venta, y soporte para imágenes (URLs).

Función de Archivado: En lugar de borrar clientes o productos y romper facturas viejas, se "Archivan" (Soft Delete). Se vuelven grises, se ocultan de las listas de creación, pero mantienen el historial intacto.

📊 5. Finanzas y Reportes
Gastos Operativos: Registro de luz, nómina, alquiler, etc., que afectan directamente el cálculo de ganancias.

Reportes Visuales: Gráfico de barras comparando ingresos y egresos de los últimos 6 meses, y un gráfico de los Top 5 productos más vendidos.

Notas de Crédito: Si un cliente devuelve algo, se genera un documento, se le aplica el saldo a favor a su factura original y los productos vuelven al estante.

🤝 6. Comisiones por Vendedor
Multi-Agente: Registro de vendedores con un porcentaje base de comisión.

Automatización: Si facturas al contado y seleccionas un vendedor, el sistema calcula y le asigna su comisión sin que tengas que hacer nada.

Dashboard Individual: Puedes filtrar por agente para saber exactamente cuánto ha generado, cuánto se le ha pagado y cuánto dinero se le debe actualmente.

🎨 7. Diseño, PDF y Experiencia de Usuario
PDFs Profesionales: Generación de documentos en PDF con diseño moderno tipo "Apple/Stripe", incluyendo el logo de la empresa y fotos en miniatura de los productos.

Notificaciones Modernas: Sistema de "Toasts" (alertas flotantes animadas) que reemplazan los feos alert() del navegador.

Impuesto Global: Configuras el impuesto (ej. 18%) en los ajustes y todo el sistema lo hereda, bloqueando la edición manual para evitar descuadres contables.

🔐 8. Seguridad y Panel de Super-Administrador (SaaS)
Base de datos Real (Firebase): Todo conectado a Firestore y Firebase Auth.

Bloqueo por Suscripción: Las empresas pueden caducar. Si no pagan, el sistema las bloquea hasta que el Administrador las renueva.

Panel Oculto: Un login de administrador seguro, cuyas credenciales viven en la base de datos (invisibles en el código), desde donde controlas quién entra y quién no a tu ERP.
