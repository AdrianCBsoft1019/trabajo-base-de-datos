# trabajo-base-de-datos
## codigo consultas
**consulta 1**

SELECT 
    c.nombre AS Cliente,
    c.documento AS Documento,
    v.fecha AS Fecha_Venta,
    p.nombre AS Producto,
    p.marca AS Marca,
    dv.cantidad AS Cantidad,
    dv.subtotal AS Subtotal
FROM clientes c
INNER JOIN ventas v ON c.id_cliente = v.id_cliente
INNER JOIN detalle_venta dv ON v.id_ventas = dv.id_ventas
INNER JOIN productos p ON dv.id_productos = p.id_productos;

**consulta 2**

SELECT 
    id_productos, 
    nombre, 
    marca, 
    precio, 
    stock
FROM productos
WHERE precio BETWEEN 50000 AND 800000;
