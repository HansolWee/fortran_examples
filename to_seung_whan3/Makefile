### Compilers & flags
F90=gfortran

EXE = exec
F90SRC = main.f90 ModDemo.f90
F90OBJ = main.o ModDemo.o

### Targets
all: $(EXE)
run: $(EXE) 
	./$(EXE)

# Link object files to executables
$(EXE): $(F90OBJ)
	$(F90) -o $(EXE) $(F90OBJ)

# All .o files depend on the corresponding .f90 file
%.o: %.f90
	$(F90) -c $<

# Dependencies
main.o: ModDemo.o

clean:
	rm *.o *.mod $(EXE)

.PHONY: all run clean


