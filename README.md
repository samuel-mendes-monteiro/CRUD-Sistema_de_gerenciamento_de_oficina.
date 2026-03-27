 Sistema de Gestão de Veículos em C
 Descrição:

Este projeto é um sistema simples de gestão de veículos desenvolvido em linguagem C.
Ele permite cadastrar, buscar e remover veículos utilizando armazenamento em arquivo texto, simulando um banco de dados.

O sistema segue o conceito de CRUD (Create, Read, Update, Delete), sendo um projeto voltado para prática de lógica de programação e manipulação de arquivos.

-Funcionalidades-
 Adicionar veículo
Cadastro de modelo, ano, placa, status de troca de óleo e quilometragem
 Pesquisar veículo
Busca por placa
Exibe todas as informações do veículo
 Remover veículo
Exclusão baseada na placa
Utiliza arquivo temporário para reescrita dos dados
 Atualização do status do veiculo
Atualiza o veiculo na oficina
 Sair do sistema
Encerramento controlado do programa


 Estrutura do Projeto

O sistema utiliza uma estrutura (struct) para representar os veículos:

typedef struct {
    char modelo[50];
    int ano;
    char placa[15];
    int trocaoleo;
    int km_ultimarev;
    int km_atual;
} Veiculo;
 Armazenamento

Os dados são armazenados no arquivo:

banco-de-dados-oficina.txt

Cada linha representa um veículo, com os dados separados por espaço.

 Tecnologias Utilizadas
Linguagem C
Biblioteca padrão (stdio.h, string.h, time.h, ctype.h)
Manipulação de arquivos (FILE, fopen, fprintf, fscanf)
 Funcionamento

O programa apresenta um menu interativo:

1 - Pesquisar veiculo
2 - Editar status de veiculo
3 - Adicionar veiculo
4 - Remover veiculo
0 - Sair

O sistema permanece em execução até o usuário escolher sair.

 Tratamento de Dados
Uso de fgets para leitura segura de strings
Remoção do \n com strcspn
Padronização de placas em letras maiúsculas (toupper)
Comparação de strings com strcmp
▶ Como executar
1. Compilar
gcc main.c -o sistema
2. Executar
./sistema
 Conceitos Praticados
Estruturas (struct)
Manipulação de arquivos
Strings em C
Controle de fluxo (switch, do-while)
Funções
Entrada e saída de dados
CRUD básico

 Autor

Desenvolvido por Samuel Mendes

📌 Observação

Este projeto foi desenvolvido com foco educacional, visando reforçar conceitos fundamentais da linguagem C e servir como base para projetos mais avançados.