# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-2
1. Configuración Inicial y Base de Datos
Se establece la codificación a UTF8 y se configura el esquema público por defecto.

Se define la creación de la base de datos principal llamada vuelostripulacionaerolineacomercial utilizando la configuración regional de España (Spanish_Spain.1252).

2. Estructura de las Tablas y sus Campos
El script define la creación de 6 tablas relacionales principales:

avion: Almacena la información de la flota de aeronaves.

numero_matricula: Código o matrícula única del avión (clave primaria).

anio_fabricacion: Año en que fue fabricado.

modelo: Modelo del avión.

autonomia: Autonomía de vuelo (alcance).

capacidad_pasajeros: Número máximo de pasajeros que puede transportar.

vuelo: Contiene los detalles operativos de los trayectos programados.

id_vuelo: Identificador único del vuelo (clave primaria).

hora_salida y hora_llegada: Horarios programados.

origen y destino: Códigos de los aeropuertos de salida y llegada.

numero_matricula: Referencia al avión asignado para realizar el vuelo.

empleado: Registra al personal de la aerolínea (tripulación y personal operativo).

numero_empleado: Identificador único del empleado (clave primaria).

nombre y apellido: Datos personales.

dni: Documento de identidad.

categoria_profesional: Rol o categoría (ej. piloto, copiloto, tripulante de cabina).

fecha_ingreso: Fecha en la que comenzó a trabajar en la empresa.

asignacion_vuelo: Tabla intermedia que vincula a los empleados con los vuelos en los que participan.

id_vuelo y numero_empleado: Claves foráneas compuestas.

rol: Función específica que desempeña el empleado en ese vuelo en particular.

pasajero: Almacena los datos de los clientes que viajan.

id_pasajero: Identificador único del pasajero (clave primaria).

nombre y apellido: Datos personales.

nacionalidad: Nacionalidad del pasajero.

dni: Documento de identidad.

fecha_nacimiento: Fecha de nacimiento.

reserva: Gestiona las reservas de asientos realizadas por los pasajeros para determinados vuelos.

id_reserva: Identificador único de la reserva (clave primaria).

numero_asiento: Asiento asignado.

estado: Estado de la reserva (ej. confirmada, cancelada).

id_vuelo y id_pasajero: Claves foráneas que relacionan la reserva con el vuelo y el pasajero correspondientes.

3. Restricciones y Claves
Claves Primarias (PRIMARY KEY): Se configuran en cada tabla para garantizar la unicidad de los registros (por ejemplo, avion_pkey, vuelo_pkey, empleado_pkey, reserva_pkey, etc.).

IMAGEN DE EJEMPLO DE UNA CONSULTA:
<img width="1167" height="373" alt="image" src="https://github.com/user-attachments/assets/f392b3d7-678f-4d0f-afee-7851c50e72cf" />


Claves Foráneas (FOREIGN KEY): Se establecen para mantener la integridad referencial del sistema (vinculando los vuelos con sus aviones, las asignaciones de vuelo con los empleados y vuelos, y las reservas con los vuelos y pasajeros).
