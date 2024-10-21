
# 📦 Algoritmo Genético para Localização de Centros de Distribuição

Bem-vindo ao projeto **Algoritmo Genético para Localização de Centros de Distribuição**! Este repositório contém um notebook em Python que implementa um algoritmo genético para resolver o problema de localização de centros de distribuição ou fábricas (Facility Location Problem). O objetivo é selecionar o melhor centro de distribuição para minimizar os custos totais de transporte, atendendo à demanda de todos os clientes. Vamos explorar o que este notebook faz e como utilizá-lo. 🚀

## 📚 Índice

- [Visão Geral](#visão-geral)
- [Descrição do Problema](#descrição-do-problema)
- [Estrutura dos Dados de Entrada](#estrutura-dos-dados-de-entrada)
- [Como Funciona o Algoritmo Genético](#como-funciona-o-algoritmo-genético)
- [Dependências](#dependências)
- [Uso](#uso)
- [Saída](#saída)

## 📋 Visão Geral

Este notebook utiliza um algoritmo genético para resolver o problema de localização de centros de distribuição, visando minimizar os custos totais de transporte, respeitando as capacidades dos centros e atendendo às demandas dos clientes.

## 🧬 Como Funciona o Algoritmo Genético

O algoritmo genético é uma técnica de otimização inspirada no processo de seleção natural. A seguir estão os passos gerais de como ele resolve o problema de localização de centros de distribuição:

1. **Representação da Solução (Cromossomos):**
   Cada solução possível é representada como um cromossomo, geralmente uma lista binária indicando se um centro de distribuição está ativo (1) ou não (0).

2. **Inicialização da População:**
   Uma população inicial de soluções é gerada aleatoriamente.

3. **Avaliação de Fitness:**
   Cada solução é avaliada com base em uma função de fitness, que neste caso é o custo total de transporte.

4. **Seleção:**
   Soluções são selecionadas para reprodução com base em sua fitness. Soluções melhores têm uma maior probabilidade de serem selecionadas.

5. **Crossover (Recombinação):**
   Combina duas soluções selecionadas para criar novas soluções (filhos), trocando partes dos cromossomos dos pais.

6. **Mutação:**
   Pequenas alterações aleatórias são feitas nas novas soluções para manter a diversidade genética.

7. **Substituição:**
   As novas soluções substituem algumas das soluções antigas na população, criando uma nova geração.

8. **Critério de Parada:**
   O processo continua até que um critério de parada seja atingido, como um número máximo de gerações ou uma melhoria mínima na fitness.

Este método é eficaz para explorar um grande espaço de soluções e encontrar uma solução próxima do ótimo global, evitando que o algoritmo fique preso em ótimos locais.

## 🔍 Descrição do Problema

O notebook visa:
1. **Minimizar o Custo Total:** Selecionar os centros de distribuição que minimizem o custo total de transporte.
2. **Atender a Demanda:** Garantir que a demanda de todos os clientes seja atendida.
3. **Respeitar as Capacidades:** Assegurar que as capacidades dos centros de distribuição não sejam excedidas.

### 🏭 Detalhes do Problema

Dados fictícios de exemplo:
- **Clientes:** Lista de clientes com suas respectivas demandas e coordenadas geográficas.
- **Centros de Distribuição:** Lista de centros com suas capacidades e coordenadas.
- **Custos Unitários de Transporte:** Matriz de custos unitários de transporte entre centros e clientes.

O notebook define o seguinte:
- **Variáveis de Decisão:** Seleção de centros de distribuição ativos.
- **Função Objetivo:** Minimizar o custo total de transporte.
- **Restrições:** Garantir atendimento da demanda e não exceder as capacidades dos centros.

## 🗂 Estrutura dos Dados de Entrada

1. **Clientes:** Arquivo Excel com colunas `Nome`, `Demanda`, `Latitude`, `Longitude`.
2. **Centros de Distribuição:** Arquivo Excel com colunas `Nome`, `Capacidade`, `Latitude`, `Longitude`.
3. **Custos Unitários de Transporte:** Arquivo Excel com uma matriz de custos onde linhas representam centros e colunas representam clientes.

## 🛠 Dependências

Certifique-se de ter as seguintes dependências instaladas:

- Python 3.x
- Pandas
- NumPy
- Geopy

Instale-as usando pip:

```bash
pip install numpy pandas geopy
```

## 🚀 Uso

1. Clone este repositório e execute o notebook:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd <NOME_DO_REPOSITORIO>
   jupyter notebook FacilityLocationGeneticAlgorithm.ipynb
   ```

2. Carregue seus dados de clientes e centros nos formatos adequados (exemplos estão na pasta input).
3. Execute todas as células do notebook para encontrar a melhor solução.

## 📈 Saída

Após executar o notebook, você obterá:

- **Centro de Distribuição Selecionado:** Nome do centro selecionado.
- **Melhor Solução:** Configuração dos centros de distribuição ativos.
- **Custo Total:** Custo total de transporte otimizado.

### Exemplo de Saída

```plaintext
Centro de Distribuição Selecionado: Centro_X
Melhor solução: [0, 1, 0, 0]
Custo total: 123456.78
```

---

Feito com 🧠 por [Vitor Tatekawa](https://github.com/vtatekawa)
