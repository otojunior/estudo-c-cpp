# Exemplo 01 Makefile
#
# Help about Makefiles:
# http://mrbook.org/blog/tutorials/make/
#
# Syntax:
#	target: dependencies
#	[tab] system command
#
# PRÉ-REQUISITO: Biblioteca estática do Google Test Framework criada.
# $<GTEST>/make> make

# Paths específicos
GTEST = d:/cpp/tools/gtest-1.7.0

# Configurações de compilação
AR = ar
CXX = g++
FLAGS = -O2 -Wall

all:
	$(CXX) $(FLAGS) -c Calculadora.cpp
	$(AR) crv libcalc.lib Calculadora.o
	
clean:
	rm -f *.o
	rm -f *.lib
	rm -f *.exe
	
test:
	$(CXX) $(FLAGS) -I $(GTEST)/include -o run_unit_tests \
		Calculadora.cpp \
		CalculadoraTest.cpp \
		$(GTEST)/make/gtest_main.a -lm