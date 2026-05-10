# LorHels ERP


### 🏢 1. Arquitectura SaaS y Panel de Super-Administrador

* **Multi-Empresa:** El sistema permite que múltiples negocios se registren de forma independiente.
* **Control de Suscripciones:** Las empresas eligen un plan (Básico, Normal, Premium, Negocios). El sistema las mantiene "Pendientes" hasta que el Super-Administrador aprueba su acceso y establece su fecha de vencimiento.
* **Bloqueo Automático:** Si la suscripción de una empresa caduca, el sistema le bloquea el acceso automáticamente mostrando una pantalla de renovación.
* **Seguridad (Auth):** Acceso seguro mediante Correo Electrónico y un PIN de 6 dígitos. Opción de cambiar el PIN desde el panel de Ajustes.
* **Modo Demo (Offline):** Capacidad de funcionar 100% sin internet usando `localStorage` para demostraciones de ventas sin consumir base de datos.

---

### 📊 2. Dashboard Interactivo y en Tiempo Real

* **Tarjetas de Métricas:** Resumen inmediato de Total Facturado, Egresos (Compras + Gastos), Ganancia Neta Estimada y Pagos Recibidos.
* **Indicadores de Deuda:** Control visual de Cuentas por Cobrar (CXC), Cuentas por Pagar (CXP) y Comisiones pendientes.
* **Gráfico de Actividad:** Un gráfico de líneas suavizadas que compara las Ventas vs. los Egresos de los últimos 7 días.
* **Acciones Rápidas:** Botones directos para crear facturas, registrar gastos o añadir clientes.
* **Alertas de Cobro:** Mini-tabla interactiva que muestra las últimas 5 facturas que los clientes aún no te han pagado.

---

### 💼 3. Módulo de Ventas (Facturas y Cotizaciones)

* **Cotizaciones:** Creación de propuestas que, al ser aprobadas, se convierten en Facturas con un solo clic (descontando el inventario automáticamente).
* **Facturación Avanzada:** Control de facturas al contado o a crédito. Soporta pagos parciales (abonos), marcando la factura como "Pendiente", "Pago Parcial", "Pagada" o "Saldo a Favor".
* **Envíos por WhatsApp:** Botón inteligente que genera un resumen de cobro con el número de factura, balance pendiente y abre WhatsApp Web/Móvil directo al chat del cliente.

---

### 🛒 4. Compras y Proveedores

* **Órdenes de Compra:** Solicitudes a proveedores que, al recibirse, se convierten en "Compras" y suman automáticamente la mercancía al inventario.
* **Cuentas por Pagar:** Registro de deudas con proveedores y un historial de pagos emitidos (egresos).
* **Devoluciones a Proveedor:** Si algo llega mal, el sistema procesa la devolución, resta el inventario y ajusta la deuda con el proveedor de forma matemática.

---

### 📦 5. Inventario y Catálogo de Productos

* **Control de Stock:** Los productos suman o restan cantidades automáticamente según las ventas, compras o devoluciones.
* **Alertas de Escasez:** El sistema avisa visualmente cuando un producto está por debajo de su límite mínimo establecido.
* **Ajustes de Inventario:** Módulo para registrar Entradas, Salidas (mermas) o "Toma Física" (conteo manual), dejando un historial detallado del motivo del ajuste.
* **Archivado (Soft Delete):** Posibilidad de "Archivar" productos descontinuados para que no salgan al facturar, pero sin dañar el historial de facturas antiguas.

---

### 👥 6. Directorio de Contactos (Clientes y Proveedores)

* **Perfiles Detallados:** Información de contacto, direcciones, redes sociales y asignación de Límites de Crédito.
* **Estado de Cuenta Individual:** Al abrir un cliente, el sistema calcula al instante todo lo que ha comprado y exactamente cuánto dinero debe.
* **Archivado de Contactos:** Oculta clientes inactivos sin perder su historial financiero.

---

### 🤝 7. Comisiones para Vendedores

* **Módulo de Agentes:** Registro de vendedores con su porcentaje (%) de comisión base.
* **Cálculo Automático:** Si se cobra una factura y tiene un vendedor asignado, el sistema genera la comisión sola para evitar errores humanos.
* **Seguridad Anti-Duplicados:** Candados de software que evitan pagarle doble comisión a un vendedor por la misma factura.

---

### 💵 8. Finanzas y Contabilidad

* **Registro de Gastos:** Control de egresos operativos (Luz, Alquiler, Nómina) que afectan la gráfica de ganancias.
* **Cobros y Pagos Globales:** Un panel centralizado para registrar cualquier pago que entre o salga de la empresa hacia facturas o compras pendientes.
* **Notas de Crédito:** Generación formal de devoluciones de clientes. Devuelve el producto al estante y le otorga saldo a favor al cliente.
* **Reportes Gráficos:** Pestaña dedicada con gráficos de "Ingresos vs Egresos (6 meses)" y "Top 5 Productos Más Vendidos".

---

### 📄 9. Generación de PDFs y Personalización

* **Diseño Premium:** Plantillas de PDF modernas con encabezados degradados, datos bancarios automáticos en el pie de página, logotipo de la empresa e **imágenes en miniatura de cada producto** facturado.
* **Ajustes Maestros:** El dueño configura su Moneda (RD$, US$, €), su Impuesto Global (bloqueado para evitar errores de los cajeros), datos del banco, prefijos de facturación (FAC-001) y términos por defecto.
* **Notificaciones Toasts:** Alertas visuales flotantes y modernas que reemplazan las ventanas bloqueantes del navegador.
