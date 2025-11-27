# Calculadora de Partidas Rankeadas — Python

Projeto desenvolvido para o desafio da **DIO**, aplicando lógica de programação com variáveis, funções, condicionais e cálculo de classificação de jogadores.

---

## Sobre o projeto

O programa solicita ao usuário o número de **vitórias** e **derrotas**, calcula o **saldo de partidas** e determina o **nível ranqueado** conforme as regras do desafio.

A classificação segue a seguinte lógica:

| Vitórias | Nível |
|---------|--------|
| < 10 | Ferro |
| 11–20 | Bronze |
| 21–50 | Prata |
| 51–80 | Ouro |
| 81–90 | Diamante |
| 91–100 | Lendário |
| ≥ 101 | Imortal |

---

## Tecnologias utilizadas

- Python 3
- Lógica de programação
- Funções
- Estruturas condicionais

---

## Como executar o projeto

1. Certifique-se de ter o **Python 3** instalado.
2. Abra o terminal e navegue até a pasta do projeto:
   ```bash
   cd nome-do-repositorio
   ```
3. Execute o arquivo principal:
   ```bash
   python src/classificador.py
   ```

---

## Código utilizado

```python
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
```

## Exemplo de saída

> O Herói tem de saldo de **15** está no nível de **Prata**.
