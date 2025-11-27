Calculadora de Partidas Rankeadas — Python

Este projeto foi desenvolvido como parte do desafio da DIO, utilizando conceitos fundamentais de programação: variáveis, operadores, funções, condicionais e loops.

A aplicação calcula o saldo de vitórias de um jogador e determina seu nível ranqueado conforme a tabela proposta no desafio.

Objetivo

Criar uma função que recebe a quantidade de vitórias e derrotas, calcula o saldo e classifica o jogador em um nível:

Vitórias	Nível
< 10	Ferro
11–20	Bronze
21–50	Prata
51–80	Ouro
81–90	Diamante
91–100	Lendário
≥ 101	Imortal
Como executar o projeto

Certifique-se de ter o Python 3 instalado.

No terminal, navegue até a pasta do projeto:

cd nome-do-projeto


Execute o arquivo principal:

python src/classificador.py

Código utilizado
def calcular_nivel(vitorias, derrotas):
    saldo = vitorias - derrotas
    
    if vitorias < 10:
        nivel = "Ferro"
    elif 11 <= vitorias <= 20:
        nivel = "Bronze"
    elif 21 <= vitorias <= 50:
        nivel = "Prata"
    elif 51 <= vitorias <= 80:
        nivel = "Ouro"
    elif 81 <= vitorias <= 90:
        nivel = "Diamante"
    elif 91 <= vitorias <= 100:
        nivel = "Lendário"
    else:
        nivel = "Imortal"
    
    return saldo, nivel


vitorias = int(input("Digite o número de vitórias: "))
derrotas = int(input("Digite o número de derrotas: "))

saldo, nivel = calcular_nivel(vitorias, derrotas)

print(f"O Herói tem de saldo de {saldo} está no nível de {nivel}.")


Ao final da execução, aparece uma mensagem como:

O Herói tem de saldo de 15 está no nível de Prata.
