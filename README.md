# CRUD-prueba-laravel
El Modelo de la base de datos sería éste:

Tabla usuarios(pacientes)
Create table usuarios(
id bigint auto_increment,
clave text,
nombres text,
apellidos text,
fechanacimiento date,
correo text,
telefono text,
PRIMARY KEY(id)
)

Tabla Medicos
Create table medicos(
idmedico bigint auto_increment,
nombres text,
apellidos text,
dni text,
correo text,
PRIMARY KEY(idmedico)
)

Tabla Especialidades
Create table especialidades(
idespecialidad bigint auto_increment,
nombre text,
PRIMARY KEY (idespecialidad)
)

Tabla MedicosEspecialidades
Crate table MedicosEspecialidades(
idmedico int,
idespecialidad int,
PRIMARY KEY(idmedico,idespecialidad),
FOREIGN KEY(idmedico) REFERENCES medicos(idmedico),
FOREIGN KEY(idespecialidad) REFERENCES especialidades(idespecialidad)
)
