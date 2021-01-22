.PHONY: all clean

all:  clean
	ln -s ${MF_DIR}/VXC
	ln -s ${MF_DIR}/WFN_inner
	ln -s ../EPSILON/eps0mat.h5
	${MPI_CMD} ${SIG_EXE}

clean:
	rm -f *.h5 *.log *.dat WFN_inner VXC RHO

