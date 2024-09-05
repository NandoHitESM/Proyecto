# Modelo Relacional Para Aplicación De Un Restaurante

## Integrantes/Autor
Emmanuel Hernandez Gallego - Estudiante
Samuel Yepes Vasquez - Estudiante
Matias Zapata Hincapié - Estudiante

## Producto(Product)
    product_id(PK) Primary key (Número) 
    product_name: Nombre del producto (Texto)
    product_description: Descripcion del producto (Texto)
    product_price: Precio del producto (Número)
    product_category: Categoría del producto (Texto)
    product_amount: Cantidad  del producto (Número)
    product_category_id(FK): Id de la categoria (Numero)

## Factura(Invoice)
    invoice_id(PK) Primary key (Número)
    invoice_date: Fecha de la factura (Fecha)
    invoice_time: Hora de la factura (Hora)
    invoice_total: Total de la factura (Número)
    invoice_status: Estado de la factura (Texto)
    invoice_client_id(FK): Id del cliente (Número)

## Cliente(Client)
    client_id(PK) Primary key (Número)
    client_name: Nombre del cliente (Texto)
    client_address: Dirección del cliente (Texto)
    client_phone: Número de telefono del cliente (Texto)
    client_email: Correo electrónico del cliente (Texto)
    client_invoice_id: Id  de la factura (Número)

## Empleados(Staff)
    staff_id(PK) Primary key (Número)
    staff_name: Nombre del empleado (Texto)
    staff_invoice_id(FK): Id de la factura (Número)

## Proveedores(Provider)
    provider_id(PK) Primary key (Número)
    provider_name: Nombre del proveedor (Texto)
    provider_address: Dirección del proveedor (Texto)
    provider_phone: Número de telefono del proveedor (Texto)
    provider_email: Correo electrónico del proveedor (Texto)
    provider_product_id: Id del producto (Número)

## Pagos(Payment)
    payment_id(PK) Primary key (Número)
    payment_date: Fecha de pago (Fecha)
    payment_metod: Método de pago (Texto)
    payment_amount: Monto del pago (Número)
    payment_invoice_id(FK): Id de la factura (Número)
    payment_product_id(FK): Id del producto (Numero)
    payment_client_id(FK): Id del cliente (Número)

## Categorias(Category)
    category_id(PK) Primary key (Número)
    category_name: Nombre de la categoria (Texto)
    category_description: Descripcion de la categoria (Texto)
