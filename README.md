# GabrielGuimar-es_EP2
# -*- coding: utf-8 -*-
"""
Created on Thu Mar 26 00:53:29 2015

@author: GABRIEL
"""

import turtle
import random
import time


acertos = 0
o = open("entrada.txt", encoding="utf-8") # abre arquivo entrada.txt

p = o.readlines()  # le o arquivo e coloca em lista p 

lista = []
for ln in p:
    c = ln.strip()
    if c != "":
        lista.append(c) #limpando
        
tela = turtle.Screen() 
tela.bgcolor("orange")
tela.title("Jogo da Forca")
#tela.bgpic("1374.png")

tortugal = turtle.Turtle()
tortugal.pen(shown =False,fillcolor="blue",pencolor="black")
tortugal.penup()


tortuga = turtle.Turtle()
tortuga.speed(50)
tortuga.pen(shown =False,fillcolor="blue",pencolor="black")
tortuga.penup()
tortuga.setpos(-350,100)   
tortuga.color("red")

def desenharforca():
    tartarugaf = turtle.Turtle()
    tartarugaf.penup()
    tartarugaf.pen(shown =False,fillcolor="black",pencolor="black")
    tartarugaf.pensize(8)
    tartarugaf.setpos(-250 , -250)
    tartarugaf.pendown()
    tartarugaf.left(90)
    tartarugaf.forward(400)
    tartarugaf.right(90)
    tartarugaf.forward(100)
    tartarugaf.right(90)
    tartarugaf.forward(95)
    tartarugaf.penup()
    tartarugaf.pen(shown =False,fillcolor="red",pencolor="black")  
    
tortugam = turtle.Turtle()
tortugam.pen(shown =False,fillcolor="red",pencolor="red")


tartarugac = turtle.Turtle()
tartarugac.penup()
tartarugac.pen(shown =False,fillcolor="red",pencolor="red")

def forcaclear():
    tartarugac.clear()
    tortuga.clear()
    
def tortugalsetposwrite(X,Y):
    global acertos
    global acento
    global chutes
    
    if letras[w] == X and chutee == Y and Y not in acento:
        
        tortugal.setpos(w*35-x*16,-290)
                    
        tortugal.write(X, False, align="center",font=("Arial",25))
        
        acento.append(Y)
        chutes +=1                   
        acertos += 1
    
def underline(X):
    i = 0
    while i != X:
        
        
        
        tortuga.setpos(i*35-X*17.5,-300)
        
    
    
 
        if palavra[i] == " " :
            
            tortuga.write(" ", False, align="left",font=("Arial",30))
        else:
            tortuga.write("_ ", False, align="left",font=("Arial",30))
            
        i +=1 
    
 
chutes = 0
pal = 0
dnv = "sim"

while dnv == "sim" and len(lista) != 0:
    forcaclear()
    tortugal.clear()
    erros = 0
    acertos = 0
    
    acento = []
    
    
    

    n= len(lista) - 1
    pn = random.randint(0,n)
    palavra = lista[pn] #escolha palavra
    
    palavram = palavra.upper()
    
    pal +=1
    
    x= len(palavra)#qnts espaços
    
    espaco = []
    letras = []
    
    start = 0
    while start != -1:
        start = palavra.find(" ", start)
        espaco.append(start)
        if start!= -1:
            start += 1
            
  del espaco[-1]
    
    del lista[pn]
    
    t = 0
    
    while t != x: #x = len(palavra)
        letras.append(palavra[t].upper()) #letras
        t += 1
    
    
    
    i = 0
    while i != x: #x = len(palavra)
        
        
        tortuga.setpos(i*35-x*17.5,-300)
        if palavra[i] == " " :
            
            tortuga.write(" ", False, align="left",font=("Arial",30))
        else:
            tortuga.write("_ ", False, align="left",font=("Arial",30))
        i +=1
    
    
    
