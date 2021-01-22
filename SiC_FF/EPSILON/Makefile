.PHONY: all clean

all:  clean
	ln -s ${MF_DIR}/WFN.h5
	ln -s ${MF_DIR}/WFNq.h5
	${MPI_CMD} ${EPS_EXE}

clean:
	rm -f *.h5 *.log *.dat EpsDyn EpsInvDyn

