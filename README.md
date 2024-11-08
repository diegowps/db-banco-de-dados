---
icon: arrow-down-to-square
cover: >-
  https://images.unsplash.com/photo-1728266601727-64b2c27d01ef?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3MzEwMjAxMTd8&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Banco de dados - SQL

07/11 - quinta-feira

DDL - Definição

Data Definition Language

&#x20; _->create database_

&#x20; _->create table_

DML - Manipulação

Data Definition Language

&#x20;_->insert into_

DQL - Solicitações

\>>>>>>>>>>>>>>>>>>>>>

`create database cadastro default character set utf8 default collate utf8_general_ci;`

`use cadastro;`

`create table pessoas( id int not null auto_increment, nome varchar (50) not null, Nascimento date, sexo enum ('F', 'M', 'O'), peso decimal(5,2), altura decimal (3,2), nacionalidade varchar (20) default 'Brasil', primary key (id) ) default charset = utf8;`

`describe pessoas;`

`drop table pessoas;`

`insert into pessoas(id, nome, nascimento, sexo, peso, altura, nacionalidade) values ('1', 'Amanda', '1997-10-21', 'F', '60', '1.57', 'Brasileira');`

`select * from pessoas;`

`insert into pessoas(nome, nascimento, sexo, peso, altura, nacionalidade) values ('Bruno', '1997-08-12', 'M', '95', '1.68', 'Brasileiro');`

`insert into pessoas values (default, 'Diego', '1994-12-05', 'M', '90', '1.65', 'Brasileiro');`

`/`_`Inserindo dados na tabela`_`/ insert into pessoas (nome, nascimento, sexo, peso, altura, nacionalidade) values ('diego', '2021-10-27', 'f', '58.5', '1.57', 'brasil'); insert into pessoas values (default, 'Adriano', '1957-08-01', 'M', '84.5', '1.89', default);`

`select * from pessoas;`

`insert into pessoas (id, nome, nascimento, sexo, peso, altura, nacionalidade) values (default, 'Leandro Ramos', '1979-04-02', 'm', '90.5', '1.87', 'Portugal'), (default, 'Robson Vaamonde', '1979-07-02', 'm', '80,5', '1,77', 'Italia'), (default, 'Jose Assis', '1969-04-15', 'm', '60,5', '1,57', 'Portugal');`

`/`_`alterar estrutura da tabela`_`/ alter table pessoas add column profissao varchar(10);`

`desc pessoas; select * from pessoas;`









características semelhantes

nome idade sexo peso altura nacionalidade

***

/\*Criando do banco \*/ create database if not exists cadastro default character set utf8 default collate utf8\_general\_ci;

/_Criando tabela_/ create table if not exists cursos( idcursos int not null auto\_increment, nome varchar(30) not null unique, descricao text, carga int unsigned, totalaulas int, ano year default '2024', primary key (idcursos) )default charset = utf8;

create table if not exists alunos( id int not null auto\_increment, nome varchar(80) not null, profissao varchar(50), nacimento date, sexo enum('F','M'), peso decimal(5,2), altura decimal(3,2), nacionalidade varchar(30) default 'Brasil', primary key (id) )default charset = utf8;

insert into alunos value (default,'Andres Cristian Yapiticona Flores' , 'Engenheiro Civil' , '2004-05-09' , 'M' , '62.3' , '1.75' , 'Brasil'), (default,'Edinaldo Pereira de Barros' , 'Administrador' , '1979-02-12' , 'M' , '85' , '1.90' , 'Brasil'), (default,'Érica da Silva Pires' , 'Contadora' , '1993-10-25 ','F' ,' 67' , '1.75' , 'Espanha'), (default,'Erick Luan Ferreira' , 'Astronauta' , '1999-11-02' ,'M', '79.9' , '1.69' , 'Brasil'), (default,'Gabriela Gomes Da Silva' , 'Advogada' , '2003-12-12' ,'F' , '48' , '1.62' , 'Italia'), (default,'Gabriel Rodrigues Dos Santos' , 'Administrador' , '2002-07-20' , 'M', '100' , '1.85' , 'Portugal'), (default,'Gustavo Pinheiro Leite' , 'Analista de Dados' , '2003-12-22' , 'M' , '62' , '1.68' , 'Brasil'), (default,'Gustavo Teodoro Gabilan' , 'Programador' , '2005-01-21' , 'M' ,' 47' , '1.65' , 'Brasil'), (default,'Julia Picole Turubia' , 'Veterinaria' , '2004-10-01' , 'F' ,' 58 ', '1.62' , 'Italia'), (default,'Luiz Henrique Da Silva Costa' , 'Desenvolvedor FrontEnd' ,'2005-04-18','M' , '97' , '1.78' , 'Brasil'), (default,'Millena Gutemberg Dos Santos Silva' , 'Modelo' , '2003-05-22' , 'F' , '62.5' , '1.65' , 'Brasil'), (default,'Paulo Nicolas dos Santos' , 'Vendedor ',' 2003-04-29' , 'M' , '65.5' ,' 1.89' , 'Brasil'), (default,'Pedro Henrique' , 'Programador' , '2002-05-25' ,'M', '70' , '1.79' , 'Espanha'), (default,'Ryan Gomes dos Santos' , 'Uber' , '2005-09-09' ,'M', '62' , '1.82' , 'Portugal'), (default,'Vinicius de Souza Nascimento' , 'Vendedor' , '1996-08-18' , 'M' , '67' ,' 1.75' , 'Portugal'), (default,'Vitor Fialho Bergami' , 'Lutador' , '1998-01-25' , 'M' ,' 75' , '1.85' , 'Nova Zelândia'), (default,'Weslley Carlos Gonçalves da Silva' ,' Administrador' , '2005-06-04' , 'M' , '75' , '1.80' , 'Canada'), (default,'Weslley Moreira Nascimento Da Silva' , 'Analista de dados' , '2006-06-12' , 'M' , '70' , '1.83' , 'Brasil'), (default,'Sirlene Sanches' , 'Professor' , '1979-08-10' ,'F', '60.5' , '1.56 ', 'Espanha'), (default,'José de Assis' , 'Professor' , '1970-04-10' ,'M', '65.8' , '1.57 ', 'Portugal'), (default,'Leandro Ramos' , 'Professor' , '1979-04-02' ,'F', '95.8' , '1.85' , 'Canadá'), (default,'Robson Vaamonde' , 'Professor' , '1979-07-02' ,'M', '78.9' , '1.72' , 'Itália');

insert into cursos value (default, 'Algoriitimos', 'Lógica de programação. Você aprenderá sobre o desenvolvimento de soluções com apl', '40', '10', default), (default, 'Exel Essencl', 'Você aprenderá a criar planilhas e tabelas, fazer gráficos simples, além de salvar arquivos em nuvem e realizar cálculos usando fórmulas e funções de Excel básico.', '2', '10', default), (default, 'Excel Avançado I', 'Você aprofundará conhecimentos em funções do Excel avançado para otimizar cálculos e facilitar a construção de planilhas, banco de dados, relatórios e gráficos.', '24', '6', default), (default, 'Excel Avançado II', 'Você saberá mais sobre ferramentas avançadas e em recursos de banco de dados no Excel para automatizar tarefas e aprimorar consultas, relatórios, gráficos e cálculos.', '24', '6', default), (default, 'Form Excel: do básico ao avançado', 'Você aprenderá a inserir informações em planilhas, usando recursos, funções e ferramentas avançadas do Excel 365 para criar gráficos, fazer cálculos e manipular dados.', '72', '1', '2025'), (default, 'Desenvvidor Web Front-end 1', 'Você aprenderá a planejar e desenvolver sites responsivos com imagens.', '60', '15', '2025'), (default, 'Desenvolvedor GeWeb Front-end 2: JavaScript', ' Você aprenderá como utilizar a codificação JavaScript para criar e usar recursos básicos de interatividade em um site.', '40', '12', '2023'), (default,'PHP com MySQL', 'Você aprenderá a desenvolver sistemas computacionais e websites com recursos da linguagem de programação PHP e do gerenciador de banco de dados MySQL.', '40', '12', '2023'), (default,'Lógica de Programação Direcionada a PHP', 'Você aprenderá a criar algoritmos e desenvolver aplicações e sistemas web com a linguagem de programação PHP.', '40', '12', '2023'), (default,'PHP', 'Você aprenderá a desenvolver sistemas computacionais e websites com recursos da linguagem de programação PHP.', '24', '6', '2023'), (default,'PHP4', 'Você aprenderá a desenvolver sistemas computacionais e websites com recursos da linguagem de programação PHP.', '32', '8', '2025'), (default,'Photoshop', 'Você aprenderá como tratar, manipular e editar imagens, utilizando filtros, cores, efeitos de camada e demais recursos do Adobe Photoshop.', '36', '9', '2025'), (default,'Photoshop para Mídias Sociais', 'Você aprenderá técnicas de criação, edição, composição e exportação de conteúdo gráfico para mídias sociais, utilizando recursos e ferramentas do Adobe Photoshop.', '36', '9', '2025'), (default,'Python','Você aprenderá a desenvolver programação web por meio da linguagem Python.', '32', '8', '2025'), (default,'Python I - fundamentos', 'Você aprenderá a desenvolver programação web por meio da linguagem Python, que possibilita a pesquisa e a extração de dados de páginas da internet.', '44', '11', '2024'), (default,'Python II - desenvolvendo aplicações web', 'Você aprenderá a desenvolver soluções para a web aplicando linguagem Python em framework de projetos de software e a manipular banco de dados.', '60', '15', '2024'), (default,'Introdução à Linguagem Java', 'Você aprenderá a programar aplicações básicas com a linguagem Java.', '40', '10', '2023'), (default,'Formação Front-end', 'Você aprenderá a planejar e produzir site com imagens, linguagem HTML5, CSS3 e Web Semântica usando codificação JavaScript.', '108', '27', '2026'), (default,'Desenvolvedor Web Back-end: NodeJs', 'Você aprenderá a configurar ambiente Node.js, desenvolvendo código JavaScript e executando no back-end. Também criará APTI Rest para acessar banco de dados e atender requisições HTTPs.', '48', '12', '2026'), (default,'POO', 'Curso de Programação Orientada ao Objeto', '60', '15', '2022'), (default,'C++', 'Curso de C++', '40', '10', '2023'), (default,'C#', 'Curso de C#', '24', '6', '2023'), (default,'PowerPoint', 'Curso completo de PowerPoint', '24', '6', '2023'), (default,'Word', 'Curso completo de Word', '24', '6', '2023'), (default,'Pacote Office', 'Curso de Word, PowerPoint e Excel', '60', '15', '2024'), (default,'Hardware', 'Curso de Montagem e Manutenção de Computadores', '36', '9', '2021'), (default,'Redes', 'Curso de Redes para Iniciantes0', '40', '10', '2021'), (default,'Segurança da Informação', 'Curso de Segurança', '16', '4', '2021');



Tipos primitivos

Númerico: inteiro: TinyInt, SmallInt, Int, MediumInt, BigInt real: decimal, float, double, real lógico: bit, boolean

Data/tempo: data, dateTime, TimeStamp, Time, Year

Literal: caractere: char, varchar texto: TinyText, Text, MediumText, LongText binário: TinyBlob, Blob, MediumBlob, LongBlob coleção: enum, set

Espacial: Geometry, Point, Polygon, MultiPlygon

***

DDL: Date Definition Language CREATE DATABASES CREATE TABLE ALTER TABLE DROP TABLE DROP DATABASES

DML: Data Manipulation Language INSERT INTO UPDATE DELETE TRUNCATE

DQL - Data Query Language SELECT
