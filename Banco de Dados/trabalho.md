# Alunos

* Rafael Christhyan Borges Moraes
* Vinicius Henrique da Silva Moreira
* Arthur Gabriel Monteiro Sobral

# 1. Levantamento do Ambiente

A economia globalizada tem gerado grandes transformações no setor
farmacêutico. A tendência são as constantes fusões e aquisições das empresas
que buscam alianças para conquistar maior vantagem competitiva e atingir
maiores mercados.  empresas farmacêuticas buscam
conquistar vantagem competitiva através da ampliação de seu portfólio de
lançamento de novos produtos, maior eficiência nas atividades de distribuição e
marketing, e consequentemente ampliação de sua participação no mercado.
a indústria farmacêutica é composta por mais de dez mil empresas, sendo que somente as oito maiores empresas
contribuem com cerca de 40% do faturamento mundial. apenas cem dessas empresas são
responsáveis por cerca de 90% de todos os produtos farmacêuticos produzidos
e destinados ao consumo humano, atendendo cerca de 50% do mercado
mundial, o que pode tornar o mercado mais competitivo, necessitando que as
indústrias busquem desenvolver novas estratégias.
Indústrias farmacêuticas estão diante de sérios desafios na produtividade e
na área de pesquisa e desenvolvimento (P&D), e declínio em seu crescimento.
Por essa razão, as empresas estão buscando melhores estratégias para
estimular a produtividade e o crescimento através de adoção de uma logística
colaborativa.
Neste contexto, a cadeia de suprimentos no setor tem grande importância
devido ao seu nível de complexidade. A produção dos medicamentos apresenta
uma demanda orientada, isto é, o produto é produzido em lotes de acordo com a
demanda. Raramente, a indústria farmacêutica vende seu produto direto para o
consumidor, ela vende para o distribuidor/atacadista, que repassa para os
fornecedores (drogarias e hospitais) e cliente final.
componentes presentes na cadeia de suprimentos da indústria farmacêutica são:
1. Fornecedor de Matéria Prima (ingredientes ativos)
2. Indústria Farmacêutica (Manufatura);
3. Armazéns/Centros de Distribuição; 
4. Distribuidoras;
5. Farmácias e Hospitais
6. Consumidor final
# 2. Diagrama de Entidade e Relacionamento - DER

![Imagem](https://www.imagemhost.com.br/images/2022/11/08/Diagrama-em-branco-1.png)

# 3. Diagrama de Estrutura de Dados - DED

![https://ibb.co/rQ28ZVM](https://www.imagemhost.com.br/images/2022/11/08/DEDDER-quase-1.png)

# 4. Diagrama de Árvore: Formato dos Registros

![This is an image](https://www.imagemhost.com.br/images/2022/11/08/Diagramas-de-arvores.png)



# 5. Criando Tabelas

## Tabela Fornecedor
```
CREATE TABLE FORNECEDOR
(ID_FORNECEDOR SERIAL NOT NULL PRIMARY KEY,
NOME VARCHAR2(30), CNPJ VARCHAR2(14),
TELEFONE VARCHAR(10), ENDERECO VARCHAR(100) NOT NULL)
```

## Tabela Nota_Fiscal
```
CREATE TABLE NOTA_FISCAL
(ID_NOTAFISCAL SERIAL NOT NULL PRIMARY KEY,
NUMERO_NOTA VARCHAR2(44), FORNECEDOR_ID INT,
VALOR MONEY, DATA_CADASTRONOTA DATE)
```
## Tabela Produtos_Nota
```
CREATE TABLE PRODUTOS_NOTA
(ID_PRODUTONOTA SERIAL NOT NULL PRIMARY KEY,
NOTA_FISCAL_ID INT, PRODUTOS_ID INT,
QUANTIDADE_ID INT, LOTE INT)
```

## Tabela Produtos
```
CREATE TABLE PRODUTOS
(ID_PRODUTO SERIAL NOT NULL PRIMARY KEY,
NOME INT, DATA_VALIDADE DATE,
NOME_TIPO VARCHAR(11), DESCRICAO VARCHAR(150),
FABRICANTE VARCHAR(15))
```

## Tabela Estoque
```
CREATE TABLE ESTOQUE
(PRODUTOS_ID_PRODUTO INT NOT NULL,
QUANTIDADE INT, ID_ESTOQUE SERIAL)
```

## Tabela Entrada_Saida
```
CREATE TABLE ENTRADA_SAIDA
(USUARIO_ID INT,
MEDICO_ID INT, ID_ENTRADASAIDA SERIAL NOT NULL PRIMARY KEY,
DATA_HORA TIMESTAMP, TIPO_TRANSACAO VARCHAR(6),
QUANTIDADE INT, PACIENTE_ID INT, PRODUTOS_ID_PRODUTO)
```

## Tabela Usuario
```
CREATE TABLE USUARIO
(ID_USUARIO SERIAL NOT NULL,
PESSOA_ID INT, SENHA VARCHAR(2000) NOT NULL,
LOGIN VARCHAR(50), TIPO VARCHAR(15))
```

## Tabela Paciente
```
CREATE TABLE PACIENTE
(ID_PACIENTE SERIAL NOT NULL PRIMARY KEY,
CARTAO_SUS VARCHAR(15) NOT NULL, PESSOA_ID INT,
PLANO_SAUDE VARCHAR(50))
```

## Tabela Pessoa
```
CREATE TABLE PESSOA
(ID_PESSOA SERIAL NOT NULL PRIMARY KEY,
NOME VARCHAR(50), DATA NASC DATE,
CPF CHAR(11), TELEFONE VARCHAR(11), SEXO VARCHAR(1),
DATA_CADASTRO DATE)
```
## Tabela Medico
```
CREATE TABLE MEDICO
(ID_MEDICO SERIAL NOT NULL PRIMARY KEY,
PESSOA_ID INT, CRM VARCHAR(6))
```


