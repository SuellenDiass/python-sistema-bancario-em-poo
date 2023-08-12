<p> <h1 align="center">Modelando o Sistema Bancário em POO com Python</h1></p>


<p align="center">
    <img width="700" src="https://github.com/SuellenDiass/SuellenDiass/assets/102911341/b45c694e-06af-4de5-a804-b7d68981f5a9">
    <p> <spam align="center">Modelo de classes na UML</spam></p>
</p>



O código a seguir é uma implementação de um sistema bancário simples em Python, que permite criar clientes, contas bancárias, realizar operações como depósitos, saques e exibir extratos, além de outras funcionalidades relacionadas a clientes e contas. A seguir segue a  explicação da estrutura e os principais componentes do código:

1. **Importações de Módulos:**
   - `import textwrap`: Importa o módulo `textwrap`, que é usado para formatar o texto no menu.
   - `from abc import ABC, abstractclassmethod, abstractproperty`: Importa as classes `ABC`, `abstractclassmethod` e `abstractproperty` do módulo `abc` (Abstract Base Classes). Essas são usadas para criar classes abstratas e definir métodos e propriedades abstratas.

2. **Definição das Classes:**
   - `Cliente`: Representa um cliente do banco, com um endereço e uma lista de contas associadas.
   - `PessoaFisica`: É uma subclasse de `Cliente` que adiciona informações específicas para clientes pessoa física, como nome, data de nascimento e CPF.
   - `Conta`: Representa uma conta bancária, com um saldo, número, cliente associado e histórico de transações.
   - `ContaCorrente`: É uma subclasse de `Conta` que implementa as funcionalidades específicas de uma conta corrente, como limite de saques e limite de saldo.
   - `Historico`: Mantém um registro das transações realizadas em uma conta.
   - `Transacao`: É uma classe abstrata que define os métodos necessários para realizar uma transação.
   - `Saque`: É uma subclasse de `Transacao` que representa uma transação de saque.
   - `Deposito`: É uma subclasse de `Transacao` que representa uma transação de depósito.

3. **Funções de Interatividade:**
   - `menu()`: Mostra um menu interativo para o usuário escolher entre diversas operações.
   - `filtrar_cliente(cpf, clientes)`: Filtra os clientes com base no CPF.
   - `recuperar_conta_cliente(cliente)`: Recupera a primeira conta associada a um cliente (pode ser melhorado para permitir escolha).
   - `depositar(clientes)`: Permite realizar uma operação de depósito.
   - `sacar(clientes)`: Permite realizar uma operação de saque.
   - `exibir_extrato(clientes)`: Mostra o extrato de transações e o saldo de uma conta.
   - `criar_cliente(clientes)`: Permite criar um novo cliente.
   - `criar_conta(numero_conta, clientes, contas)`: Cria uma nova conta corrente e associa-a a um cliente existente.
   - `listar_contas(contas)`: Exibe informações sobre todas as contas.

4. **Função Principal `main()`:**
   - Esta função contém um loop onde o usuário pode escolher diferentes operações do menu.
   - Ela cria listas vazias de clientes e contas.
   - As operações escolhidas pelo usuário são chamadas de acordo com as funções mencionadas acima.

5. **Execução:**
   - Ao chamar `main()`, o programa entra em um loop interativo, onde o usuário pode escolher várias operações bancárias.

#### Curso Formação Python Developer da Dio.me administrado pelo mentor Guilherme Carvalho/Python Consultant, Oak Solution

[DIO](https://www.dio.me/).

