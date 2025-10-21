# 🏛️ SISTEMA BANCARIO

## Estrutura:
- classes.py
    - class Banco
    - class Cliente
    - class Conta (ABC)
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
    - A **classe Banco** foi criada

- **class Cliente**
    - A **classe Cliente** foi criada

- **class Conta**
    - A **classe Conta** foi criada

- **class ContaCorrente(Conta)**
    - A **classe ContaCorrente** foi criada

- **class ContaPoupanca(Conta)**
    - A **classe ContaPoupanca** foi criada



