# ⚙️ Configuração Inicial do Windows Server

## 📌 Objetivo

Realizar as configurações iniciais do servidor após a instalação, preparando o ambiente para a implementação de serviços como:

* Active Directory (AD DS)
* DHCP
* File Server
* Integração com estação cliente

---

## 🧪 Contexto do Ambiente

Este servidor faz parte de um ambiente virtualizado contendo:

* 🖥️ Servidor (Windows Server 2022)
* 💻 Estação cliente (Windows 10/11)

📌 Ambas as máquinas estão conectadas à mesma rede interna (**REDE-LAB**), permitindo comunicação e simulação de um ambiente corporativo.

---

## 🚀 Acesso ao Gerenciador de Servidor

O **Server Manager** é a principal ferramenta de administração do Windows Server.

* É aberto automaticamente ao iniciar o sistema
* Caso não abra:

  * Menu Iniciar → Server Manager

---

## 🔧 Verificação e Inicialização de Serviços

1. Acessar:

   * **Server Manager → Servidor Local**
2. Verificar o status dos serviços
3. Caso algum serviço esteja parado:

   * Botão direito → **Iniciar**

📌 Garantir que todos os serviços essenciais estejam em execução antes de instalar novas funções.

---

## 🏷️ Alteração do Nome do Servidor

Padronizar o nome do servidor é uma boa prática em ambientes corporativos.

### 🚀 Passo a passo:

1. Acessar:

   * **Server Manager → Servidor Local**
2. Localizar:

   * Nome do computador
3. Clicar em **Alterar**
4. Definir o novo nome:

```bash id="8u3y1o"
SRVREGIS
```

5. Confirmar alteração
6. Reiniciar o servidor

---

## 🌐 Configuração de Rede (NIC Teaming)

O agrupamento de placas de rede permite:

* Maior disponibilidade (redundância)
* Melhor desempenho

---

### 🚀 Passo a passo:

1. Acessar:

   * **Server Manager → Servidor Local**
2. Localizar:

   * **NIC Teaming (Agrupamento de NIC)**
3. Clicar em **Desabilitado**
4. Em **Tarefas** → selecionar:

   * **Nova Equipe**
5. Definir:

   * Nome da equipe (ex: `TEAM-SRV`)
6. Selecionar as **3 placas de rede**
7. Configurar:

   * Modo de balanceamento:

     * **Hash de endereço**
8. Confirmar criação

---

## 📡 Verificação de Rede

Após a configuração, validar conectividade:

### ✔ Verificar IP do servidor

```cmd id="9dhljp"
ipconfig
```

---

### ✔ Testar comunicação com cliente

```cmd id="m3lmx7"
ping 192.168.x.x
```

📌 (IP da estação cliente)

---

## ✅ Resultado Esperado

* Servidor com nome padronizado (**SRVREGIS**)
* Serviços ativos e funcionando
* NIC Teaming configurado
* Comunicação de rede funcional

---

## 📌 Boas Práticas

* Padronizar nomes de servidores (ex: SRV + função)
* Validar serviços antes de instalar novas funções
* Utilizar múltiplas interfaces de rede quando possível

---

## ⚠️ Observações

* Após renomear o servidor, o reinício é obrigatório
* O NIC Teaming pode variar conforme o ambiente virtual
* A comunicação com o cliente depende da configuração correta da rede interna

---

## 🧠 Visão Profissional

A configuração inicial define a base de estabilidade do servidor.

👉 Um erro nessa etapa pode impactar diretamente:

* Active Directory
* DHCP
* Autenticação de usuários
* Comunicação de rede

📌 Por isso, essa etapa é crítica em qualquer ambiente corporativo.
