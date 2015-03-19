import random

pedra = 10
papel = 11
tesoura = 12
spock = 13
lagarto = 14
lista = ["pedra","papel","tesoura","spock","lagarto"]
cganhou = 0
jganhou = 0

while cganhou < 3 and jganhou < 3:
    jc = random.randint(10,14)
    jp = int(input("faça sua jogada\n pedra = 10\n papel = 11\n tesoura = 12\n spock = 13\n lagarto = 14\n\n"))
    print(jc)
    if jc == 10 and (jp == 12 or jp == 14):
        print("computador ganhou")
        cganhou += 1
        jganhou = 0
    if jc == 10 and (jp == 13 or jp == 11):
        print("jogador ganhou")
        jganhou += 1
        cganhou = 0
    if jc == 11 and (jp == 13 or jp == 14):
        print ("jogador ganhou")
        jganhou += 1
        cganhou = 0
    if jc == 11 and (jp == 10 or jp == 12):
        print ("computador ganhou")
        cganhou += 1
        jganhou = 0
    if jc == 12 and (jp ==11 or jp == 14):
        print ("computador ganhou")
        cganhou += 1
        jganhou = 0
    if jc == 12 and (jp == 10 or jp == 13):
        print ("jogador ganhou")
        jganhou += 1
        cganhou = 0
    if jc == 13 and (jp == 12 or jp== 10):
        print ("computador ganhou")
        cganhou += 1
        jganhou = 0
    if jc == 13 and (jp == 14 or jp == 11):
        print ("jogador ganhou")
        jganhou += 1
        cganhou = 0
    if jc == 14 and (jp == 13 or jp== 11):
        print("computador ganhou")
        cganhou += 1
        jganhou = 0
    if jc == 14 and (jp == 12 or jp == 10):
        print ("jogador ganhou")
        jganhou += 1
        cganhou = 0
    if jp == jc:
        print ("empate")
        jganhou = 0
        cganhou = 0

if jganhou == 3:
        print ("voce ganhou")
if cganhou == 3:
        print ("vc perdeu ")
