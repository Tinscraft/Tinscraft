programa {
  funcao inicio() {


def calcular_media_idade(idades):
    if not idades:
        return 0  
    else:
        return sum(idades) / len(idades)


idades = []

while True:
    idade_str = input("Digite a idade do aluno (ou 'fim' para encerrar): ")

    if idade_str.lower() == 'fim':
        break

    try:
        idade = int(idade_str)
        idades.append(idade)
    except ValueError:
        print("Por favor, digite uma idade válida.")


media_idade = calcular_media_idade(idades)

if media_idade == 0:
    print("Não há alunos na turma.")
else:
    print(f"A média da idade dos alunos é: {media_idade}")

  }
}
