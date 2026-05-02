# 🏢 Active Directory Domain Services (AD DS)

## 📌 Objetivo

Instalar e configurar o Active Directory Domain Services (AD DS), promovendo o servidor a **Controlador de Domínio (Domain Controller)** e criando uma estrutura centralizada de autenticação e gerenciamento de rede.

---

## 🧠 Conceito

O Active Directory é um serviço de diretório que permite:

* Gerenciar usuários, computadores e grupos
* Centralizar autenticação
* Aplicar políticas de segurança
* Organizar recursos da rede

---

## 📦 Instalação do AD DS

### 🚀 Passo a passo

1. Acessar:

   * **Server Manager (Gerenciador de Servidor)**
2. Clicar em:

   * **Gerenciar → Adicionar Funções e Recursos**
3. Selecionar:

   * **Instalação baseada em função ou recurso**
4. Escolher o servidor
5. Marcar:

   * **Active Directory Domain Services**
6. Avançar e clicar em **Instalar**

---

## 🚀 Promoção a Controlador de Domínio

Após a instalação:

1. Clicar na **bandeira de notificação**
2. Selecionar:

   * **Promover este servidor a um controlador de domínio**

---

## ⚙️ Configuração do Domínio

### 📌 Definições utilizadas no laboratório:

* **Nova floresta:** Sim
* **Nome do domínio:**

  ```
  regis.tec
  ```
* **Nível funcional:** padrão
* **Senha do modo de restauração (DSRM):**

  ```
  123@senac
  ```

---

## 🔄 Processo Final

1. Avançar nas configurações padrão
2. Validar pré-requisitos
3. Clicar em **Instalar**
4. Aguardar reinicialização automática

---

## ✅ Resultado Esperado

* Servidor promovido a **Controlador de Domínio**
* Domínio **regis.tec** criado
* Active Directory funcional
* DNS configurado automaticamente

---

## 🔐 Teste de Funcionamento

Após a instalação:

### ✔ Verificar domínio

1. Abrir:

   * Prompt de Comando (CMD)
2. Executar:

```cmd
nslookup regis.tec
```

---

### ✔ Ingressar máquina no domínio

1. Pressionar:

   * `Windows + Pause Break`
2. Acessar:

   * Configurações avançadas
3. Alterar:

   * Nome do computador → Domínio
4. Informar:

   * `regis.tec`
5. Inserir credenciais:

   * Usuário: Administrator
   * Senha: 123@senac
6. Reiniciar máquina

---

## 📌 Boas Práticas

* Utilizar nomes de domínio internos padronizados
* Documentar estrutura do domínio
* Separar usuários por setores futuramente (OUs)
* Manter controle de credenciais administrativas

---

## ⚠️ Observações

* O DNS é instalado automaticamente com o AD
* O servidor passa a ser responsável pela autenticação da rede
* Qualquer falha no DC impacta toda a rede

---

## 🧠 Visão Profissional

O Active Directory é o **coração da infraestrutura Windows**.

É através dele que são controlados:

* Usuários
* Permissões
* Acessos
* Políticas de segurança

👉 Dominar AD é essencial para atuar como:

* Suporte Técnico
* Analista de Infraestrutura
* Administrador de Sistemas

---
