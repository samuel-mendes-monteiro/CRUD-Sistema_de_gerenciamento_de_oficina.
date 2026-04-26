

Sistema de Gestão de Veículos / Vehicle Management System (C)


### Português

Visão Geral

Este projeto é um sistema simples de gerenciamento de veículos desenvolvido em C. Ele permite cadastrar, consultar, editar, remover e listar veículos utilizando um arquivo .txt como armazenamento.

Funcionalidades
Pesquisar veículo por placa
Editar informações de um veículo
Adicionar novo veículo
Remover veículo
Listar todos os veículos cadastrados
Estrutura do Projeto

.
├── main.c
├── functions.c
├── functions.h
├── banco-de-dados-oficina.txt
└── README.md

main.c → Controle principal do programa (menu e fluxo)
functions.c → Implementação das funções
functions.h → Declaração das funções e estrutura Veiculo
banco-de-dados-oficina.txt → Arquivo de armazenamento dos dados
Estrutura de Dados

Cada veículo é representado por:

typedef struct {
    char modelo[50];
    int ano;
    char placa[15];
    int trocaoleo;
    int km_ultimarev;
    int km_atual;
} Veiculo;
Compilação
gcc main.c functions.c -o programa
Execução
./programa
Armazenamento de Dados

Os dados são armazenados em:

banco-de-dados-oficina.txt

Formato:

modelo ano placa trocaoleo km_ultimarev km_atual

Exemplo:

CIVIC_2020 2020 ABC1234 1 10000 21000


Observações:
O modelo do carro não pode conter espaços (eles são convertidos para _)
A placa é automaticamente convertida para letras maiúsculas
O sistema utiliza um arquivo temporário (temp.txt) para edição e remoção
Evite editar o arquivo manualmente para não causar inconsistências
Possíveis Melhorias
Interface gráfica
Validação de entrada mais robusta
Suporte a múltiplos usuários
Integração com banco de dados (SQLite, por exemplo)
Melhor tratamento de erros





### ENGLISH

Overview

This project is a simple vehicle management system developed in C. It allows users to add, search, edit, remove, and list vehicles using a .txt file as storage.

Features
Search vehicle by license plate
Edit vehicle information
Add new vehicle
Remove vehicle
List all registered vehicles
Project Structure
.
├── main.c
├── functions.c
├── functions.h
├── banco-de-dados-oficina.txt
└── README.md
main.c → Main program flow and menu
functions.c → Function implementations
functions.h → Function declarations and Veiculo struct
banco-de-dados-oficina.txt → Data storage file
Data Structure

Each vehicle is represented by:

typedef struct {
    char modelo[50];
    int ano;
    char placa[15];
    int trocaoleo;
    int km_ultimarev;
    int km_atual;
} Veiculo;
Compilation
gcc main.c functions.c -o program
Execution
./program
Data Storage

Data is stored in:

banco-de-dados-oficina.txt

Format:

modelo ano placa trocaoleo km_ultimarev km_atual

Example:

CIVIC_2020 2020 ABC1234 1 10000 21000

Notes:

Car model names cannot contain spaces (spaces are replaced with _)
License plates are automatically converted to uppercase
A temporary file (temp.txt) is used for editing and removing records
Avoid manually editing the data file to prevent inconsistencies
Possible Improvements
Graphical interface
Better input validation
Multi-user support
Database integration (e.g., SQLite)
Improved error handling


Autor

Samuel Mendes
