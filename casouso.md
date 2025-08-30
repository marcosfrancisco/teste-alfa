# Caso de Uso — Cadastrar Produto (Flowchart)

```mermaid
flowchart LR
  %% Atores
  F[Funcionario\n<<ator>>]
  E[Empresa\n<<interessada>>]

  %% Sistema como contêiner
  subgraph S[Sistema]
    UC([Cadastrar Produto])
  end

  %% Relações
  F --> UC
  E --- UC
