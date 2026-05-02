# 📂 Compartilhamento e Permissões (File Server)

## 📌 Objetivo

Configurar o compartilhamento de pastas no servidor e aplicar permissões de acesso utilizando grupos do Active Directory, garantindo segurança e organização dos dados.

---

## 🧪 Contexto do Ambiente

Este processo foi realizado em um ambiente virtualizado contendo:

* 🖥️ Servidor (Windows Server 2022 com AD DS e DHCP)
* 💻 Estação cliente (Windows 10/11)

📌 O servidor atua como File Server e Controlador de Domínio (**regis.tec**), e a estação cliente é utilizada para validar acessos.

---

## 🧠 Conceito

O File Server permite:

* Compartilhar arquivos na rede
* Controlar acesso por usuário ou grupo
* Centralizar dados corporativos

👉 Em ambientes profissionais, o acesso é controlado por **grupos**, não diretamente por usuários.

---

## 📁 Estrutura de Pastas

Criar a seguinte estrutura no servidor:

```bash
C:\EMPRESA
 ┣ 📁 VENDAS
 ┣ 📁 COMPRAS
 ┗ 📁 GERENCIA
```

---

## 🚀 Criação das Pastas

1. Acessar:

   * Disco local (C:)
2. Criar pasta:

   * **EMPRESA**
3. Dentro dela, criar:

   * VENDAS
   * COMPRAS
   * GERENCIA

---

## 🔗 Compartilhamento das Pastas

### 🚀 Passo a passo

1. Botão direito na pasta **EMPRESA**
2. Selecionar:

   * **Propriedades**
3. Aba:

   * **Compartilhamento**
4. Clicar em:

   * **Compartilhamento Avançado**
5. Marcar:

   * **Compartilhar esta pasta**
6. Nome do compartilhamento:

```bash
EMPRESA
```

---

## 🔐 Permissões de Compartilhamento

1. Clicar em:

   * **Permissões**
2. Remover:

   * **Everyone**
3. Adicionar grupos:

* VENDAS
* COMPRAS
* GERENTE

4. Definir permissões:

* Leitura ou Controle total (depende do cenário)

---

## 🔒 Permissões NTFS (Segurança)

As permissões NTFS são as mais importantes.

### 🚀 Passo a passo

1. Aba:

   * **Segurança**
2. Clicar em:

   * **Editar**
3. Remover acessos desnecessários
4. Adicionar grupos:

* VENDAS → acesso à pasta VENDAS
* COMPRAS → acesso à pasta COMPRAS
* GERENTE → acesso total

---

## 📌 Regra importante

👉 A permissão final é a combinação de:

* Permissão de compartilhamento
* Permissão NTFS

📌 Sempre prevalece a mais restritiva.

---

## 💻 Teste na Estação Cliente

### ✔ Acessar compartilhamento

Pressionar:

```bash
Windows + R
```

E digitar:

```bash
\\SRVREGIS\EMPRESA
```

---

### ✔ Validar acesso

* Usuário de VENDAS → acessa apenas VENDAS
* Usuário de COMPRAS → acessa apenas COMPRAS
* GERENTE → acessa tudo

---

## ✅ Resultado Esperado

* Pastas compartilhadas funcionando
* Permissões aplicadas corretamente
* Usuários acessando apenas o que devem
* Controle centralizado via grupos

---

## 📌 Boas Práticas

* Utilizar grupos para controle de acesso
* Nunca aplicar permissões diretamente em usuários
* Separar permissões por setor
* Manter organização de pastas padronizada

---

## ⚠️ Observações

* Permissões mal configuradas podem expor dados
* Sempre testar com usuários diferentes
* O acesso depende do login no domínio

---

## 🧠 Visão Profissional

O File Server é um dos serviços mais utilizados em empresas.

👉 É aqui que se aplica na prática:

* Segurança
* Controle de acesso
* Organização de dados

📌 Saber configurar corretamente permissões é uma habilidade essencial em infraestrutura.

---
