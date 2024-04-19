# linguagempython
class Paciente:
    def __init__(self, nome, idade, genero, altura, peso):
        self.nome = nome
        self.idade = idade
        self.genero = genero
        self.altura = altura
        self.peso = peso

def coletar_dados_paciente():
    nome = input("Nome do paciente: ")
    idade = int(input("Idade do paciente: "))
    genero = input("Gênero do paciente: ")
    altura = float(input("Altura do paciente (em metros): "))
    peso = float(input("Peso do paciente (em kg): "))
    
    paciente = paciente(nome, idade, genero, altura, peso)
    return paciente

def prioridade_atendimento(paciente):
    if paciente.idade >= 18:
        return True
    else:
        return False

# Coletar dados do paciente
paciente1 = coletar_dados_paciente()

# Verificar prioridade de atendimento
if prioridade_atendimento(paciente1):
    print("O paciente", paciente1.nome, "deve ser atendido com prioridade.")
else:
    print("O paciente", paciente1.nome, "não tem prioridade de atendimento.")
