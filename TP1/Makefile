include Make.inc
#include Make_msys2.inc
#include Make_osx.inc

CXXFLAGS = -std=c++11 -fPIC
ifdef DEBUG
CXXFLAGS += -g -O0 -Wall -fbounds-check -pedantic -D_GLIBCXX_DEBUG
else
CXXFLAGS += -O3 -march=native -Wall
endif

default:	help

all:	HelloWorld.exe Circulation_jeton.exe Circulation_jeton_bis.exe Calcul_de_pi.exe Calcul_de_pi_async.exe Diffusion_hypercube.exe 

HelloWorld.exe:	HelloWorld.cpp
	$(CXX) $(CXXFLAGS) -o HelloWorld.exe HelloWorld.cpp $(LIB)

Circulation_jeton.exe:	Circulation_jeton.cpp
	$(CXX) $(CXXFLAGS) -o Circulation_jeton.exe Circulation_jeton.cpp $(LIB)

Circulation_jeton_bis.exe:	Circulation_jeton_bis.cpp
	$(CXX) $(CXXFLAGS) -o Circulation_jeton_bis.exe Circulation_jeton_bis.cpp $(LIB)

Calcul_de_pi.exe:	Calcul_de_pi.cpp
	$(CXX) $(CXXFLAGS) -o Calcul_de_pi.exe Calcul_de_pi.cpp $(LIB)

Calcul_de_pi_async.exe:	Calcul_de_pi_async.cpp
	$(CXX) $(CXXFLAGS) -o Calcul_de_pi_async.exe Calcul_de_pi_async.cpp $(LIB)

Diffusion_hypercube.exe:	Diffusion_hypercube.cpp
	$(CXX) $(CXXFLAGS) -o Diffusion_hypercube.exe Diffusion_hypercube.cpp $(LIB)

help: 
	@echo "Available targets : "
	@echo "    all                      : compile all executables"
	@echo "    HelloWorld.exe           : compile HelloWorld executable"
	@echo "    Circulation_jeton.exe    : compile Circulation_jeton executable"
	@echo "    Circulation_jeton_bis.exe    : compile Circulation_jeton_bis executable"
	@echo "    Calcul_de_pi.exe         : compile Calcul_de_pi executable"
	@echo "    Calcul_de_pi_async.exe         : compile Calcul_de_pi_async executable"
	@echo "    Diffusion_hypercube.exe  : compile Diffusion_hypercube executable"
	@echo "Add DEBUG=yes to compile in debug"
	@echo "Configuration :"
	@echo "    CXX      :    $(CXX)"
	@echo "    CXXFLAGS :    $(CXXFLAGS)"

clean:
	@rm -f *.exe *~ 

