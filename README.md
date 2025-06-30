# 💻 Gerenciando Máquinas Virtuais no Azure

Este repositório foi desenvolvido como parte do desafio prático da **Digital Innovation One (DIO)**, com o objetivo de aplicar os conhecimentos adquiridos na trilha de formação **Microsoft AZ-104**, focando no gerenciamento de máquinas virtuais (VMs) dentro do ambiente **Microsoft Azure**.
---

## 📌 Índice
- [Objetivos do Projeto](#🎯-objetivos-do-projeto)
- [Conhecimentos Aplicados](#🧠-conhecimentos-aplicados)
- [Etapas do Laboratório](#🛠️-etapas-do-laboratório)
- [Capturas de Tela](#📸-capturas-de-tela-opcional)
- [Comandos Linux Úteis](#📋-comandos-linux-úteis)
- [Dicas Extras](#💡-dicas-extras)
- [Próximos Passos](#🚀-próximos-passos)
- [Referências](#📚-referências)
- [Conclusão](#✅-conclusão)

---

## 🎯 Objetivos do Projeto

- Criar e configurar uma máquina virtual no Azure via portal web.
- Compreender os principais componentes de infraestrutura em nuvem.
- Estimular a documentação técnica utilizando GitHub.
- Produzir um repositório reusável como base para projetos futuros ou estudos.

---

## 🧠 Conhecimentos Aplicados

| Área de Conhecimento | Tópicos Abordados |
|----------------------|-------------------|
| **Azure**            | Portal Web, Grupos de Recursos, Máquinas Virtuais, Redes Virtuais, NSG |
| **Redes**            | VNet, Subnet, IP Público, Regras de Segurança (NSG) |
| **Segurança**        | Credenciais de acesso, portas RDP/SSH, boas práticas |
| **DevOps/Git**       | Criação de repositório, versionamento de documentação, estrutura de projeto |

---

## 🛠️ Etapas do Laboratório

### 1. 🎯 Criação do Grupo de Recursos
- Nome: `rg-vm-dio-lab`
- Região: Brasil Sul
- Objetivo: Agrupar todos os recursos usados no projeto.

### 2. 🖥️ Criação da Máquina Virtual
- Nome da VM: `vm-dio-lab`
- SO: `Windows Server 2019` ou `Ubuntu Server 20.04`
- Tamanho: `B1s` (baixo custo e uso geral)
- Autenticação: Usuário + Senha
- Disco OS: SSD padrão

### 3. 🌐 Configuração de Rede
- VNet e Subnet criadas automaticamente.
- IP público atribuído à VM.
- Regras no NSG:
  - ✅ Porta **3389** liberada para RDP (Windows)
  - ✅ Porta **22** liberada para SSH (Linux)

### 4. 🔐 Acesso à Máquina
- Acesso realizado pelo **Remote Desktop Connection** ou via terminal com `ssh`.
- Testes realizados:
  - Ping para endereços externos.
  - Instalação de pacotes (Linux).
  - Ativação de funcionalidades administrativas (Windows).

---

## 📋 Comandos Linux Úteis

```bash
# Conectar via SSH
ssh usuario@ip-da-vm

# Atualizar repositórios e pacotes
sudo apt update && sudo apt upgrade -y

# Instalar Apache (exemplo prático)
sudo apt install apache2 -y

# Verificar status do serviço
sudo systemctl status apache2
```

---

## 💡 Dicas Extras

- Use **nomenclaturas padronizadas** para facilitar o gerenciamento no portal.
- Sempre **revise as regras de NSG** para evitar exposição desnecessária.
- Utilize **tags nos recursos** para organização e rastreabilidade.
- Ative o **monitoramento básico da VM** para acompanhar uso de CPU, disco e rede.

---

## 🚀 Próximos Passos

- Automatizar a criação da VM usando **Azure CLI** ou **PowerShell**.
- Estruturar o deployment com **ARM Templates** ou **Bicep**.
- Incluir **monitoramento com Azure Monitor** e alertas.
- Implementar **políticas com Azure Policy** para reforçar a segurança.

---

## 📚 Referências

- [Documentação Oficial do Azure – Gerenciar VMs](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
- [Azure CLI – Microsoft Docs](https://learn.microsoft.com/cli/azure/)
- [Templates ARM – Microsoft Docs](https://learn.microsoft.com/azure/azure-resource-manager/templates/overview)
- [DIO – Trilha de Certificação AZ-104](https://www.dio.me/)
- [Guia Markdown GitHub](https://guides.github.com/features/mastering-markdown/)

---

## ✅ Conclusão

Este projeto demonstrou na prática como provisionar e acessar máquinas virtuais na nuvem com segurança e eficiência. A documentação gerada serve como guia reutilizável tanto para estudos quanto para replicação em ambientes de teste ou produção.

> 💡 *Próximo passo sugerido*: Automatizar o provisionamento de infraestrutura e aplicar políticas de conformidade com Azure Policy.
