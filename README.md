# Análise das Tabelas de Medalhas dos Jogos Olímpicos de Verão (1896-2012)

Este projeto tem como objetivo produzir as tabelas oficiais de medalhas dos Jogos Olímpicos de Verão para todas as edições de 1896 a 2012, utilizando um conjunto de dados bruto contendo mais de 31.000 medalhas e as tabelas oficiais de medalhas para as edições de 1996 e 1976 como referência.

## Objetivo
Minimizar a divergência entre as tabelas de medalhas agregadas produzidas pelo código e as tabelas oficiais para as edições de 1996 e 1976. A divergência é calculada como a diferença absoluta entre o número de medalhas agregadas e o número oficial de medalhas.

## Descrição dos Arquivos
- - **summer.csv**: Conjunto de dados bruto contendo informações sobre mais de 35.000 medalhas dos Jogos Olímpicos de Verão.
  - Fonte: [Link para o arquivo summer.csv]([source/link/to/summer.csv](https://www.kaggle.com/datasets/the-guardian/olympic-games/data))
- **wik_1996.csv**: Tabela oficial de medalhas para a edição de 1996 dos Jogos Olímpicos de Verão.
  - Fonte: [Link para o arquivo wik_1996.csv]([source/link/to/wik_1996.csv](https://pt.wikipedia.org/wiki/Quadro_de_medalhas_dos_Jogos_Olímpicos_de_Verão_de_1996))
- **wik_1976.csv**: Tabela oficial de medalhas para a edição de 1976 dos Jogos Olímpicos de Verão.
  - Fonte: [Link para o arquivo wik_1976.csv]([source/link/to/wik_1976.csv](https://pt.wikipedia.org/wiki/Quadro_de_medalhas_dos_Jogos_Olímpicos_de_Verão_de_1976))

## Metodologia

### Passo 1: Preparação dos Dados

1. Carregar e explorar os dados dos arquivos `summer.csv`, `wik_1996.csv` e `wik_1976.csv`.
2. Limpar e alinhar os dados das tabelas oficiais (`wik_1996` e `wik_1976`) com os dados do arquivo `summer.csv`.

### Passo 2: Criação da Coluna Event_Gender

1. Determinar o gênero do evento (masculino, feminino ou misto) com base na coluna Gender e em regras específicas para eventos mistos.

### Passo 3: Contagem de Medalhas por Evento

1. Identificar todos os eventos únicos e contar a quantidade de medalhas em cada evento, criando a nova coluna `Event_Medals`.

### Passo 4: Identificação de Eventos em Equipe

1. Determinar se um evento é um evento de equipe (mais de 5 medalhas) e criar a coluna `Team`.

### Passo 5: Remoção de Medalhas Duplicadas em Eventos de Equipe

1. Remover duplicatas de medalhas em eventos de equipe, mantendo uma medalha por evento, país e tipo de medalha.

### Passo 6: Criação da Tabela Oficial de Medalhas para Todas as Edições

1. Agregar os dados para formar as tabelas de medalhas para cada edição dos Jogos Olímpicos de Verão de 1896 a 2012.

### Passo 7: Comparação com as Tabelas de Medalhas da Wikipedia

1. Comparar as tabelas de medalhas produzidas com as tabelas oficiais de 1996 e 1976 (`wik_1996.csv` e `wik_1976.csv`) para calcular a divergência total.
2. Ajustar o código para minimizar a divergência, buscando alcançar um "Score" de 0, que indica nenhuma divergência absoluta.

## Resultados
O código gera as tabelas de medalhas para todas as edições dos Jogos Olímpicos de Verão de 1896 a 2012 e calcula a divergência total para as edições de 1996 e 1976.

## Como Executar
Para executar o projeto, siga os passos abaixo:

1. Certifique-se de ter os arquivos `summer.csv`, `wik_1996.csv` e `wik_1976.csv` no mesmo diretório que o notebook.
2. Abra e execute todas as células do notebook `projeto medalhas.ipynb`.
3. Verifique os resultados das tabelas de medalhas geradas e a divergência calculada.

## Requisitos
- Python 3.7+
- Bibliotecas: pandas, numpy

## Contribuições
Sinta-se à vontade para contribuir com melhorias ao projeto. Por favor, envie suas sugestões e melhorias via pull request.

## Autor
Este projeto foi desenvolvido como forma de exercício.
