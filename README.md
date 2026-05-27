# TING (Trybe Is Not Google)

## Sobre o Projeto

O **TING (Trybe Is Not Google)** é uma aplicação em Python que simula um algoritmo de indexação de documentos, semelhante ao utilizado pelo Google. O objetivo principal do programa é permitir a anexação de arquivos de texto (`.txt`) e, posteriormente, operar funções de busca sobre o conteúdo desses arquivos.

O projeto é dividido em dois módulos principais:
1. **Modo de Gerenciamento de Arquivos**: Responsável por ler, processar e gerenciar os arquivos de texto anexados utilizando uma estrutura de dados do tipo Fila (Queue - FIFO).
2. **Modo de Buscas**: Fornece funcionalidades para buscar palavras específicas nos arquivos processados, retornando informações detalhadas sobre as ocorrências.

## Funcionalidades

### Gerenciamento de Arquivos (`ting_file_management`)
- **Fila (Queue)**: Implementação de uma estrutura FIFO para armazenar os arquivos processados.
- **Importação de Arquivos**: Leitura de arquivos `.txt` validados, ignorando extensões inválidas.
- **Processamento**: Extração de metadados dos arquivos (nome, quantidade de linhas, conteúdo).
- **Remoção**: Capacidade de remover o primeiro arquivo da fila.
- **Metadados**: Exibição de informações sobre um arquivo processado através da sua posição na fila.

### Buscas (`ting_word_searches`)
- **Verificar Existência de Palavras (`exists_word`)**: Busca _case insensitive_ que verifica a existência de uma palavra nos arquivos e lista as linhas em que ocorrem.
- **Busca por Palavra (`search_by_word`)**: Busca detalhada que, além da linha, retorna o trecho do conteúdo exato onde a palavra foi encontrada.

## Tecnologias Utilizadas

- **Linguagem**: Python 3
- **Testes**: Pytest
- **Linter de Código**: Flake8
- **Estruturas de Dados**: Pilhas, Deques, Nó, Listas Ligadas e Listas Duplamente Ligadas.

## Estrutura do Projeto

```text
.
├── statics
│   ├── arquivo_teste.txt
│   ├── novo_paradigma_globalizado.txt
│   └── novo_paradigma_globalizado-min.txt
├── tests/
├── ting_file_management/
│   ├── file_management.py
│   ├── file_process.py
│   └── queue.py
├── ting_word_searches/
│   └── word_search.py
├── dev-requirements.txt
├── requirements.txt
├── setup.cfg
└── README.md
```

## Como Executar

### Pré-requisitos
- Python 3 instalado em sua máquina.

### Instalação

1. Clone o repositório:
```bash
git clone git@github.com:devfelipesantiago/project-ting.git
cd project-ting
```

2. Crie e ative o ambiente virtual:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Instale as dependências de desenvolvimento e de execução:
```bash
python3 -m pip install -r dev-requirements.txt
```

### Executando os Testes

Para executar a suíte de testes com `pytest`:
```bash
python3 -m pytest
```

Para verificar se o código segue o guia de estilo do Python (`flake8`):
```bash
python3 -m flake8
```
