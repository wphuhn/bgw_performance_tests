.PHONY: all clean

all:  clean
	ln -s ${MF_DIR}/vxc.dat
	ln -s ${MF_DIR}/WFN_inner
	ln -s ../EPSILON/eps0mat.h5
	ln -s ../EPSILON/epsmat.h5
	${MPI_CMD} ${SIG_EXE}

clean:
	rm -f *.h5 *.log *.dat WFH_inner

