1. Código para Cálculo da Soma

# Cálculo da Soma

INDICE = 13
SOMA = 0
K = 0

while K < INDICE:
    K += 1
    SOMA += K

print(f"O valor da variável SOMA é {SOMA}.")

2. Verificação de Número na Sequência de Fibonacci

# Verificação se o número pertence à sequência de Fibonacci

def pertence_fibonacci(n):
    a, b = 0, 1
    while a <= n:
        if a == n:
            return True
        a, b = b, a + b
    return False

def main():
    numero = int(input("Digite um número: "))
    if pertence_fibonacci(numero):
        print(f"O número {numero} pertence à sequência de Fibonacci.")
    else:
        print(f"O número {numero} NÃO pertence à sequência de Fibonacci.")

if __name__ == "__main__":
    main()

    3. Análise do Faturamento Diário

import json

# Dados de faturamento mensal
dados_json = '''
{
    "faturamento_diario": {
        "1": 100.0,
        "2": 200.0,
        "3": 0.0,
        "4": 150.0,
        "5": 300.0,
        "6": 0.0,
        "7": 250.0,
        "8": 400.0,
        "9": 0.0,
        "10": 500.0,
        "11": 0.0,
        "12": 600.0,
        "13": 0.0,
        "14": 700.0,
        "15": 0.0
    }
}
'''

# Carregar dados
dados = json.loads(dados_json)
faturamento_diario = dados["faturamento_diario"]

# Calcular menor, maior e média
valores = [valor for valor in faturamento_diario.values() if valor > 0]
menor = min(valores)
maior = max(valores)
media = sum(valores) / len(valores)

# Calcular dias acima da média
dias_acima_media = sum(1 for valor in valores if valor > media)

print(f"Menor valor de faturamento: R${menor:.2f}")
print(f"Maior valor de faturamento: R${maior:.2f}")
print(f"Número de dias acima da média mensal: {dias_acima_media}")

4. Cálculo do Percentual de Representação dos Estados

# Cálculo do percentual de representação por estado

faturamento = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

total_faturamento = sum(faturamento.values())

percentuais = {estado: (valor / total_faturamento) * 100 for estado, valor in faturamento.items()}

for estado, percentual in percentuais.items():
    print(f"{estado}: {percentual:.2f}%")

5. Inversão de Caracteres de uma String

# Inversão de caracteres de uma string

def inverter_string(s):
    invertida = ""
    for char in s:
        invertida = char + invertida
    return invertida

def main():
    string = input("Digite uma string: ")
    string_invertida = inverter_string(string)
    print(f"A string invertida é: {string_invertida}")

if __name__ == "__main__":
    main()
