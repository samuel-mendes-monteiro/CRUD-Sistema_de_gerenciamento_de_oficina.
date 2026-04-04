Sistema de Gestão de Veículos (C)
Descrição

Este projeto é um sistema simples de gerenciamento de veículos desenvolvido em linguagem C. Ele permite cadastrar, buscar, editar, remover e listar veículos utilizando armazenamento em arquivo texto.

Os dados são persistidos em um arquivo chamado:

banco-de-dados-oficina.txt
Funcionalidades

O sistema possui as seguintes opções no menu:

Pesquisar veículo
Busca um veículo pela placa.
Editar veículo
Permite atualizar os dados de um veículo existente.
Adicionar veículo
Cadastra um novo veículo no sistema.
Remover veículo
Remove um veículo a partir da placa.
Listar veículos
Exibe todos os veículos cadastrados.
Sair
Encerra o programa.
Estrutura dos Dados

Cada veículo possui os seguintes atributos:

Modelo (string)
Ano (int)
Placa (string)
Troca de óleo (int: 0 ou 1)
KM da última revisão (int)
KM atual (int)

Os dados são armazenados no arquivo em formato texto, separados por espaço:

modelo ano placa trocaoleo km_ultimarev km_atual

Exemplo:

CIVIC_2020 2020 ABC1234 1 10000 21000
Como Compilar

Use um compilador C como o GCC:

gcc main.c -o programa
Como Executar

Após compilar:

./programa
Observações
O modelo do carro tem espaços substituídos por underscore (_) para facilitar leitura no arquivo.
A placa é convertida automaticamente para letras maiúsculas.
O sistema utiliza um arquivo temporário (temp.txt) para operações de edição e remoção.
O programa faz uso de leitura com fscanf, portanto o formato do arquivo deve ser respeitado.
Possíveis Melhorias
Validação de entrada de dados
Interface mais amigável
Uso de arquivos binários para maior eficiência
Sistema de busca por outros campos (modelo, ano, etc.)
Ordenação dos veículos