#!/usr/bin/python

import socket

target = "192.168.81.101"
port = 8888

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

s.connect((target, port))

s.recv(1024).decode()
lines = s.recv(1024).decode()
lines.split("/n")
numA = lines[48]
numB = lines[58]
numC = lines[67]

answer = ((int(numA) + int(numB)))*int(numC)
s.send(str(answer).encode())
print(s.recv(1024).decode())

s.close()

#This is not working 100%. It got the flag PYTHON{Fastest_C0d3r_in_the_W3st} 
#but the script does not work when there are double digit numbers used. Not sure how to get around that. 
