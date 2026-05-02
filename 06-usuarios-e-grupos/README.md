# 👥 Usuários e Grupos no Active Directory

## 📌 Objetivo

Criar e gerenciar usuários e grupos no Active Directory, organizando o ambiente de forma estruturada e aplicando boas práticas de administração.

---

## 🧪 Contexto do Ambiente

Este processo foi realizado em um ambiente virtualizado contendo:

* 🖥️ Servidor (Windows Server 2022 com Active Directory)
* 💻 Estação cliente (Windows 10/11)

📌 O servidor atua como Controlador de Domínio (**regis.tec**) e a estação cliente é utilizada para testes de autenticação.

---

## 🧠 Conceito

O Active Directory permite:

* Criar usuários para acesso à rede
* Agrupar usuários por função ou setor
* Controlar permissões de forma centralizada

👉 Em ambientes corporativos, usuários nunca são gerenciados individualmente, e sim por grupos.

---

## 📂 Acesso à Ferramenta

1. Acessar:

   * **Server Manager → Ferramentas**
2. Abrir:

   * **Usuários e Computadores do Active Directory**

---

## 🏢 Criação de Unidade Organizacional (OU)

As OUs ajudam a organizar o ambiente.

### 🚀 Passo a passo

1. Botão direito no domínio (**regis.tec**)
2. Selecionar:

   * **Novo → Unidade Organizacional**
3. Definir nome (ex: `EMPRESA`)

---

## 👤 Criação de Usuários

### 🚀 Passo a passo

1. Acessar a OU criada
2. Botão direito → **Novo → Usuário**
3. Preencher:

   * Nome
   * Sobrenome
   * Nome de logon
4. Definir senha
5. Marcar:

   * Usuário deve alterar a senha no próximo logon

---

### 📌 Exemplo de usuários (laboratório)

* Professor (Sergio Marquina)
* Tóquio (Silene Oliveira)
* Berlim (Andrés de Fonollosa)
* Nairóbi (Ágata Jimenez)
* Rio (Aníbal Cortés)
* Moscou (Agustín Ramos)

---

## 👥 Criação de Grupos

### 🚀 Passo a passo

1. Botão direito na OU
2. Selecionar:

   * **Novo → Grupo**
3. Definir:

   * Nome do grupo
   * Tipo: Segurança
   * Escopo: Global

---

### 📌 Grupos criados

* VENDAS
* COMPRAS
* GERENTE

---

## 🔗 Adicionar Usuários aos Grupos

### 🚀 Passo a passo

1. Abrir o grupo desejado
2. Aba:

   * **Membros**
3. Clicar em:

   * **Adicionar**
4. Selecionar os usuários

---

## 🔐 Configurações Avançadas de Usuário

### ✔ Restringir horário de logon

1. Abrir propriedades do usuário
2. Aba:

   * **Conta**
3. Selecionar:

   * Horário de logon

---

### ✔ Restringir login por máquina

1. Ainda na aba **Conta**
2. Selecionar:

   * **Fazer logon em…**
3. Definir computadores permitidos

---

## 💻 Teste na Estação Cliente

### ✔ Login com usuário do domínio

1. Tela de login
2. Selecionar:

   * Outro usuário
3. Informar:

```bash
regis\usuario
```

4. Inserir senha

---

## ✅ Resultado Esperado

* Usuários criados no Active Directory
* Grupos organizados por setor
* Usuários vinculados aos grupos
* Login funcionando na estação cliente

---

## 📌 Boas Práticas

* Organizar usuários em OUs
* Utilizar grupos para controle de acesso
* Evitar atribuir permissões diretamente a usuários
* Padronizar nomes de usuários e grupos

---

## ⚠️ Observações

* O controle de acesso será aplicado através dos grupos
* As OUs serão utilizadas futuramente para aplicar GPOs
* Usuários devem ser criados com padrão definido

---

## 🧠 Visão Profissional

Gerenciamento de usuários é uma das tarefas mais importantes em infraestrutura.

👉 Em ambientes reais:

* Tudo é baseado em grupos
* Segurança depende da organização correta
* Erros nessa etapa podem comprometer o ambiente

📌 Dominar essa parte é essencial para qualquer profissional de TI.

---
