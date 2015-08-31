def quadrados_menores(n):
    return [i**2 for i in range (1, n+1) if i**2 <=n]
         

assert [1]==quadrados_menores(1)
assert [1,4]==quadrados_menores(4)
assert [1,4,9]==quadrados_menores(9)
assert [1,4,9]==quadrados_menores(11)


def soma_quadrados (n):
    if n>0:
        menores=quadrados_menores(n)
        ultimo=menores[-1]
        if ultimo==n:
           return [n]
        else:
           ultimo=menores.pop()
           lista_escolhida=[ultimo]
           lista_escolhida.extend((soma_quadrados(n-ultimo)))
           
           while menores:
               lista_escolhida_2=gerar_solucao(menores, n)
               if len (lista_escolhida_2)<len(lista_escolhida):
                   lista_escolhida=lista_escolhida_2
           return lista_escolhida
                   
                       
    return [0]

def gerar_solucao(menores,n):
    ultimo=menores.pop()
    lista_escolhida=[ultimo]
    lista_escolhida.extend(soma_quadrados(n-ultimo))
    return lista_escolhida


assert [0]== soma_quadrados(0)
assert [1]== soma_quadrados(1)
assert [4]== soma_quadrados(4)
assert [9]== soma_quadrados(9)
assert [1,1]== soma_quadrados(9)
assert [1,1,1]== soma_quadrados(3)
assert [4,1] == soma_quadrados(5)
assert [4,4,4] == soma_quadrados(12)
