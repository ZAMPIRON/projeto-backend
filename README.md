# 🏛️ SISTEMA BANCARIO

## Estrutura:
- classes.py
    - class Banco
    - class Cliente
    - class OperacoesFinanceiras (ABC)
    - class Conta (OperacoesFinanceiras)
    - class ContaCorrente(Conta)
    - class ContaPoupanca(Conta)
    
- funcoes.py
    - def gerente_cliente()
    - def gerente_senha()
    - def menu_gerente()
    - def gerenciar_clientes()
    - def gerenciar_contas()
    - def login_ou_cadastro_cliente()
    - def login_cliente()
    - def cadastro_cliente()
    - def menu_cliente()
    - def criar_conta()
    - def listar_clientes()
    - def listar_clientes_por()
    - def excluir_cliente()
    - def listar_contas()
    - def listar_contas_por_cliente()
    - def verificar_conta()
    - def deposito()
    - def saque()
    - def transferencia()
    - def consulta_saldo_extrato()
 
- app.py
```python
  - from time import sleep
    import os
    from funcoes import gerente_cliente
    from classes import *
    print("===SEJA BEM VINDO!===")
    gerente_cliente()
```

---
## Explicação classes
- **class Banco**
    - A **classe Banco** foi criadapara gerenciar clientes e contas do sistema. Ela mantém listas de clientes e contas, permitindo cadastrar, localizar e controlar operações bancárias. Representa uma agregação, pois os clientes podem existir fora do banco.

- **class Cliente**
    - A **classe Cliente** foi criada para armazenar informações pessoais do cliente, como nome, CPF e contatos. Cada cliente pode possuir uma ou mais contas, estabelecendo uma associação com a classe Conta. Facilita o gerenciamento das contas vinculadas ao cliente.

- **class OperacoesFinanceiras**
    - A **classe OperacoesFinanceiras** foi criada como uma interface (ou contrato) para definir métodos obrigatórios relacionados a operações financeiras, como depositar(), sacar() e transferir(). Isso garante padronização entre diferentes tipos de conta.

- **class Conta**
    - A **classe Conta** foi criada como classe base abstrata, representando o comportamento comum de todas as contas. Contém atributos como número da conta, saldo e cliente associado, além de métodos genéricos como depósito, saque e transferência. Não pode ser instanciada diretamente, promovendo abstração e reutilização de código.

- **class ContaCorrente(Conta)**
    - A **classe ContaCorrente** herda de Conta e representa contas correntes. Permite saques sem saldo mínimo, reimplementando o método sacar() da classe base. Demonstra o uso de herança e polimorfismo, pois aproveita métodos comuns, mas ajusta comportamentos específicos.

- **class ContaPoupanca(Conta)**
    - A **classe ContaPoupanca** herda de Conta e representa contas poupança. Possui regra de saldo mínimo (R$ 100,00) para saques, reimplementando o método sacar() com comportamento diferente da conta corrente. Demonstra polimorfismo e garante maior controle financeiro.

---
## Explicação classes
- **def gerente_cliente()**  
  Exibe o menu inicial do sistema, permitindo escolher entre acesso de gerente ou cliente.

- **def gerente_senha()**  
  Solicita a senha do gerente e permite acesso ao menu do gerente caso a senha esteja correta.

- **def menu_gerente()**  
  Exibe as opções de gerenciamento do gerente: gerenciar clientes ou contas.

- **def gerenciar_clientes()**  
  Permite listar todos os clientes cadastrados ou excluir um cliente específico.

- **def gerenciar_contas()**  
  Permite listar todas as contas ou verificar detalhes de uma conta específica.

- **def login_ou_cadastro_cliente()**  
  Menu que permite ao usuário escolher entre fazer login ou se cadastrar como cliente.

- **def login_cliente()**  
  Realiza o login do cliente verificando nome e CPF, redirecionando para o menu do cliente em caso de sucesso.

- **def cadastro_cliente()**  
  Solicita dados do cliente, cria um objeto `Cliente`, cadastra-o no sistema e chama a função para criar a conta.

- **def menu_cliente()**  
  Exibe o menu do cliente, permitindo realizar depósito, saque, transferência, consultar extrato ou voltar ao menu principal.

- **def criar_conta()**  
  Cria uma conta (corrente ou poupança) para o cliente, vinculando-a ao mesmo e adicionando à lista de contas do banco.

- **def listar_clientes()**  
  Lista todos os clientes cadastrados, mostrando ID, nome, CPF e gênero.

- **def listar_clientes_por()**  
  Função complementar para listar clientes filtrando por algum critério (não implementada completamente no código fornecido).

- **def excluir_cliente()**  
  Remove um cliente da lista de clientes pelo nome, caso exista.

- **def listar_contas()**  
  Lista todas as contas cadastradas, mostrando ID, nome do cliente e saldo atual.

- **def listar_contas_por_cliente()**  
  Lista todas as contas de um cliente específico (não implementada completamente no código fornecido).

- **def verificar_conta()**  
  Exibe detalhes de uma conta específica, incluindo status de ativação e saldo.

- **def deposito()**  
  Realiza um depósito na conta vinculada ao cliente, atualizando o saldo.

- **def saque()**  
  Realiza um saque na conta do cliente, obedecendo às regras da conta (como saldo mínimo para poupança).

- **def transferencia()**  
  Realiza transferência entre contas de clientes diferentes, atualizando os saldos das duas contas envolvidas.

- **def consulta_saldo_extrato() / consulta_extrato()**  
  Exibe todas as operações registradas no extrato da conta e o saldo atual do cliente.

- **def getContaCliente()**  
  Função auxiliar que retorna a conta associada a um cliente, utilizada nas operações financeiras como depósito, saque e transferência.

---
