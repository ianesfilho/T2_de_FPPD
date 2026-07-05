# T2_de_FPPD

Estrutura do repositorio:
T2-FPPD/
+-- go.mod
+-- go.sum
+-- sequencial/
| +-- main.go
+-- paralelo/
+-- main.go

Instruções de compilação e execução:
Entrando no cluster, podemos executar os comandos:
- necessário ter clonado no cluster o repositório "https://github.com/ianesfilho/T2_de_FPPD.git"
- depois "ls"
- "cd T2_de_FPPD"
- ls
- e então "srun -N 1 -n 1 ./seq" para rodar a versão sequencial do programa (pois já realizamos o "go build -o seq ./sequencial")
- depois, fazemos "srun -N 1 -n 2 ./par" para rodar a versão paralela com 1 nó e 2 processos (pois já realizamos o "go build -o par ./paralelo")
- "srun -N 1 -n 4 ./par" para rodar com 1 nó e 4 processos
- "srun -N 1 -n 8 ./par" 1 nó e 8 processos
- "srun -N 1 -n 2 ./par" 1 nó e 16 processos
- "srun -N 2 -n 8 ./par" 2 nós e 8 processos
- "srun -N 4 -n 8 ./par" 4 nós e 8 processos
- "srun -N 2 -n 16 ./par" 2 nós e 16 processos
