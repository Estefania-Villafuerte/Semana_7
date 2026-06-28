# Sensor Puyo - Control ambiental

Sistema WinForms para registrar estaciones IoT y lecturas de temperatura y humedad de la ciudad de Puyo.

## Modulos

- Autenticacion por usuario y contrasena.
- Menu superior filtrado por rol.
- Administracion de usuarios.
- Inventario de sensores y estaciones.
- Historial de mediciones ambientales.
- Auditoria de intentos sin autorizacion.
- Inicializacion del esquema MySQL.

## Requisitos

1. Visual Studio 2022 o posterior con Desarrollo de escritorio de .NET.
2. MAMP con MySQL disponible en `127.0.0.1:3306`.

## Inicio

1. Encienda MySQL en MAMP.
2. Abra `Sensor Puyo Control.slnx`.
3. Compruebe los datos de conexion en `MonitoreoAmbiental.WinForms/appsettings.json`.
4. Ejecute con `Ctrl+F5`.

Esta variante trabaja con la base `sensores_puyo_control`. El archivo `scripts/database.sql` permite crearla manualmente desde phpMyAdmin.

## Usuarios de demostracion

| Usuario | Contrasena | Rol |
|---|---|---|
| `admin` | `Admin123*` | Admin |
| `operador` | `Opera123*` | Operador |
| `consulta` | `Consulta123*` | Consulta |

## Alcance de cada rol

| Modulo | Admin | Operador | Consulta |
|---|:---:|:---:|:---:|
| Usuarios | CRUD | Sin acceso | Sin acceso |
| Dispositivos | CRUD | CRUD | Lectura |
| Mediciones | CRUD | Crear y editar | Lectura |
| Auditoria | Lectura | Sin acceso | Sin acceso |

Las evidencias visuales estan en `evidencias/`.

