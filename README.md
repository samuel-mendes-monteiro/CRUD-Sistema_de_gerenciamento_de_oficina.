Sistema de Gestão de Veículos (C)

Este projeto é um sistema simples de gerenciamento de veículos desenvolvido em linguagem C. Ele permite cadastrar, consultar, editar, remover e listar veículos, utilizando armazenamento em arquivo .txt.

Funcionalidades

O sistema oferece as seguintes operações:

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
banco-de-dados-oficina.txt → Arquivo onde os dados são armazenados
Estrutura de Dados

Cada veículo é representado pela struct:

typedef struct {
    char modelo[50];
    int ano;
    char placa[15];
    int trocaoleo;
    int km_ultimarev;
    int km_atual;
} Veiculo;
Como Compilar

Use o GCC para compilar o projeto:

gcc main.c functions.c -o programa
Como Executar

Após compilar:

./programa
Armazenamento de Dados

Os dados são armazenados no arquivo:

banco-de-dados-oficina.txt

Formato de cada linha:

modelo ano placa trocaoleo km_ultimarev km_atual

Exemplo:

CIVIC_2020 2020 ABC1234 1 10000 21000
Observações
O modelo do carro não pode conter espaços (eles são convertidos para _)
A placa é automaticamente convertida para letras maiúsculas
O sistema utiliza um arquivo temporário (temp.txt) para operações de edição e remoção
Recomenda-se não editar o arquivo manualmente para evitar inconsistências
Possíveis Melhorias
Interface gráfica
Validação mais robusta de entrada
Suporte a múltiplos usuários
Banco de dados (SQLite, por exemplo)
Melhor tratamento de erros


Autor

Samuel Mendes
