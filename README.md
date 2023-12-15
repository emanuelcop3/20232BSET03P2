# 20232BSET03P2
Inteli - Engenharia de Software | Avaliação 2023-2B P2


# Cats and Dogs Vote App 😸 🐶

Abaixo estão as vulnerabilidades identificadas e as medidas adotadas para corrigi-las:

## Vulnerabilidades Identificadas e Medidas Corretivas

1. **SQL Injection em Rotas de Inserção (`/cats` e `/dogs`):**
   - **Descrição:** O código original utilizava interpolação de strings para inserção no banco de dados, o que tornava suscetível a ataques de SQL Injection.
   - **Medida Corretiva:** As consultas SQL foram alteradas para utilizar prepared statements, garantindo assim a sanitização e validação dos dados de entrada.

2. **Lógica de Votação sem Verificação de Existência do Registro:**
   - **Descrição:** A lógica de votação não verificava se o registro do animal existia antes de adicionar um voto, o que poderia levar a operações inválidas.
   - **Medida Corretiva:** Foi adicionada uma consulta prévia para verificar a existência do registro antes de adicionar um voto, evitando assim operações em registros inexistentes.

3. **Tratamento de Erros Não Adequado:**
   - **Descrição:** O tratamento de erros nas rotas estava incompleto e poderia expor detalhes de implementação no caso de falhas.
   - **Medida Corretiva:** Foram implementados tratamentos de erro mais adequados, registrando mensagens genéricas no log e fornecendo respostas de erro ao cliente sem expor detalhes sensíveis.

4. **Métodos Não Implementados:**
   - **Descrição:** Algumas rotas e métodos declarados não estavam completamente implementados.
   - **Medida Corretiva:** Foram implementados todos os métodos que possuíam assinatura no código, garantindo o funcionamento correto de todas as funcionalidades.


