# Traveling Salesman Problem (TSP) Solver using Branch and Bound

Este projeto implementa uma solução para o Problema do Caixeiro Viajante (TSP) utilizando a técnica de Branch and Bound. O objetivo é encontrar o caminho de menor custo que visita todas as cidades exatamente uma vez e retorna à cidade de origem.

## Estrutura do Projeto

O projeto é composto pelas seguintes partes:

1. **Importações e Inicializações:** Configuração inicial das bibliotecas e variáveis globais.
2. **Funções Auxiliares:** Funções para encontrar os custos mínimos e copiar soluções temporárias.
3. **Função Principal de Recursão (`TSPRec`):** Implementa o algoritmo de Branch and Bound para explorar as possíveis rotas e realizar a poda de ramos.
4. **Função de Configuração (`TSP`):** Prepara a matriz de adjacência e inicia a chamada recursiva.
5. **Função de Leitura de Arquivo (`file_tsp`):** Lê a matriz de adjacência de um arquivo de entrada.
6. **Código Principal:** Executa a leitura do arquivo, inicializa variáveis e chama a função para resolver o TSP, exibindo os resultados.

## Como Usar

1. **Preparação do Arquivo de Entrada:**
   - O arquivo deve conter uma matriz de adjacência representando as distâncias entre as cidades, com cada linha representando as distâncias de uma cidade para as outras.

2. **Configuração do Caminho do Arquivo:**
   - Defina o caminho do arquivo de entrada na variável `file_path`.

3. **Execução do Código:**
   - Execute o código. Ele lerá a matriz de adjacência, resolverá o TSP usando Branch and Bound e imprimirá o custo mínimo, o caminho tomado, o número de iterações e o tempo de execução.

### Exemplo de Caminho de Arquivo

```python
file_path = "/path/to/your/tsp_file.txt"
```

## Saída Esperada

- **Minimum cost:** O custo mínimo da rota encontrada.
- **Path Taken:** O caminho tomado pelo caixeiro viajante.
- **Total iterations:** O número total de iterações realizadas pelo algoritmo.
- **Time taken:** O tempo total de execução do algoritmo.

## Requisitos

- Python 3.x
- Biblioteca `math`
- Biblioteca `time`

## Executando o Projeto

1. Coloque o arquivo de entrada contendo a matriz de adjacência no caminho especificado.
2. Execute o script Python.
3. Veja os resultados impressos no console.

## Exemplo de Uso

```python
# Defina o caminho do arquivo
file_path = "/content/drive/MyDrive/AEDIII/tsp3_1194.txt"

# Execute o código principal
adj = file_tsp(file_path)
N = len(adj)

final_path = [None] * (N + 1)
visited = [False] * N
final_res = maxsize
iteration_count = 0

start_time = time.time()
TSP(adj)
end_time = time.time()

time_taken = end_time - start_time

print("Minimum cost:", final_res)
print("Path Taken:", end=' ')
for i in range(N + 1):
    print(final_path[i], end=' ')

print("\nTotal iterations:", iteration_count)
print("Time taken: {:.6f} seconds".format(time_taken))
```
