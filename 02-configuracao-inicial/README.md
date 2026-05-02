# ⚙️ Configuração Inicial do Windows Server

## 📌 Objetivo

Realizar as configurações iniciais do servidor após a instalação, preparando o ambiente para a implementação de serviços como Active Directory, DHCP e File Server.

---

## 🚀 Acesso ao Gerenciador de Servidor

O **Server Manager** é a principal ferramenta de administração do Windows Server.

* Ele é aberto automaticamente ao iniciar o sistema
* Caso não abra:

  * Menu Iniciar → Server Manager

---

## 🔧 Verificação e Inicialização de Serviços

1. Acessar:

   * **Server Manager → Servidor Local**
2. Verificar o status dos serviços
3. Caso algum serviço esteja parado:

   * Clicar com o botão direito
   * Selecionar **Iniciar**

📌 Garantir que todos os serviços essenciais estejam em execução

---

## 🏷️ Alteração do Nome do Servidor

Padronizar o nome do servidor é uma boa prática em ambientes corporativos.

### Passo a passo:

1. Acessar:

   * **Server Manager → Servidor Local**
2. Localizar:

   * Nome do computador
3. Clicar em **Alterar**
4. Definir o novo nome:

```
SRVREGIS
```

5. Confirmar alteração
6. Reiniciar o servidor

---

## 🌐 Configuração de Rede (NIC Teaming)

O agrupamento de placas de rede aumenta:

* Disponibilidade (redundância)
* Desempenho

### Passo a passo:

1. Acessar:

   * **Server Manager → Servidor Local**
2. Localizar:

   * **NIC Teaming (Agrupamento de NIC)**
3. Clicar em **Desabilitado** → abrir configurações
4. Em **Tarefas**, selecionar:

   * **Nova Equipe**
5. Definir:

   * Nome da equipe (ex: TEAM-SRV)
6. Selecionar as **3 placas de rede**
7. Configurar:

   * Modo de balanceamento:

     * **Hash de endereço**
8. Confirmar criação

---

## ✅ Resultado Esperado

* Servidor com nome padronizado (**SRVREGIS**)
* Serviços ativos e funcionando
* Placas de rede agrupadas (NIC Teaming configurado)

---

## 📌 Boas Práticas

* Nunca utilizar servidor com apenas uma placa de rede em ambiente corporativo
* Sempre padronizar nomes de servidores (ex: SRV + função ou nome)
* Validar serviços antes de instalar novas funções

---

## ⚠️ Observações

* Após renomear o servidor, o reboot é obrigatório
* O NIC Teaming pode variar dependendo do ambiente virtual

---
