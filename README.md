# Sistema Bancário em Python

Este projeto é um **sistema bancário simples** implementado em Python. Ele simula operações básicas como **depósitos**, **saques**, consulta de **extrato**, além de permitir a criação de **usuários** e **contas bancárias**.

## Funcionalidades

1. **Menu Interativo**
    - O sistema apresenta um menu com opções para o usuário escolher as operações desejadas:
      - `[d] Depositar`
      - `[s] Sacar`
      - `[e] Exibir Extrato`
      - `[nc] Nova Conta`
      - `[lc] Listar Contas`
      - `[nu] Novo Usuário`
      - `[q] Sair`

2. **Operações Bancárias**
    - **Depósito**: Permite ao usuário depositar valores na conta, atualizando o saldo e registrando a transação no extrato.
    - **Saque**: O usuário pode realizar saques, desde que respeitem o saldo disponível, o limite máximo por saque e o número diário de saques permitidos.
    - **Extrato**: Mostra todas as transações realizadas, incluindo depósitos e saques, e exibe o saldo final.

3. **Gerenciamento de Usuários**
    - **Criar Usuário**: O usuário pode cadastrar um novo perfil no sistema fornecendo nome, CPF, data de nascimento e endereço.
    - **Verificar Usuário**: Antes de criar uma nova conta, o sistema verifica se o CPF informado já está registrado.

4. **Gerenciamento de Contas**
    - **Criar Conta**: O sistema cria uma nova conta bancária vinculada a um CPF já cadastrado.
    - **Listar Contas**: Exibe uma lista de todas as contas criadas, incluindo detalhes como agência, número da conta e o nome do titular.

## Estrutura Geral

- O sistema mantém controle de:
  - Saldo da conta
  - Extrato de transações (depósitos e saques)
  - Limite de saque por transação e número máximo de saques por dia
  - Cadastro de usuários e contas bancárias

## Principais Funções

- **menu()**: Exibe o menu de opções.
- **depositar(saldo, valor, extrato)**: Adiciona um valor ao saldo e registra a operação no extrato.
- **sacar(saldo, valor, extrato, limite, numero_saques, limite_saques)**: Realiza o saque, respeitando limites de saldo, valor máximo e número de saques diários.
- **exibir_extrato(saldo, extrato)**: Exibe o extrato e o saldo atual.
- **criar_usuario(usuarios)**: Cadastra um novo usuário no sistema.
- **criar_conta(agencia, numero_conta, usuarios)**: Cria uma nova conta bancária associada a um usuário.
- **listar_contas(contas)**: Lista todas as contas registradas no sistema.

## Execução

O sistema roda em um loop contínuo, aguardando a seleção de operações pelo usuário até que ele escolha a opção de sair (`[q]`).

### Observações:
- O sistema utiliza estruturas como **listas** para armazenar usuários e contas, e mantém o controle das transações financeiras através de variáveis como `saldo`, `extrato` e `numero_saques`.
- Utiliza a função `input()` para a interação com o usuário, permitindo operações dinâmicas e personalizadas.

