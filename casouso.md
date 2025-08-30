# Caso de Uso - Cadastrar Produto

```mermaid
%% Diagrama de Caso de Uso - Cadastrar Produto
usecaseDiagram
  actor Funcionario as F
  actor Empresa as E

  rectangle Sistema {
    usecase "Cadastrar Produto" as UC1
  }

  F --> UC1
  E --> UC1
