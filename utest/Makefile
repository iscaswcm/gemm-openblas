UTEST_CHECK = 1
TOPDIR	= ..

UTESTBIN=openblas_utest

.PHONY : all
.NOTPARALLEL : all run_test $(UTESTBIN)

include $(TOPDIR)/makefiles/Makefile.system

OBJS=utest_main.o 
#test_rot.o test_swap.o test_axpy.o test_dotu.o test_rotmg.o test_dsdot.o test_fork.o


all : run_test

$(UTESTBIN): $(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ ../$(LIBNAME) $(EXTRALIB) $(FEXTRALIB)

run_test: $(UTESTBIN)
ifndef CROSS
	./$(UTESTBIN)
endif

clean:
	-rm -f *.o $(UTESTBIN)

libs:

