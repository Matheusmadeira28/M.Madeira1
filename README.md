import numpy as np

# Definição da função F(x) = 2x + 2
def F(x):
    return 2 * x + 2

# Definição dos limites de integração e do número de amostras
n1 = 0
n2 = 1
rn = 1000000

# Geração de números aleatórios uniformemente distribuídos no intervalo [0, 1]
x_random = np.random.uniform(n1, n2, rn)

# Avaliação da função F(x) para os valores aleatórios gerados
F_random = F(x_random)

# Cálculo da média dos valores da função
F_mean = np.mean(F_random)

# Estimativa da integral usando o método de Monte Carlo
integral = (n2 - n1) * F_mean

# Impressão dos resultados
print("Calculo de uma Integral 'irresolvivel' usando Monte Carlo")
print("\nIntegral: I = ∫(2x + 2) dx de 0 a 1")
print("Quantidade de valores aleatorios (rn):", rn)
print("Intervalo de integracao: [", n1, ",", n2, "]")
print("\nValor aproximado da integral: {:.5f}".format(integral))
