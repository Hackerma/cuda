NVCC=nvcc
BIN=main
SRC=main.cu
CUDAFLAGS= -D_FORCE_INLINES -Xcompiler -O3

$(BIN):
	$(NVCC) $(SRC) $(CUDAFLAGS) -o $(BIN)

all: $(BIN)

test:
	nvprof ./$(BIN)
	nvprof --print-gpu-trace ./$(BIN)
clean:
	$(RM) $(BIN)
