-- CREATE DATABASE banking_customer_transactions_analysis;
-- USE banking_customer_transactions_analysis;

CREATE TABLE IF NOT EXISTS clientes (
    cliente_id INT PRIMARY KEY,
    nombre VARCHAR(100),
    edad INT,
    ciudad VARCHAR(100),
    segmento VARCHAR(20),
    fecha_alta DATE
);

CREATE TABLE IF NOT EXISTS cuentas (
    cuenta_id INT PRIMARY KEY,
    cliente_id INT,
    tipo_cuenta VARCHAR(30), -- Caja Ahorro / Cuenta Corriente
    saldo_actual DECIMAL(12,2),
    fecha_apertura DATE,
    FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id)
);

CREATE TABLE IF NOT EXISTS transacciones (
    transaccion_id INT PRIMARY KEY,
    cuenta_id INT,
    fecha DATE,
    tipo VARCHAR(30), -- Deposito / Extraccion / Transferencia / Pago
    monto DECIMAL(12,2),
    canal VARCHAR(30), -- Sucursal / ATM / Online
    FOREIGN KEY (cuenta_id) REFERENCES cuentas(cuenta_id)
);

CREATE TABLE IF NOT EXISTS productos (
    producto_id INT PRIMARY KEY,
    nombre_producto VARCHAR(100),
    categoria VARCHAR(30) -- Tarjeta / Prestamo / Inversion
);

CREATE TABLE IF NOT EXISTS clientes_productos (
    cliente_id INT,
    producto_id INT,
    fecha_contratacion DATE,
    PRIMARY KEY (cliente_id, producto_id),
    FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id),
    FOREIGN KEY (producto_id) REFERENCES productos(producto_id)
);
