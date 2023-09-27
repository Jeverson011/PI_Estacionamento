# PI_Estacionamento

Neste trabalho acadêmico, descreveremos a estrutura do banco de dados que foi projetada para atender aos requisitos de um sistema de estacionamento. O banco de dados consiste em quatro tabelas principais: Pessoas, Funcionário, Cliente e Veículo. Cada tabela é projetada para armazenar informações específicas relacionadas a pessoas, funcionários, clientes e veículos envolvidos no sistema de estacionamento.

1. Introdução
Afim de agregar qualidade ao serviço de pequenos empresarios, pensamos em desenolver um sistema que controla a entrada, saida e ganhos de um estacionamento.

2. Descrição das Tabelas
2.1. Tabela Pessoas



A tabela Pessoas é projetada para armazenar informações pessoais, como nome, CPF, email e telefone das pessoas envolvidas no sistema de estacionamento.

- Nome (VARCHAR): Armazena o nome da pessoa.
- CPF (VARCHAR): Armazena o número de CPF da pessoa.
- Email (VARCHAR): Armazena o endereço de e-mail da pessoa.
- Telefone (VARCHAR): Armazena o número de telefone da pessoa.
2.2. Tabela Funcionário



A tabela Funcionário registra informações sobre os funcionários do estacionamento.

- Registro (VARCHAR): Serve como chave primária e armazena o registro único do funcionário.
- IdFuncionário (INTEGER): Armazena um identificador único para cada funcionário.
2.3. Tabela Cliente



A tabela Cliente armazena informações sobre os clientes que utilizam o estacionamento.

- IdCliente (INTEGER): Serve como chave primária e armazena um identificador único para cada cliente.
2.4. Tabela Veículo



A tabela Veículo registra informações sobre os veículos que entram no estacionamento.

- IdCarro (INTEGER): Serve como chave primária e armazena um identificador único para cada veículo.
- Modelo (VARCHAR): Armazena o modelo do veículo.
- Placa (VARCHAR): Armazena a placa do veículo.
- Cor (VARCHAR): Armazena a cor do veículo.
2.5. Tabela Estacionamento



A tabela Estacionamento registra as atividades de estacionamento, incluindo a associação de funcionários, clientes e veículos a vagas específicas.

- IdFuncionário (INTEGER): Armazena o identificador do funcionário responsável pelo registro.
- IdCliente (INTEGER): Armazena o identificador do cliente associado à vaga.
- IdCarro (INTEGER): Armazena o identificador do veículo estacionado.
- NumeroDeVaga (INTEGER): Serve como chave primária e armazena o número da vaga.
- EntradaDeVeículo (INTEGER): Armazena o horário de entrada do veículo.
- SaidaDeVeículo (INTEGER): Armazena o horário de saída do veículo.
- ValorTotal (DOUBLE PRECISION): Armazena o valor total a ser pago pelo cliente.


-- Tabela Pessoas
CREATE TABLE Pessoas (
    Nome VARCHAR(100),
    CPF VARCHAR(11),
    Email VARCHAR(90),
    Telefone VARCHAR(15)
);

-- Tabela Funcionario
CREATE TABLE Funcionario (
    Registro VARCHAR(20) PRIMARY KEY,
    IdFuncionario INTEGER
);

-- Tabela Cliente
CREATE TABLE Cliente (
    IdCliente INTEGER PRIMARY KEY
);

-- Tabela Veiculo
CREATE TABLE Veiculo (
    IdCarro INTEGER PRIMARY KEY,
    Modelo VARCHAR(255),
    Placa VARCHAR(10),
    Cor VARCHAR(50)
);

-- Tabela Estacionamento
CREATE TABLE Estacionamento (
    IdFuncionario INTEGER,
    IdCliente INTEGER,
    IdCarro INTEGER,
    NumeroDeVaga INTEGER PRIMARY KEY,
    EntradaDeVeiculo INTEGER,
    SaidaDeVeiculo INTEGER,
    ValorTotal DOUBLE PRECISION
);




