Create database DBAPI

use DBAPI

create table CATEGORIA(
IdCategoria int primary key identity(1,1),
Descripcion varchar(50)
)

create table PRODUCTO(
IdProducto int primary key identity(1,1),
CodigoBarra varchar(20),
Descripcion varchar(50),
Marca varchar(50),
IdCategoria int,
Precio decimal(10,2)
constraint FK_IDCATEGORIA foreign key (IdCategoria) references CATEGORIA(IdCategoria)
)

insert into CATEGORIA(Descripcion) values
('Tecnologia'),
('ElectroHogar'),
('Accesorios')



insert into PRODUCTO(CodigoBarra,Descripcion,Marca,IdCategoria,Precio) values
('50910010','Monitor Aoc - Curvo Gaming','AOC',1,1200),
('50910012','Lavadora 21 KG WLA-21','WINIA',2,1749)

select * from CATEGORIA
select * from PRODUCTO
