def soma(x, y):
    return x + y

def subtracao(x, y):
    return x - y

def multiplicacao(x, y):
    return x * y

def divisao(x, y):
    if y != 0:
        return x / y
    else:
        return "Erro! Divisão por zero."

while True:
    print("\nOperações disponíveis:")
    print("1: Soma")
    print("2: Subtração")
    print("3: Multiplicação")
    print("4: Divisão")
    print("0: Sair")

    escolha = input("Digite o número para a operação desejada: ")

    if escolha == '0':
        print("Saindo da calculadora. Adeus!")
        break
    elif escolha in ('1', '2', '3', '4'):
        try:
            num1 = float(input("Digite o primeiro valor: "))
            num2 = float(input("Digite o segundo valor: "))
        except ValueError:
            print("Erro! Certifique-se de inserir valores numéricos.")
            continue

        if escolha == '1':
            resultado = soma(num1, num2)
            print(f"Resultado da soma: {resultado}")
        elif escolha == '2':
            resultado = subtracao(num1, num2)
            print(f"Resultado da subtração: {resultado}")
        elif escolha == '3':
            resultado = multiplicacao(num1, num2)
            print(f"Resultado da multiplicação: {resultado}")
        elif escolha == '4':
            resultado = divisao(num1, num2)
            print(f"Resultado da divisão: {resultado}")
    else:
        print("Essa opção não existe. Por favor, escolha uma opção válida.")
