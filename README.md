# BaseDeps
DROP DATABASE ImportacionDB;

CREATE DATABASE ImportacionDB;

USE ImportacionDB;

create table departamentos(
	id_departamento int primary key AUTO_INCREMENT,
	nombreDepartamento varchar(40) not null
);

create table municipios(
	id_municipio int primary key AUTO_INCREMENT,
	nombre_municipio varchar(40) NOT NULL, 
	id_departamento INT,
	FOREIGN KEY (id_departamento) 
	REFERENCES departamentos(id_departamento)
);
