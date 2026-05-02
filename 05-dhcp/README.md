# 🌐 DHCP (Dynamic Host Configuration Protocol)

## 📌 Objetivo

Instalar e configurar o serviço DHCP no Windows Server para distribuição automática de endereços IP e parâmetros de rede para a estação cliente.

---

## 🧪 Contexto do Ambiente

Este serviço foi configurado em um ambiente virtualizado contendo:

* 🖥️ Servidor (Windows Server 2022)
* 💻 Estação cliente (Windows 10/11)

📌 Ambas as máquinas estão conectadas à mesma rede interna (**REDE-LAB**), permitindo comunicação e obtenção automática de IP.

---

## 🧠 Conceito

O DHCP é responsável por:

* Distribuir endereços IP automaticamente
* Definir gateway padrão
* Informar servidor DNS
* Evitar conflitos de IP na rede

👉 Sem DHCP, a configuração de rede seria manual em cada máquina.

---

## 📦 Instalação do DHCP

### 🚀 Passo a passo

1. Acessar:

   * **Server Manager**
2. Clicar em:

   * **Gerenciar → Adicionar Funções e Recursos**
3. Selecionar:

   * **Instalação baseada em função ou recurso**
4. Escolher o servidor
5. Marcar:

   * **Servidor DHCP**
6. Avançar e clicar em **Instalar**

---

## ⚙️ Configuração Inicial do DHCP

Após a instalação:

1. Clicar na **bandeira de notificação**
2. Selecionar:

   * **Configuração do DHCP**
3. Avançar e concluir a configuração

---

## 🌐 Criação do Escopo DHCP

O escopo define a faixa de IPs que serão distribuídos.

---

### 🚀 Passo a passo

1. Acessar:

   * **Server Manager → Ferramentas → DHCP**
2. Expandir:

   * IPv4
3. Clicar com botão direito:

   * **Novo Escopo**
4. Avançar e configurar:

---

### 📌 Configuração utilizada no laboratório

* **Nome do escopo:** REDE-LAB
* **IP inicial:** 192.168.31.100
* **IP final:** 192.168.31.200
* **Máscara:** 255.255.255.0 (/24)
* **Duração:** 2 horas (laboratório)

---

### 🌐 Configurações adicionais

* **Gateway:**

  ```
  192.168.31.1
  ```

* **DNS:**

  ```
  192.168.31.10
  ```

📌 (IP do servidor)

---

## 🔄 Ativação do Escopo

1. Finalizar o assistente
2. Garantir que o escopo esteja **ativo**

---

## 💻 Teste na Estação Cliente

### ✔ Renovar IP

```cmd
ipconfig /release
ipconfig /renew
```

---

### ✔ Verificar IP recebido

```cmd
ipconfig
```

📌 O IP deve estar dentro da faixa configurada (ex: 192.168.31.100+)

---

### ✔ Testar conectividade

```cmd
ping 192.168.31.10
```

(Servidor)

---

### ✔ Testar resolução de nome

```cmd
nslookup regis.tec
```

---

## ✅ Resultado Esperado

* Cliente recebendo IP automaticamente
* Gateway configurado corretamente
* DNS funcional
* Comunicação com servidor ativa

---

## 📌 Boas Práticas

* Definir escopo organizado e documentado
* Reservar IPs fora do escopo para servidores
* Ajustar tempo de concessão conforme o ambiente
* Monitorar distribuição de IPs

---

## ⚠️ Observações

* O DHCP depende do funcionamento do DNS e da rede
* O cliente deve estar configurado para obter IP automaticamente
* Em redes maiores, pode haver múltiplos servidores DHCP

---

## 🧠 Visão Profissional

O DHCP é essencial em qualquer rede corporativa.

👉 Ele permite:

* Escalabilidade
* Facilidade de administração
* Redução de erros manuais

📌 Sem DHCP, o gerenciamento de rede se torna inviável em ambientes grandes.

---
