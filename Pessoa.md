```mermaid
classDiagram
    class Pessoa {
        - int id
        - String nome
        - String cpf
        - Date dataNasc
        - String endereco

        + Pessoa(int id, String nome, String cpf, Date dataNasc, String endereco)
        + int getId()
        + String getNome()
        + String getCpf()
        + Date getDataNasc()
        + String getEndereco()
        + int getIdade()
    }
