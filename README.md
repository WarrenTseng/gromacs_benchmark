# Benchmark for GROMACS: Lysozeme in Water

## GPU Benchmark
### Start the GROMACS container
    docker run -it --rm --gpus=all --net=host -v /YOUR/GROMACS/WORKSPACE:/ws/gromacs -w /ws/gromacs nvcr.io/hpc/gromacs:2023.2 bash
### Benchmarking
    cd gromacs_benchmark/MD/
    chmod +x benchmark_gpu.sh
    ./benchmark_gpu.sh

## CPU Benchmark
### Start the GROMACS container
    docker run -it --rm --net=host -v /YOUR/GROMACS/WORKSPACE:/ws/gromacs -w /ws/gromacs gromacs/gromacs:2022.2 bash
### Benchmarking
    cd gromacs_benchmark/MD/
    chmod +x benchmark_cpu.sh
    ./benchmark_cpu.sh
