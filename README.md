# heranca2

class Animal:
    def __init__(self, numero_d_patas):
        self.numero_d_patas = numero_d_patas

    def __str__(self):
        return f"{self.__class__.__name__}: {', '.join([f'{chave}= {valor}' for chave, valor in self.__dict__.items()])}"


class Mamifero(Animal):
    def __init__(self, numero_d_patas, cor_pelo):
        self.cor_pelo = cor_pelo
        super().__init__(numero_d_patas)


class Ave(Animal):
    def __init__(self, numero_d_patas):
        super().__init__(numero_d_patas)


class Gato(Mamifero):
    pass


class Ornitorinco(Mamifero, Ave):
    pass


gato = Gato(4, "preto")
print(gato)

