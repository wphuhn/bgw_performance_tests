include ../make.sys

export MPI_CMD
export EPS_EXE
export SIG_EXE
export MF_DIR=${PWD}/../mean_field/SiC

.PHONY: all gw epsilon sigma clean

all: gw

gw:  epsilon sigma

epsilon:
	cd EPSILON && make

sigma:
	cd SIGMA && make

clean:
	cd EPSILON && make clean
	cd SIGMA && make clean

