# Banco de Dados

## Ìndice

* B.D = BANCO DE DADOS
* S.B.D = SISTEMA DE BANCO DE DADOS
* S.G.B.D = SISTEMA DE GERÊNCIAMENTO DE BANCO DE DADOS
* D.D = DICIONARIO DE DADOS, CATÁLOGO OU METADADOS
* D.B.A = ADMINISTRADOR DE BANCO DE DADOS
* SQL = LINGUAGEM DE CONSULTA(QUERY) ESTRUTURAVEL
* CHAVE PRIMARIA(BUSCAR ENTENDER MELHOR) = IDENTIFICADO UNICO DA TABELA
* DADO = DADOS SÃO FATOS BRUTOS QUE NÃO FORAM SUBMETIDOS A NENHUM PROCESSAMENTO DE MODO A MOSTRAR SEU REAL SIGNIFICADO
* INFORMAÇÃO = A INFORMAÇÃO É O PROCESSAMENTO DE DADOS BRUTOS PARA REVELAR O SEU SIGNIFICADO
* COMANDOS ATOMICOS = SO PODEM SER REALIZADOS UMA UNICA VEZ

## Estrutura de um Sistema de Banco de Dados(SBD)

<h3 align="center">S.B.D(Usuarios -> Aplicações -> (IF ANY PROBLEM D.B.A ->) S.G.B.D <-> B.D - D.D)</h3>
<br></br>


![SBD Model](https://bookdown.org/labxss/coorte_adm2/sgbd.png)



## Prática 1 - Modelagem B.D de RH

### Projeto Lógico:

nome(DNOME), numero de departamento(DEPTNO) e localização do departamento(LOC) <- **dept(departamento)** --RELAÇÃO-- **empregados**

### Etapas:

- [x] Criar tabela
- [x] Colocar a PK(primary key)
- [x] Inserir os dados
- [x] Consultar os dados


### COMANDOS:

1. Criar tabela
```
CREATE TABLE DEPT
(DEPTNO NUMBER(2, 0) NOT NULL,
DNAME VARCHAR2(20), LOC VARCHAR2(13))
```
2. Visualizar a tabela
```
DESC DEPT
```
3. Colocar a chave primaira
```
ALTER TABLE DEPT
ADD CONSTRAINT PK_DEPT PRIMARY KEY (DEPTNO)
USING INDEX
```
4. Inserir dados na tabela
> Command 1
```
INSERT INTO DEPT
VALUES
(10, 'ENGENHARIA', 'BELÉM')
```
> Command 2
```
INSERT INTO DEPT
VALUES
(20, 'COMPUTAÇÃO', 'IPIXUNA')
```
5. Selecionar todos os dados da tabela
```
SELECT *
FROM DEPT
```
6. Testar pk(chave primaria)
> O resultado tem que ser um erro
```
INSERT INTO DEPT
VALUES
(10, 'BUSINESS, 'NEW YORK')
```
> Adicionar valor valido
```
INSERT INTO DEPT
VALUES
(30, 'BUSINESS', 'NEW YORK')
```
7. Criar tabela de empregados
```
CREATE TABLE emp
    (empno NUMBER(4, 0) NOT NULL,
    ename   VARCHAR2(10),
    job VARCHAR2(9),
    mgr NUMBER(4, 0),
    hiredate    DATE,
    sal NUMBER(7, 2),
    comm    NUMBER(7, 2),
    deptno NUMBER(2, 0))
```
8. Verificar tabela emp
```
DESC emp
```
9. Criar as Constraints(restrições) da tabela emp
```
ALTER TABLE emp
ADD CONSTRAINT pk_emp PRIMARY KEY (empno)
USING INDEX
```
10. Criar foreing key(fk)
```
ALTER TABLE emp
ADD CONSTRAINT fk_deptno FOREIGN KEY (deptno)
REFERENCES dept (deptno)
```



oracle apex keys:

Workspace:	vmoreira
Username:	vmoreira021@gmail.com
Environment:	https://apex.oracle.com/pls/apex/
