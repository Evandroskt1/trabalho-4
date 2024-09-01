# trabalho-4

class Calculadora:
    def __init__(self, valorA, valorB, operacao):
        self.__valorA = valorA
        self.__valorB = valorB
        self.__operacao = operacao

    @property
    def valorA(self):
        return self.__valorA
    
    @valorA.setter
    def valorA(self, valor):
        self.__valorA = valor

    @property
    def valorB(self):
        return self.__valorB
    
    @valorB.setter
    def valorB(self, valor):
        self.__valorB = valor

    @property
    def operacao(self):
        return self.__operacao
    
    @operacao.setter
    def operacao(self, operacao):
        self.__operacao = operacao

    def validar_operacao(self, operacao):
        operacoes_validas = ['+', '-', '*', '/']
        return operacao in operacoes_validas

    def calcular(self):
        if not self.validar_operacao(self.operacao):
            print("Operação inválida!")
            exit()
        
        if self.operacao == '/':
            if self.valorB == 0:
                print("Divisão por zero!")
                exit()

        if self.operacao == '+':
            return self.valorA + self.valorB
        elif self.operacao == '-':
            return self.valorA - self.valorB
        elif self.operacao == '*':
            return self.valorA * self.valorB
        elif self.operacao == '/':
            return self.valorA / self.valorB

    def mostrar_resultado(self):
        print(f"{self.valorA} {self.operacao} {self.valorB} = {self.calcular()}")



main

from Calculadora import Calculadora

# Criando uma instância da classe
calculadora = Calculadora(10, 5, '/')

# Mostrando o resultado
calculadora.mostrar_resultado()



entrada de dados para teste

valorA = float(input("Digite o primeiro valor: "))
valorB = float(input("Digite o segundo valor: "))
operacao = input("Digite a operação (+, -, *, /): ")

calculadora = Calculadora(valorA, valorB, operacao)
calculadora.mostrar_resultado()
 
 
 [Documento3.docx](https://github.com/user-attachments/files/16829585/Documento3.docx)

