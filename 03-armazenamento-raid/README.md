# 💾 Armazenamento com RAID (RAID 1 e RAID 5)

## 📌 Objetivo

Configurar volumes RAID no Windows Server para garantir **tolerância a falhas**, **disponibilidade** e melhor uso do armazenamento.

---

## 🧠 Conceito de RAID

RAID (Redundant Array of Independent Disks) é uma técnica que combina múltiplos discos físicos para:

* Aumentar segurança dos dados
* Melhorar desempenho
* Garantir disponibilidade do sistema

---

## 🔁 RAID 1 — Espelhamento

### 📖 Descrição

O RAID 1 cria uma cópia exata dos dados em dois discos.

👉 Tudo que é gravado em um disco é replicado no outro.

---

### ⚙️ Requisitos

* Mínimo: **2 discos**
* Tamanho igual recomendado

---

### 🚀 Configuração no Windows Server

1. Acessar:

   * **Gerenciamento de Disco**
2. Inicializar os discos como:

   * **GPT (recomendado)**
3. Clicar com botão direito em um disco:

   * Selecionar **Novo Volume Espelhado**
4. Adicionar o segundo disco
5. Definir:

   * Letra da unidade
   * Nome do volume
6. Confirmar conversão para:

   * **Disco Dinâmico**
7. Finalizar a criação

---

### ✅ Resultado Esperado

* Volume com espelhamento ativo
* Dados duplicados automaticamente
* Tolerância à falha de 1 disco

---

### ⚠️ Recuperação de Falha

Caso um disco apresente problema:

1. Acessar **Gerenciamento de Disco**
2. Clicar no volume RAID
3. Selecionar:

   * **Remover espelho**
4. Adicionar um novo disco
5. Recriar o espelhamento

---

## 🧠 RAID 5 — Paridade

### 📖 Descrição

O RAID 5 distribui dados e informações de paridade entre os discos.

👉 Permite reconstrução dos dados em caso de falha de um disco.

---

### ⚙️ Requisitos

* Mínimo: **3 discos**
* Tamanho igual obrigatório

---

### 🚀 Configuração no Windows Server

1. Acessar:

   * **Gerenciamento de Disco**
2. Garantir que existam pelo menos **3 discos disponíveis**
3. Clicar com botão direito:

   * **Novo Volume RAID-5**
4. Adicionar os discos
5. Definir:

   * Letra da unidade
   * Nome do volume
6. Escolher tipo de formatação:

   * ❗ **Não utilizar formatação rápida**
7. Confirmar conversão para:

   * **Discos Dinâmicos**
8. Finalizar

---

### ✅ Resultado Esperado

* Volume RAID 5 ativo
* Distribuição de dados + paridade
* Tolerância à falha de 1 disco

---

## 📊 Comparação RAID 1 vs RAID 5

| Característica   | RAID 1  | RAID 5           |
| ---------------- | ------- | ---------------- |
| Discos mínimos   | 2       | 3                |
| Segurança        | Alta    | Média/Alta       |
| Desempenho       | Médio   | Alto (leitura)   |
| Aproveitamento   | 50%     | Maior que RAID 1 |
| Tolerância falha | 1 disco | 1 disco          |

---

## 📌 Boas Práticas

* Sempre utilizar discos do mesmo tamanho
* Monitorar estado dos discos regularmente
* Evitar RAID como única forma de backup
* Planejar crescimento de armazenamento

---

## ⚠️ Observações Importantes

* RAID melhora disponibilidade, mas **não substitui backup**
* RAID 5 perde todos os dados se mais de um disco falhar
* Em ambientes reais, RAID pode ser implementado via hardware (controladora)

---

## 🧠 Visão Profissional

* RAID 1 → ideal para sistemas críticos com baixo custo
* RAID 5 → equilíbrio entre desempenho, segurança e capacidade
* RAID 10 (avançado) → alta performance + alta segurança

---
