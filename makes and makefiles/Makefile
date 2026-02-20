# Author: AJ Hopkins
# File Name: Makefile
# Last Date of Modification: February 20, 2026
# Purpose: A build makefile for an employee inheritance project

# Variables
CC = g++
TARGET = employee
# Compile with all errors and warnings
CFLAGS = -c -Wall -Wextra

# Targets
all: $(TARGET)

$(TARGET): main.o Employee.o Officer.o Supervisor.o
	$(CC) main.o Employee.o Officer.o Supervisor.o -o $(TARGET)

main.o: main.cpp Employee.h Officer.h Supervisor.h
	$(CC) $(CFLAGS) main.cpp

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp

Officer.o: Officer.cpp Officer.h Employee.h
	$(CC) $(CFLAGS) Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h Employee.h
	$(CC) $(CFLAGS) Supervisor.cpp

clean:
	rm -f *.o *~ $(TARGET)
