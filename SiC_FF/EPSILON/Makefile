.PHONY: all clean

all:  clean
	ln -s ../../mean_field/SiC/WFN.h5
	ln -s ../../mean_field/SiC/WFNq.h5
	${MPI_CMD} ${EPS_EXE}

clean:
	rm -f *.h5 *.log *.dat EpsDyn EpsInvDyn 

