# 🖥️ Windows Server 2022 Lab — Active Directory, DHCP & File Services

> 📌 Projeto prático de laboratório focado na implementação de uma infraestrutura corporativa utilizando Windows Server.

---

## 🚀 Visão Geral

Este repositório documenta a criação de um ambiente completo de rede corporativa em laboratório, incluindo:

* Controlador de Domínio (Active Directory)
* Gerenciamento de usuários e grupos
* DHCP (Dynamic Host Configuration Protocol)
* RAID (armazenamento resiliente)
* Compartilhamento de arquivos com controle de acesso
* Scripts de logon e mapeamento de rede
* Gerenciamento de cotas de armazenamento

💡 Todo o processo foi realizado de forma prática, simulando um ambiente real de empresa.

---

## 🧠 Objetivo do Projeto

Desenvolver habilidades práticas em:

* Administração de servidores Windows
* Estruturação de ambientes corporativos
* Controle de acesso e segurança
* Automação básica com scripts
* Boas práticas de infraestrutura

---

## 🏗️ Arquitetura do Ambiente

```bash
[ CLIENTE WINDOWS 11 ]
          │
          ▼
[ DHCP + DNS + AD ]
          │
          ▼
[ FILE SERVER + RAID ]
```

---

## ⚙️ Ambiente de Laboratório

| Recurso       | Configuração        |
| ------------- | ------------------- |
| Virtualização | VirtualBox          |
| Sistema       | Windows Server 2022 |
| RAM           | 4GB                 |
| CPU           | 4 vCPUs             |
| Armazenamento | 50GB                |
| Rede          | 3 NICs (Teaming)    |

---

## 📁 Estrutura do Repositório

```bash
📁 windows-server-active-directory
 ┣ 📁 01-instalacao-windows-server
 ┣ 📁 02-configuracao-inicial
 ┣ 📁 03-armazenamento-raid
 ┣ 📁 04-active-directory
 ┣ 📁 05-dhcp
 ┣ 📁 06-usuarios-e-grupos
 ┣ 📁 07-compartilhamento
 ┣ 📁 08-mapeamento-rede
 ┣ 📁 09-pastas-home
 ┣ 📁 10-cotas
 ┗ README.md
```

---

## 🔑 Principais Implementações

### 🏢 Active Directory

* Criação de domínio (`regis.tec`)
* Estrutura organizacional (OUs)
* Gerenciamento centralizado de usuários

### 🌐 DHCP

* Distribuição automática de IP
* Configuração de gateway e DNS
* Controle de escopo

### 💾 RAID

* RAID 1 (Espelhamento)
* RAID 5 (Paridade)
* Tolerância a falhas

### 📂 File Server

* Compartilhamento por setor:

  * Vendas
  * Compras
  * Gerência
* Controle de permissões por grupo

### 🔗 Automação

* Scripts de logon (.cmd)
* Mapeamento automático de unidades de rede

### 📊 Cotas

* Limitação de armazenamento por usuário/pasta
* Aplicação automática em subpastas

---

## 🔐 Segurança Aplicada

* Controle de acesso baseado em grupos
* Permissões NTFS configuradas corretamente
* Enumeração baseada em acesso (ABE)
* Restrição de login por horário/máquina

---

## 🧪 Testes Realizados

* Ingresso de máquina no domínio
* Autenticação de usuários
* Resolução de nomes (DNS / nslookup)
* Aplicação de permissões
* Funcionamento do DHCP

---

## ⚠️ Observações

* Ambiente criado exclusivamente para fins educacionais
* Senhas simples utilizadas apenas para laboratório
* Estrutura pode ser expandida com:

  * GPOs
  * Backup
  * Monitoramento

---

## 📈 Próximos Passos

* Implementação de Group Policy (GPO)
* Scripts em PowerShell
* Backup automatizado
* Monitoramento de rede

---

## 👨‍💻 Autor

**Reginaldo Tirolla Filho**

---

## ⭐ Destaque

Este projeto demonstra habilidades práticas essenciais para:

* Suporte Técnico
* Analista de Infraestrutura
* Administrador de Sistemas

---

## 📌 Como Usar

1. Navegue pelas pastas do projeto
2. Siga os guias passo a passo
3. Replique o ambiente no seu laboratório

---

## 🤝 Contribuição

Este é um projeto de estudo, mas sugestões são bem-vindas!

---

## 📜 Licença

Uso educacional.
