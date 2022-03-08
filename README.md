# Sistemas Distribuídos
**Códigos de Exercícios e Atividades**

Estes códigos são exemplos de programação paralela com OpenMP. </br>
&emsp; Parallel_1 - Códigos hello_world serial e paralelo. </br>
&emsp; Parallel_2 - Códigos de um count sort serial e paralelo. </br>
&emsp; Parallel_3 - Código Fibonacci serial  </br>

Os códigos foram desenvolvidos em Linux. Para compilar use os exemplos abaixo: </br>
&emsp; gcc -o hello hello.c </br> 
&emsp; gcc -o parallel_hello -fopenmp parallel_hello.c </br>
    
O Linux utilizado é o Linux Ubuntu Server 18 LTS. </br>
Os pacotes instalados foram: </br> 
&emsp; gcc (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0 </br>
&emsp; mpirun (Open MPI) 2.1.1 </br>
Para instalar os pacotes use: </br>
&emsp; apt-get install gcc openmpi-bin git net-tools </br>


Parallel_1 </br> 
Após compilar os códigos é possível executá-los via terminal com os comandos: </br>
&emsp; ./hello </br>
&emsp; ./parallel_hello </br>

Parallel_2 </br>
Após compilar os códigos é possível executá-los indicando o arquivo de entrada via terminal com os comandos: </br>
&emsp; ./sort_serial < arq3.in </br>
&emsp; ./sort_parallel < arq3.in </br>
    
 

