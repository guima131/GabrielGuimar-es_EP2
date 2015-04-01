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
    
    
 
