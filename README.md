# Sistemas Distribuídos
**Códigos de Exercícios e Atividades**

Estes códigos são exemplos de programação paralela com OpenMP e MPI. </br>
&emsp; <b> Parallel_1 </b> - Códigos hello_world serial e paralelo. </br>
&emsp; <b> Parallel_2 </b> - Códigos de um count sort serial e paralelo. </br>
&emsp; <b> Parallel_3 </b> - Código Fibonacci serial. </br>
&emsp; <b> Parallel_4 </b> - Exercício: Código de soma de elementos de um vetor. </br>
&emsp; <b> MPI_1 </b> - Códigos hello_mpi e um código simples com send e recv em MPI. </br>
&emsp; <b> MPI_2 </b> - Código exemplo de redução com MPI. </br>

Todos os códigos foram desenvolvidos em Linux. </br>
O Linux utilizado é o Linux Ubuntu Server 18 LTS. </br>
<b> LEMBRE_SE:</b> A máquina virtual precisa ter ao menos 2 CPUs. </br>
Os pacotes instalados foram: </br> 
&emsp; gcc (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0 </br>
&emsp; mpirun (Open MPI) 2.1.1 </br>
Para instalar os pacotes use: </br>
&emsp; apt-get install gcc openmpi-bin libopenmpi-dev git net-tools </br>

<b> Preparação do ambiente Linux para execução dos códigos. </b> </br>
OpenMP - é necessário definir a quantidade de threads utilizando uma variável de ambiente. Use o comando abaixo: </br>
&emsp; export OMP_NUM_THREADS=2 </br>
MPI - é necessário definir o parametro de MCA (Modular Component Architecture) para não alertar a falta de rede Infiniband. Use o comando abaixo: </br>
&emsp; export OMPI_MCA_btl_base_warn_component_unused=0 </br>

<b> Parallel_1 </b> </br> 
Para compilar use os exemplos abaixo: </br>
&emsp; gcc -o hello hello.c </br> 
&emsp; gcc -o parallel_hello -fopenmp parallel_hello.c </br>
Após compilar os códigos é possível executá-los via terminal com os comandos: </br>
&emsp; ./hello </br>
&emsp; ./parallel_hello </br>

<b> Parallel_2 </b> </br>
Para compilar use os exemplos abaixo: </br>
&emsp; gcc -o sort_serial -fopenmp sort_serial.c </br>
&emsp; gcc -o sort_parallel -fopenmp sort_parallel.c </br>
Após compilar os códigos é possível executá-los indicando o arquivo de entrada via terminal com os comandos: </br>
&emsp; ./sort_serial < arq3.in </br>
&emsp; ./sort_parallel < arq3.in </br>

<b> Parallel_3 </b> </br>
Exercício: Código de uma sequência de Fibonacci em serial. </br>
Este é o primeiro exercício de paralelização de código. </br>

<b> Parallel_4 </b> </br>
Exercício: Código de soma de elementos de um vetor. </br>
Veja o código serial em C e utilize seus conhecimentos para paralelizar o código com OpenMP e MPI. </br>
Neste diretório está o código serial em C e em Python, dessa forma, pode-se comparar o desempenho de cada linguagem. </br>
Para compilar use os exemplos abaixo: </br>
&emsp; gcc -o soma -fopenmp soma.c </br>
Após compilar o código em C é possível executar ambos em terminal com os comandos: </br>
&emsp; ./soma </br>
&emsp; python3 ./soma.py </br>

<b> MPI_1 </b> </br>
Códigos hello_mpi e um código simples com send e recv em MPI.
Para compilar use os exemplos abaixo: </br>
&emsp; mpicc -o simples simples.c </br>
&emsp; mpicc -o hello_mpi hello_mpi.c </br>
Após compilar o código em C com MPI é possível executar ambos em terminal com os comandos: </br>
&emsp; mpirun -n 2 ./hello_mpi </br>
&emsp; mpirun -n 2 ./simples </br>

<b> MPI_2 </b> </br>
Código exemplo de redução com MPI. </br>
Para compilar use os exemplos abaixo: </br>
&emsp; mpicc -o reduce_mpi reduce_mpi.c </br>
Após compilar o código em C com MPI é possível executar em terminal com o comando: </br>
&emsp; mpirun -n 2 ./reduce_mpi </br>


<b> Referências </b> </br>
Exercícios Prof. Guido Araújo - Unicamp </br>
Prof. Gabriel P. Silva - UFRJ - Programação Paralela e Distribuída - Um curso prático </br>
Prof. Gabriel P. Silva - UFRJ - Programação Paralela com MPI - Um Curso Prático - 2019 </br>
Cenapad - Introdução ao OpenMP - 2014 </br>
Cenapad - Introdução ao MPI - 2012 </br>
