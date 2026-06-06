# LorHels ERP

---

### 🛡️ 1. Motor del SaaS y Seguridad (El Core)

* **Login Inteligente:** Un único formulario que sabe quién entra. Si eres tú (Super Admin), te manda a la sala de control. Si es un cliente, lo manda a su propio entorno aislado.
* **Panel Super Admin (`admin.html`):** Tu mesa de control privada. Desde aquí ves qué empresas se han registrado, apruebas sus cuentas (activando sus suscripciones) y monitoreas cuándo caducan sus planes.
* **Ajustes Multi-Tenant (`ajustes.html`):** Cada empresa tiene su propio espacio aislado en la base de datos (Firebase) para configurar sus datos, moneda, ITBIS, términos, cambiar su PIN y subir su **Logo** (conectado a Cloudinary para no saturar tu base de datos).

### 💰 2. Ciclo de Ventas y Cobros

* **Dashboard (`dashboard.html`):** El panel de bienvenida del cliente. Muestra KPIs en tiempo real (Ventas, Cuentas por Cobrar, Gastos), un gráfico interactivo (Chart.js) y las últimas facturas emitidas.
* **Cotizaciones (`cotizaciones.html`):** Permite crear presupuestos y enviarlos por WhatsApp. Incluye un botón mágico que **convierte una cotización en factura** con un solo clic.
* **Facturación (`facturas.html`):** El motor principal. Calcula matemáticas en tiempo real (subtotal, ITBIS, descuentos), gestiona el estado (A Crédito, Pagada), resta automáticamente los NCF y genera PDFs hermosos (`html2pdf.js`).
* **Pagos (`pagos.html`):** Registra los cobros a facturas a crédito. Al aplicar un pago, el sistema rebaja la deuda de la factura y del cliente automáticamente, generando un Recibo de Ingreso.
* **Notas de Crédito (`nota-credito.html`):** Permite revertir saldos de facturas por errores o devoluciones sin romper la contabilidad.
* **Comisiones (`comisiones.html`):** Lee qué vendedor hizo cada factura, permite asignarle un porcentaje de comisión dinámico y llevar el control de lo que se le ha pagado a los empleados.

### 📦 3. Ciclo de Compras e Inventario

* **Directorio (`clientes-prov.html`):** Un CRM integrado que divide a los contactos entre Clientes y Proveedores, rastreando automáticamente cuánto te deben (Cuentas por Cobrar).
* **Productos y Servicios (`productos.html`):** El catálogo. Diferencia entre un producto físico (que requiere control de stock) y un servicio (intangible).
* **Órdenes de Compra (`orden-compra.html`):** Para pedir mercancía a los proveedores (Borrador, Aprobada, Enviada).
* **Compras (`compras.html`):** Registra las facturas de tus proveedores. Al marcar la compra como "Recibida", el sistema **suma automáticamente** las cantidades al inventario.
* **Inventario (`inventario.html`):** Panel de control físico. Valora en dinero cuánto hay en el almacén, lanza alertas de stock bajo y permite hacer ajustes manuales (entradas, mermas, auditorías).
* **Gastos Operativos (`gastos.html`):** Controla el dinero que sale de la empresa (luz, nómina, internet) categorizado por fijo o variable.

### 🏛️ 4. Reportes y Cumplimiento Fiscal (DGII)

* **Contabilidad / DGII (`contabilidad-dgii.html`):** Administrador de talonarios fiscales. Controla las secuencias de NCF (B01, B02, B04, etc.) para que la facturación nunca exceda los límites aprobados. Además, genera automáticamente los archivos `.TXT` listos para subir a la Oficina Virtual (Formatos **606** de compras y **607** de ventas).
* **Informes (`informes.html`):** Generador de reportes analíticos. Con la integración de `SheetJS` y `html2pdf.js`, el cliente puede exportar sus ventas, gastos e inventario a **Excel** o **PDF** seleccionando rangos de fechas.

---

### 🛠️ Pila Tecnológica Usada:

* **Frontend:** HTML5, CSS3 Nativo (CSS Grid y Flexbox para diseño responsivo sin depender de frameworks pesados como Bootstrap) y JavaScript (ES6+).
* **Backend & Base de Datos:** Firebase Auth (Seguridad) y Cloud Firestore (Base de datos NoSQL en tiempo real).
* **Almacenamiento de Medios:** Cloudinary (vía API directa).
* **Librerías de Utilidad:** `Chart.js` (Gráficos), `html2pdf.js` (Documentos en PDF) y `SheetJS` (Exportación a Excel .xlsx).
