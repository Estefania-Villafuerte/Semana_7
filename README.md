# Sensor Puyo - Consola de Operaciones

Aplicación WinForms para la gestión y monitoreo de estaciones ambientales de temperatura y humedad en Puyo

## Contenido

- Inicio de sesión con roles **Admin**, **Operador** y **Consulta**.
- Gestión de usuarios, estaciones y mediciones.
- Control de permisos según el rol.
- Registro de auditoría de accesos.
- Conexión a MySQL.
- Script SQL para crear la base de datos.
- Integración con Arduino y sensor DHT11.

## Requisitos

- Visual Studio 2022 o superior.
- .NET 8 Desktop Runtime.
- MySQL (MAMP o XAMPP).

## Ejecución

1. Iniciar el servidor MySQL.
2. Ejecutar el script `scripts/database.sql`.
3. Configurar la conexión en `appsettings.json`.
4. Abrir la solución y ejecutar el proyecto.

## Accesos

| Usuario | Contraseña | Rol |
|----------|------------|-----|
| admin | Admin123* | Admin |
| operador | Opera123* | Operador |
| consulta | Consulta123* | Consulta |

## Permisos

| Función | Admin | Operador | Consulta |
|----------|:-----:|:---------:|:---------:|
| Usuarios (CRUD) | Sí | No | No |
| Consultar dispositivos | Sí | Sí | Sí |
| Modificar dispositivos | Sí | Sí | No |
| Consultar mediciones | Sí | Sí | Sí |
| Crear y editar mediciones | Sí | Sí | No |
| Eliminar mediciones | Sí | No | No |
| Auditoría | Sí | No | No |

Las capturas del proyecto se encuentran en la carpeta `evidencias/`.
