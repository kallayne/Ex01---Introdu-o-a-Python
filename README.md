# Ex01---Introdu-o-a-Python


def converter(unidade_entrada, valor, unidade_saida):

    if unidade_entrada == "pe" or unidade_entrada == "pes":
        metros = valor * 0.3048

    elif unidade_entrada == "jarda" or unidade_entrada == "jardas":
        metros = valor * 0.9144

    elif unidade_entrada == "metro" or unidade_entrada == "metros":
        metros = valor

    else:
        return "Unidade de entrada invalida"

    if unidade_saida == "metro" or unidade_saida == "metros":
        resultado = metros

    elif unidade_saida == "pe" or unidade_saida == "pes":
        resultado = metros * 3.281

    elif unidade_saida == "jarda" or unidade_saida == "jardas":
        resultado = metros / 0.9144

    else:
        return "Unidade de saida invalida"

    return resultado


unidade_entrada = input()
valor = float(input())
unidade_saida = input()

resultado = converter(unidade_entrada, valor, unidade_saida)

print(resultado)