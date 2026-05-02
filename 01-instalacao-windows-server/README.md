# 🧱 Instalação do Ambiente (Windows Server + Estação Cliente)

## 📌 Objetivo

Criar um ambiente virtualizado completo para simular uma infraestrutura corporativa, contendo:

* Servidor Windows Server 2022
* Estação de trabalho Windows 10/11

📌 Ambas as máquinas serão utilizadas para testes de domínio, autenticação, rede e serviços como DHCP e File Server.

---

## 🧪 Estrutura do Laboratório

O ambiente foi criado utilizando o VirtualBox com duas máquinas virtuais:

---

### 🖥️ Servidor (Windows Server 2022)

* Função: Controlador de Domínio, DHCP e File Server
* RAM: 4GB
* CPU: 4 núcleos
* Armazenamento: 50GB
* Rede: 3 adaptadores

---

### 💻 Estação Cliente (Windows 10/11 Pro)

* Função: Cliente do domínio
* RAM: 2GB (mínimo recomendado)
* CPU: 2 núcleos
* Armazenamento: 30GB (mínimo recomendado)
* Rede: 1 adaptador

---

## 🌐 Configuração de Rede (IMPORTANTE)

Para funcionamento correto do ambiente:

* Servidor e cliente devem estar na **mesma rede interna**
* O nome da rede deve ser idêntico nas duas máquinas

### 📌 Exemplo:

```bash
Rede interna: REDE-LAB
```

---

### 🖥️ Configuração de rede no Servidor

* Adaptador 1 → Rede Interna (**REDE-LAB**)
* Adaptador 2 → Opcional
* Adaptador 3 → Opcional

---

### 💻 Configuração de rede no Cliente

* Adaptador 1 → Rede Interna (**REDE-LAB**)

---

⚠️ Caso essa configuração esteja incorreta:

* O cliente não encontrará o servidor
* O domínio não funcionará
* O DHCP não distribuirá IP

---

## 🚀 Instalação do Windows Server 2022

### 📥 Pré-requisitos

* ISO do Windows Server 2022
* VirtualBox instalado

---

### ⚙️ Passo a passo

1. Criar nova máquina virtual no VirtualBox
2. Configurar recursos conforme especificado
3. Iniciar a VM com a ISO
4. Selecionar:

   * **Windows Server 2022 Datacenter (Desktop Experience)**
5. Prosseguir com instalação personalizada
6. Selecionar o disco e instalar

---

### 🔐 Configuração inicial

Definir senha do administrador:

```bash
123@senac
```

📌 (Uso apenas em laboratório)

---

## 🚀 Instalação da Estação Cliente (Windows 10/11)

### 📥 Pré-requisitos

* ISO do Windows 10/11 Pro

---

### ⚙️ Passo a passo

1. Criar nova máquina virtual no VirtualBox
2. Configurar:

   * RAM: 2GB ou mais
   * CPU: 2 núcleos
   * Rede: mesma rede interna do servidor (**REDE-LAB**)
3. Iniciar a instalação com a ISO
4. Seguir o processo padrão do Windows

---

## 🔧 Instalação dos Drivers (VirtualBox)

Realizar em ambas as máquinas:

1. Menu da VM:

   * Dispositivos → Inserir imagem de CD dos adicionais
2. Abrir o Explorador de Arquivos
3. Executar o instalador
4. Reiniciar a máquina

---

## ✅ Teste de Comunicação

Após instalação das duas máquinas:

### No cliente:

```cmd
ping 192.168.x.x
```

(IP do servidor)

---

```cmd
nslookup regis.tec
```

(Será funcional após configuração do domínio)

---

## ✅ Resultado Esperado

* Servidor instalado e funcional
* Estação cliente instalada
* Comunicação entre as máquinas ativa
* Ambiente pronto para configuração de serviços (AD, DHCP, etc.)

---

## 📌 Observações

* A versão do Windows cliente deve ser **Pro ou superior**
* Windows Home não permite ingresso em domínio
* Ambas as máquinas devem estar na mesma rede virtual

---

## 🧠 Visão Profissional

Criar um ambiente com servidor + cliente permite:

* Testar autenticação real
* Validar políticas (GPO)
* Simular ambiente corporativo completo

👉 Esse tipo de laboratório é padrão em estudos de infraestrutura e redes.
