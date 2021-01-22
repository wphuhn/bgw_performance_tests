.PHONY: all clean

all:  clean
	ln -s ../../mean_field/SiC/vxc.dat
	ln -s ../../mean_field/SiC/WFN_inner
	ln -s ../EPSILON/eps0mat.h5
	ln -s ../EPSILON/epsmat.h5
	${MPI_CMD} ${SIG_EXE}

clean:
	rm -f *.h5 *.log *.dat WFN_inner

