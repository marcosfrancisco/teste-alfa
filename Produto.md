```mermaid
classDiagram
    class Produto {
        - id : int
        - valorUnitario : double
        - unidadeMedida : enumString
        - nome : String
        - categoria : enumString

        + editarValor(novoValor: double) : String
        + getInformacoes() : dict
    }
