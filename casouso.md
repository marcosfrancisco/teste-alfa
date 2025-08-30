# Caso de Uso: Cadastrar Produto

**ID:** UC01  
**Nome:** Cadastrar Produto  
**Ator Principal:** Funcionário  
**Atores Secundários:** Sistema de Estoque, Empresa  

---

## Descrição
Este caso de uso descreve como um funcionário cadastra um novo produto no sistema, incluindo informações obrigatórias (nome, código, preço, quantidade) e opcionais (descrição, categoria, fornecedor).

---

## Pré-condições
- O funcionário deve estar autenticado no sistema.  
- O funcionário deve ter permissão de cadastro de produtos.  

---

## Pós-condições
- O produto será registrado no banco de dados.  
- O produto ficará disponível para operações de consulta, venda e atualização.  

---

## Fluxo Principal (Cenário de Sucesso)
1. O caso de uso inicia quando o funcionário solicita a opção **Cadastrar Produto** no sistema.  
2. O sistema exibe o formulário de cadastro de produto.  
3. O funcionário informa os seguintes dados obrigatórios:  
   - Nome do Produto  
   - Código/SKU  
   - Preço  
   - Quantidade em Estoque  
4. O funcionário pode informar dados adicionais:  
   - Descrição  
   - Categoria  
   - Fornecedor  
   - Data de Validade (quando aplicável)  
5. O funcionário confirma a operação clicando em **Salvar**.  
6. O sistema valida os dados:  
   - Código único (não duplicado)  
   - Preço ≥ 0  
   - Quantidade ≥ 0  
7. O sistema grava o novo produto no banco de dados.  
8. O sistema exibe a mensagem **“Produto cadastrado com sucesso”**.  
9. O caso de uso é encerrado com sucesso.  

---

## Fluxos Alternativos
**A1 – Dados inválidos**  
- Se algum campo obrigatório não for preenchido ou estiver inválido (ex.: preço negativo), o sistema exibe mensagem de erro.  
- O funcionário corrige os dados e volta ao passo 5.  

**A2 – Código duplicado**  
- Se já existir um produto com o mesmo código/SKU, o sistema rejeita o cadastro e informa o erro.  
- O funcionário deve informar um código diferente.  

---

## Regras de Negócio
- Cada produto deve ter um **código único (SKU)**.  
- O preço deve ser um número não negativo.  
- A quantidade inicial deve ser maior ou igual a zero.  

---

## Exceções
- Se houver falha de conexão com o banco de dados, o sistema informa o erro e o cadastro não é concluído.  
- Caso o funcionário não tenha permissão, o sistema bloqueia a operação.  

---

## Extensões
- Integração com módulo de fornecedores (para preencher dados automaticamente).  
- Integração com módulo de estoque mínimo (avisar quando quantidade for baixa).  
