# CP01 - Priorização Logística com Estruturas de Dados

## Sobre o Projeto

Este projeto foi desenvolvido para o **Checkpoint 01 (CP01)** com o objetivo de aplicar conceitos de:

* Estruturas de Dados
* Algoritmos
* Análise de Complexidade (Big O)

em um cenário prático de **logística no Brasil**.

A solução simula dois contextos distintos:

* **Enunciado A (RM PAR)** → Centro de distribuição com fila de pedidos
* **Enunciado B (RM ÍMPAR)** → Sistema de fretes e entregas

### Descrição dos arquivos

* `CP_DYNAMIC_01.ipynb`
  → Notebook para o cenário **ímpar (fretes e entregas)**

* `CP_DYNAMIC_01-par.ipynb`
  → Notebook para o cenário **par (centro de distribuição)**

* `*.csv`
  → Datasets utilizados em cada cenário

---

## Objetivo

Simular sistemas logísticos capazes de:

* Priorizar operações
* Organizar fluxo de processamento
* Aplicar regras de negócio reais

---

## Abordagem da Solução

A solução segue um pipeline estruturado:

```text
Entrada → Processamento → Score → Regras → Classificação → Ordenação → Fila → Execução
```

### Etapas principais:

1. Leitura do dataset
2. Feature engineering
3. Cálculo de score de prioridade
4. Aplicação de regras de negócio
5. Classificação (alta, média, baixa)
6. Ordenação dos dados
7. Simulação de fila com `deque`
8. Processamento recursivo
9. Geração de gráfico

---

## Estruturas de Dados Utilizadas

| Estrutura  | Uso                  | Complexidade |
| ---------- | -------------------- | ------------ |
| DataFrame  | Manipulação de dados | O(n)         |
| Lista      | Armazenamento de IDs | O(n)         |
| Deque      | Fila (FIFO)          | O(1)         |
| Dicionário | Mapeamento rápido    | O(1)         |
| Tupla      | Estrutura imutável   | O(1)         |

---

## Lógica de Priorização

Cada item (pedido ou entrega) recebe um **score de prioridade**, baseado em:

* Urgência / prioridade do cliente
* Tempo ou prazo
* Valor financeiro
* Situação operacional

Regras adicionais aumentam a prioridade em cenários críticos.

---

## Complexidade Computacional (Big O)

| Etapa               | Complexidade   |
| ------------------- | -------------- |
| Feature engineering | O(n)           |
| Cálculo de score    | O(n)           |
| Regras de negócio   | O(n)           |
| Classificação       | O(n)           |
| Ordenação           | **O(n log n)** |
| Recursão            | O(n)           |

### Análise

A solução é majoritariamente linear (**O(n)**), sendo a ordenação o principal custo computacional.

---

## Execução do Projeto

### Instalação

```bash
pip install pandas matplotlib
```

---

### Executar via notebook

* Para RA **ÍMPAR**:
  → `CP_DYNAMIC_01.ipynb`

* Para RA **PAR**:
  → `CP_DYNAMIC_01-par.ipynb`

---

## Visualização

O projeto gera gráficos que mostram:

* Distribuição de prioridades
* Análise da carga logística

---

## Justificativa Técnica

A solução foi construída priorizando:

* Clareza do fluxo
* Uso de estruturas eficientes
* Aplicação prática de conceitos teóricos

A recursão foi utilizada com objetivo didático.

---

## 🧑‍💻  Equipe

Projeto desenvolvido por:

* Davi Marques de Andrade Munhoz - 566223
* Diogo Oliveira Lima - 562559
* Leandro Simoneli da Silva - 566539
* Lucas dos Reis Aquino - 562414
* Lucas Perez Bonato - 565356