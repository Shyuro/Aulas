# Banco de Dados

## Ìndice

* B.D = BANCO DE DADOS
* S.B.D = SISTEMA DE BANCO DE DADOS
* S.G.B.D = SISTEMA DE GERÊNCIAMENTO DE BANCO DE DADOS
* D.D = DICIONARIO DE DADOS, CATÁLOGO OU METADADOS
* D.B.A = ADMINISTRADOR DE BANCO DE DADOS
* SQL = LINGUAGEM DE CONSULTA(QUERY) ESTRUTURAVEL
* CHAVE PRIMARIA(BUSCAR ENTENDER MELHOR) = IDENTIFICADO UNICO DA TABELA


## Estrutura de um Sistema de Banco de Dados(SBD)

S.B.D(Usuarios -> Aplicações -> (IF ANY PROBLEM D.B.A ->) S.G.B.D <-> B.D - D.D)


![SBD Model](https://bookdown.org/labxss/coorte_adm2/sgbd.png)



## Prática 1 - Modelagem B.D de RH

### Projeto Lógico:

<sub> nome(DNOME), numero de departamento(DEPTNO) e localização do departamento(LOC) <- </sub> **dept(departamento)** --RELAÇÃO-- **empregados**

### Etapas:

- [x] Criar tabela
- [x] Colocar a PK(primary key)
- [x] Inserir os dados
- [x] Consultar os dados


### COMANDOS:

1# Criar tabela
```
CREATE TABLE DEPT
(DEPTNO NUMBER(2, 0) NOT NULL,
DNAME VARCHAR2(20), LOC VARCHAR2(13))
```
2# Visualizar a tabela
```
DESC DEPT
```
3# Colocar a chave primaira
```
ALTER TABLE DEPT
ADD CONSTRAINT PK_DEPT PRIMARY KEY (DEPTNO)
USING INDEX
```











oracle apex keys:

Workspace:	vmoreira
Username:	vmoreira021@gmail.com
Environment:	https://apex.oracle.com/pls/apex/
