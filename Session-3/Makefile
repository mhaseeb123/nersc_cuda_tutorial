all: vec_add-debug-printf vec_add-debug-memcheck
vec_add-debug-printf: vec_add-debug-printf.cu
	nvcc -G -Xcompiler -rdynamic --gpu-architecture=compute_70 $^ -o $@.exe

vec_add-debug-memcheck: vec_add-debug-memcheck.cu
	nvcc -G -Xcompiler -g -Xcompiler -rdynamic --gpu-architecture=compute_70 $^ -o $@.exe

clean:
	rm -f vec_add-debug-printf.exe vec_add-debug-memcheck.exe
