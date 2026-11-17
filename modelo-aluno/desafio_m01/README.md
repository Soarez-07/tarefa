print("=== CALCULADORA PY ===")

contas = 0

while True:
    print("\n1-Somar 2-Subtrair 3-Multiplicar 4-Dividir 5-Potência 6-Resto 0-Sair")

    opcao = input("Opção: ")

    if opcao == "0":
        print(f"Contas feitas: {contas}. Até a próxima!")
        break

    elif opcao in ["1", "2", "3", "4", "5", "6"]:
        num1 = float(input("Primeiro número: "))
        num2 = float(input("Segundo número: "))

        if opcao == "1":
            resultado = num1 + num2
            print(f"{num1:.2f} + {num2:.2f} = {resultado:.2f}")

        elif opcao == "2":
            resultado = num1 - num2
            print(f"{num1:.2f} - {num2:.2f} = {resultado:.2f}")

        elif opcao == "3":
            resultado = num1 * num2
            print(f"{num1:.2f} * {num2:.2f} = {resultado:.2f}")

        elif opcao == "4":
            if num2 == 0:
                print("Não dá para dividir por zero!")
                continue
            resultado = num1 / num2
            print(f"{num1:.2f} / {num2:.2f} = {resultado:.2f}")

        elif opcao == "5":
            resultado = num1 ** num2
            print(f"{num1:.2f} ** {num2:.2f} = {resultado:.2f}")

        elif opcao == "6":
            if num2 == 0:
                print("Não dá para dividir por zero!")
                continue
            resultado = num1 % num2
            print(f"{num1:.2f} % {num2:.2f} = {resultado:.2f}")

        contas += 1

    else:
        print("Opção inválida. Escolha de 0 a 6.")
