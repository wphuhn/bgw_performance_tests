.PHONY: all clean

all:  clean
	ln -s ${MF_DIR}/WFN_inner ./WFN_co
	ln -s ../EPSILON/epsmat.h5
	ln -s ../EPSILON/eps0mat.h5
	${MPI_CMD} ${KER_EXE}

clean:
	rm -f *.h5 WFN_co

