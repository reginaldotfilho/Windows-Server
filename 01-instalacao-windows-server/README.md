# 🧱 Instalação do Windows Server 2022 (VirtualBox)

## 📌 Objetivo

Realizar a instalação do Windows Server 2022 em ambiente virtual para uso em laboratório de Active Directory e serviços de rede.

---

## 🧰 Pré-requisitos

* ISO do Windows Server 2022
* VirtualBox instalado
* Computador com no mínimo:

  * 4GB de RAM disponíveis
  * Suporte à virtualização habilitado

---

## ⚙️ Configuração da Máquina Virtual

Antes da instalação, configurar a VM com os seguintes parâmetros:

* **Memória RAM:** 4 GB
* **Processador:** 4 núcleos
* **Armazenamento:** 50 GB
* **Placas de Rede:** 3 adaptadores (rede interna)

---

## 🚀 Processo de Instalação

1. Iniciar a máquina virtual com a ISO do Windows Server
2. Selecionar idioma e formato de teclado
3. Clicar em **Instalar agora**
4. Escolher a versão:

   * **Windows Server 2022 Datacenter (Desktop Experience)**
5. Aceitar os termos de licença
6. Selecionar:

   * **Instalação personalizada**
7. Escolher o disco de 50GB
8. Prosseguir com a instalação

---

## 🔐 Configuração Inicial

Após a instalação:

1. Definir senha do usuário **Administrator**

   ⚠️ Exemplo utilizado em laboratório:
   `123@senac` (não usar em produção)

---

## 🔧 Instalação dos Drivers do VirtualBox

Para melhor desempenho da VM:

1. No menu da VM:

   * Dispositivos → Inserir imagem de CD dos adicionais para convidado
2. Abrir o **Explorador de Arquivos**
3. Acessar:

   * Este Computador → Unidade do VirtualBox
4. Executar o instalador
5. Reiniciar a máquina virtual

---

## ✅ Resultado Esperado

* Windows Server instalado com interface gráfica
* VM funcionando corretamente
* Drivers do VirtualBox ativos

---

## 📌 Observações

* Sempre utilize a versão com interface gráfica (GUI) para facilitar o aprendizado inicial
* Essa máquina será a base para instalação do Active Directory e demais serviços

---
