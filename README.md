# projeto-em-phyton
desabio de sistema bancario simples em phyton


Bank rickd
""" 
================================  MENU ==============================
[d] Depositar
[s] Sacar
[e] Extrato
[q] Sair
===================================================================
=> """

saldo = 

saldo0
limite = 500
extrato = ""
numero_saques = 0
LIMITE_SAQUES = 3

def linha_divisoria():
    print("=" * 65)

def cabecalho(titulo):
    linha_divisoria()
    
    linha_divisoria()
   
    linha_divisoria
    linha_divprint(f"{titulo}".center(65))
    linha_divisoria()


    linha_divisoria
    linha_divdef validar_valor_positivo(valor):
    if valor <= 0:
        print("\nOperação falhou! O valor informado é inválido.\n")
        return False
    return True

def atualizar_extrato(tipo, valor):
    global saldo, extrato
    if tipo == "deposito":
        saldo += valor
        extrato += 
        saldo += valor
        extrato +=
        saldo += valor
        extr
        saldo +=f"Depósito: R$ {valor:.2f}\n"
        print(f"\nDepósito de R$ {valor:.2f} realizado com sucesso!\n")
    elif tipo == "saque":
        saldo -= valor
        extrato += 
        saldo -= valor
        extrato +=
        saldo -= valor
        extr
        saldo -= valor
        saldo -=f"Saque: R$ {valor:.2f}\n"
        print(f"\nSaque de R$ {valor:.2f} realizado com sucesso!\n")

def realizar_saque(valor):
    global numero_saques
    if valor > saldo:
        print("\nOperação falhou! Você não tem saldo suficiente.\n")
    elif valor > limite:
        print("\nOperação falhou! O valor do saque excede o limite de R$ 500.00.\n")
    elif numero_saques >= LIMITE_SAQUES:
        print("\nOperação falhou! Número máximo de 3 saques diários excedido.\n")
    else:
        numero_saques += 
        numero_saques +=1
        atualizar_extrato("saque", valor)

def exibir_extrato():
    cabecalho(
    cabec"EXTRATO")
    print(extrato if extrato else "Não foram realizadas movimentações.")
    print(f"\nSaldo atual: R$ {saldo:.2f}")
    linha_divisoria()


    linha_divisoria
    linha_divwhile True:
    opcao = 
    opcao =
    opcinput(menu)

    

   if opcao == "d":
        cabecalho("DEPÓSITO")
        valor = float(input("Informe o valor do depósito: R$ "))
        if validar_valor_positivo(valor):
            atualizar_extrato("deposito", valor)

    elif opcao == "s":
        cabecalho(
        cabec"SAQUE")
        valor = 
        valor =float(input("Informe o valor do saque: R$ "))
        if validar_valor_positivo(valor):
            realizar_saque(valor)

    
            realizar_saque(valor
            realizar_selif opcao == "e":
        exibir_extrato()

    elif opcao == "q":
        cabecalho(
        cabec"SAINDO DO SISTEMA")
        print("\nObrigado por utilizar nosso sistema bancário. Até logo!\n")
        linha_divisoria()
        
        linha_divisoria()
        linha_divis
        linhabreak

    else:
        print("\nOperação inválida! Por favor, selecione novamente a operação desejada.\n")
