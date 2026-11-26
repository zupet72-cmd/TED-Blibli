# ⋆☕︎ ˖Sistema de Biblioteca (TED)

Aplicação de console em **C#** para gerenciar livros em estoque, devoluções e integrantes de uma biblioteca, aplicando algoritmos de **busca**, **ordenação** e **seleção** sobre estruturas de dados lineares.

## INTEGRANTES DO PROJETO 

| [EDUARDO BRAZ] 
| [JHEMILLY ALVES] 
| [PEDRO ZUZARTE] 
| [PEDRO NICHOLAS] 
| [THIAGO ESTEVES] 

**Disciplina:** Algoritmos e Estrutura de Dados II
**Professora:** [ROSANGELA SILVA]
**Instituição:** [UNISAPIENS]

## 📖 Sobre o Projeto

Trabalho avaliativo cujo objetivo é aplicar, na prática, algoritmos clássicos sobre uma estrutura de dados linear. O sistema simula uma biblioteca em que é possível cadastrar livros, registrar devoluções e gerenciar integrantes, localizando, ordenando e selecionando registros por diferentes critérios.

## Funcionalidades presentes projeto⬩➤

###  Livros no estoque⫶☰
- Cadastrar, remover e listar livros (código/ISBN, título, autor e quantidade)
- Buscar livro por código (busca linear ou binária)
- Ordenar livros por título (Bubble Sort ou Insertion Sort)
- Selecionar o livro com **maior** e com **menor** estoque

### Opção de  Devoluções
- Registrar devolução (livro, integrante e data prevista)
- Remover, listar e buscar devoluções
- Ordenar devoluções por prazo (Bubble Sort ou Insertion Sort)
- Selecionar a devolução com o prazo mais próximo

### Integrantes parceiros da biblioteca
- Cadastrar, remover, listar e buscar integrantes (matrícula e nome)
- Ordenar integrantes por nome (Bubble Sort ou Insertion Sort)

### Validações⭒ ⚠
- O código do livro aceita apenas números (hífens opcionais) e a matrícula apenas números
- Não permite cadastrar código ou matrícula duplicados
- Só registra devolução de livro e integrante já cadastrados
- Não permite remover um integrante que tenha devoluções vinculadas
- Campos vazios, datas e quantidades inválidas são recusados

## A Estrutura de dados e os algoritmos

**Estrutura de dados linear:** `List<T>` (lista), usada para livros, devoluções e integrantes.

| Tipo | Algoritmo | Onde é usado |
|---|---|---|
| Busca | Busca Linear | Livros por código |
| Busca | Busca Binária | Livros por código (a lista é ordenada por código antes) |
| Ordenação | Bubble Sort | Livros, devoluções e integrantes |
| Ordenação | Insertion Sort | Livros, devoluções e integrantes |
| Seleção | Maior / menor valor (varredura linear) | Maior e menor estoque; devolução de prazo mais próximo |

> Os algoritmos de ordenação são (`List<T>` com `Comparison<T>`), então a mesma implementação serve para as três listas.

## 𖣠 Tecnologias 𖣠

- **Linguagem:** C#
- **Plataforma:** .NET 8 (aplicação de console)
- **Estrutura:** `List<T>` da biblioteca padrão (`System.Collections.Generic`)
- **Versionamento:** Git e GitHub

## 𖣠 Estrutura do projeto 𖣠

```
BibliotecaTED/
├── Program.cs       # Menus e a interação com o usuário
├── Livro.cs         # Classe Livro
├── Devolucao.cs     # Classe Devolucao
├── Integrante.cs    # Classe Integrante
├── Algoritmos.cs    # Bubble Sort, Insertion Sort, busca linear e binária
├── docs/            # A Documentação em PDF
├── screenshots/     # Prints da execução
└── README.md
```

## ▶ Como executar o projeto? 

### Pré-requisitos
- [.NET SDK 8.0](https://dotnet.microsoft.com/download) ou superior
- Git

### Passo a passo

```bash
# 1. Clone o repositório
git clone https://github.com/[seu-usuario]/[nome-do-repositorio].git

# 2. Acesse a pasta do projeto
cd [nome-do-repositorio]

# 3. Execute
dotnet run
```

### Exemplo de uso
1. No menu principal, escolha **3. Integrantes** e cadastre um integrante.
2. Volte e escolha **1. Livros em estoque** e cadastre um livro.
3. Escolha **2. Devoluções** e registre uma devolução usando o código do livro e a matrícula.
4. Teste as buscas, ordenações e seleções em cada menu.

## Evidências de execução do código

**Menu principal**
![Menu principal](screenshots/cadastro-livro.png)

**Busca binária de livro**
![Busca binária](screenshots/busca-binaria.png)

**Validação de entrada (código inválido)**
![Validação](screenshots/cadastro-livro.png)

## Documentação

A descrição completa do projeto (introdução, objetivo, desenvolvimento e conclusão) está inclusa na pasta [`docs/`](docs/).

##  ⚠  Observações

- Os dados ficam **apenas em memória**: ao fechar o programa, tudo é perdido.
- A busca binária reordena a lista de livros por código antes de pesquisar, pois exige dados ordenados.
- A devolução registrada **não altera** a quantidade em estoque do livro.
