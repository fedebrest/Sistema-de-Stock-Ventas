# 📦 Sistema de Gestión de Stock y Ventas 
Este sistema ha sido desarrollado como una solución integral, ágil y de "cero configuración" para gestionar el inventario de stands, registrar ventas en tiempo real y realizar arqueos de caja durante el evento.

## 📋 Descripción del Sistema
Este sistema es una aplicación web de una sola página (SPA) construida para ofrecer máxima portabilidad. No requiere bases de datos externas ni servidores; toda la información se almacena localmente en el navegador del usuario (LocalStorage), lo que garantiza rapidez y funcionamiento incluso sin conexión a internet.

### 📋 Características Principales
**Inventario Dinámico:** Visualización clara de stock, estados (óptimo, crítico, sin stock) y gestión de productos.   
**Gestión de Ventas:** Registro de operaciones con distinción de método de pago (Efectivo / Transferencia).  
**Motor de Promociones:** Aplicación de descuentos porcentuales o montos fijos de forma rápida durante la venta.  
**Reportes Profesionales:** Generación de PDFs detallados con arqueo de caja, historial de ventas e inventario, listos para imprimir o compartir.  
**Interfaz Moderna:** Diseño oscuro (Dark Mode) optimizado con Tailwind CSS, amigable a la vista para largas jornadas de trabajo en el evento.  

### 🛠️ Módulos Incluidos
**1. Dashboard de Inventario:** Panel principal para carga de nuevos productos y monitoreo de existencias.  
**2. Módulo de Ventas:** Formulario inteligente que calcula subtotales y permite aplicar promociones precargadas.  
**3. Gestión de Promociones:** Panel dedicado a crear y editar códigos de descuento o promociones especiales.  
**4. Arqueo de Caja:** Contadores globales que separan recaudación en Efectivo vs. Transferencias.  
**5. Historial y Auditoría:** Listado completo de ventas realizadas con capacidad de edición o anulación de registros (con ajuste automático de stock).  

### 📚 Librerías y Tecnologías Utilizadas
Este proyecto utiliza tecnologías web para asegurar la máxima compatibilidad:
- [Tailwind CSS](https://tailwindcss.com/): Framework de CSS para el diseño responsivo y la interfaz de usuario moderna.
- [FontAwesome](https://fontawesome.com/): Conjunto de iconos vectoriales.
- [jsPDF](https://artskydj.github.io/jsPDF/docs/jsPDF.html): Motor para la generación de archivos PDF desde el navegador.
- [jsPDF-AutoTable](https://github.com/JonatanPe/jsPDF-AutoTable): Plugin para crear tablas elegantes dentro de los documentos PDF

## 🚀 Instrucciones de Uso
### 1. Preparación Inicial
- El sistema no requiere instalación. Simplemente se debe abrir el archivo ```index.html``` en cualquier navegador web (Chrome, Firefox, Brave, etc.).
- **Importante:** Al usar ```LocalStorage```, los datos persistirán en ese navegador específico. Evita borrar la caché del navegador para no perder el historial de ventas.

### 2. Cargar Productos
1. Dirigirse a la sección **"Cargar Producto"**.  
2. Ingresar el nombre, stock inicial y precio unitario.
3. Hacer clic en **"Agregar a Stock"**. El producto aparecerá instantáneamente en la tabla de Inventario.

### 3. Registrar una Venta
1. Ir al módulo **"Registrar Venta"** .
2. Seleccionar el producto del desplegable.
3. Ingresar la cantidad. (El sistema mostrará automáticamente si hay stock disponible).
4. Seleccionar el método de pago y, si aplica, una promoción.
5. Pulsar **"Procesar Venta"**.

### 4. Generar Reportes
1. En la parte superior derecha, hacer clic en el botón verde **"Exportar PDF"** .
2. El sistema generará automáticamente un documento con:
   - Resumen financiero total.
   - Desglose de ventas por método de pago.
   - Estado actual del stock.
   - Impacto de las promociones utilizadas.

## ⚠️ Notas para Administradores

**Cierre de Caja:** Si se desea comenzar un nuevo día o evento, utilizar el botón **"Reiniciar Caja"** en el panel de Historial de Ventas. *¡Cuidado!* Esta acción borra el historial de ventas y reinicia los contadores a $0.00.  

**Correcciones:** Si se cometió un error en una venta, se puede usar el botón **"Corregir"** (icono de lápiz) en la fila de la venta específica para modificar la cantidad o el precio sin necesidad de borrar y recrear la operación.
