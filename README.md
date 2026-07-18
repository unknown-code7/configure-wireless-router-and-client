# 🏠 Configure a Wireless Router and Client

> **Cisco Packet Tracer Lab**
>
> **Autor:** Jordão Paulo  
> **Categoria:** Redes de Computadores • Cisco Packet Tracer • Cisco Networking Academy (NetAcad)  
> **Nível:** Iniciante

---

# 📖 Descrição

Este laboratório simula a implementação de uma **rede doméstica (Home Network)** utilizando o **Cisco Packet Tracer**, permitindo compreender como diferentes dispositivos compartilham a mesma infraestrutura de rede por meio de um **Wireless Router**.

A residência recebe o sinal do provedor de Internet através de um **Cable Splitter**, responsável por dividir o sinal coaxial em duas saídas: uma destinada ao **Cable Modem**, que fornece acesso à Internet ao roteador, e outra destinada à **Smart TV**, permitindo a recepção do sinal de televisão via cabo coaxial.

Após receber a conexão do Cable Modem, o **Wireless Router** distribui a conectividade para todos os dispositivos da rede local, tanto por conexões cabeadas quanto sem fio.

Além da rede doméstica, o cenário também inclui um **Servidor Web Externo**, responsável por hospedar o website **https://skillsforall.srv**, permitindo validar a conectividade entre a rede local e um serviço Web localizado na Internet.

Durante este laboratório serão abordados conceitos fundamentais de Redes de Computadores, como configuração de redes sem fio, DHCP, endereçamento IPv4, conectividade, acesso a serviços Web e testes de comunicação.

---

# 🎯 Objetivos

Ao concluir este laboratório, o estudante será capaz de:

- Configurar um Wireless Router;
- Configurar uma rede Wireless (Wi-Fi);
- Compreender o funcionamento do DHCP;
- Configurar clientes da rede;
- Validar a comunicação entre dispositivos;
- Testar o acesso a um servidor Web externo;
- Entender a arquitetura de uma rede doméstica.

---

# 🏡 Arquitetura da Rede

```mermaid
flowchart TD

    Internet((🌐 Internet))

    Web["🌍 Servidor Web Externo<br/>https://skillsforall.srv"]

    Splitter["📡 Cable Splitter"]

    Modem["📶 Cable Modem"]

    TV["📺 Smart TV"]

    Router["📡 Wireless Router<br/>DHCP • NAT • WLAN"]

    Sala["🛋️ Sala<br/>📺 Smart TV<br/>💻 Laptop"]

    Quarto["🛏️ Quarto<br/>🖥️ Desktop PC"]

    Escritorio["🖥️ Escritório<br/>🖥️ Desktop PC<br/>💻 Laptop"]

    Internet --> Web
    Internet --> Splitter

    Splitter --> Modem
    Splitter --> TV

    Modem --> Router

    Router --> Sala
    Router --> Quarto
    Router --> Escritorio

    classDef internet fill:#FFF8DC,stroke:#F39C12,stroke-width:2px,color:#000000,font-weight:bold;
    classDef infra fill:#E3F2FD,stroke:#1565C0,stroke-width:2px,color:#000000,font-weight:bold;
    classDef clientes fill:#E8F5E9,stroke:#2E7D32,stroke-width:2px,color:#000000,font-weight:bold;

    class Internet,Web internet;
    class Splitter,Modem,Router infra;
    class Sala,Quarto,Escritorio,TV clientes;
---

# 🏠 Estrutura do Laboratório

## 🛋️ Sala (Living Room)

**Equipamentos:**

- Smart TV
- Laptop

---

## 🛏️ Quarto (Bedroom)

**Equipamentos:**

- Desktop PC

---

## 🖥️ Escritório (Home Office)

### Infraestrutura de Rede

- Cable Splitter
- Cable Modem
- Wireless Router

### Dispositivos

- Desktop PC
- Laptop

---

## 🌐 Infraestrutura Externa

### Internet

- Servidor Web Externo
  - Website: **https://skillsforall.srv**

---

# 📦 Inventário de Equipamentos

| Equipamento | Quantidade | Função |
|-------------|-----------:|--------|
| Cable Splitter | 1 | Divide o sinal coaxial entre o Cable Modem e a Smart TV |
| Cable Modem | 1 | Converte o sinal coaxial em Ethernet para acesso à Internet |
| Wireless Router | 1 | Gateway da rede, NAT, DHCP e Access Point |
| Desktop PC | 2 | Clientes da rede |
| Laptop | 2 | Clientes da rede |
| Smart TV | 1 | Recebe sinal coaxial e integra-se à rede local |
| Servidor Web Externo | 1 | Hospeda o website **https://skillsforall.srv** |

---

# 🌐 Tecnologias Utilizadas

- Cisco Packet Tracer
- IPv4
- Ethernet
- Cabo Coaxial
- IEEE 802.11 (Wi-Fi)
- DHCP
- NAT
- HTTP
- DNS
- Wireless LAN (WLAN)

---

# ⚙️ Configurações Realizadas

Durante este laboratório serão realizadas as seguintes atividades:

- Configuração do Wireless Router;
- Configuração do SSID (Nome da Rede);
- Configuração da senha da rede Wi-Fi;
- Configuração do serviço DHCP;
- Associação dos dispositivos à rede;
- Obtenção automática de endereços IP;
- Testes de conectividade entre os dispositivos;
- Teste de acesso ao servidor Web **https://skillsforall.srv**.

---

# 🔄 Fluxo do Laboratório

```mermaid
flowchart LR

    A[🌐 Internet]
    B[📡 Cable Splitter]
    C[📶 Cable Modem]
    D[📡 Wireless Router]
    E[🖥️ Desktop PCs]
    F[💻 Laptops]
    G[📺 Smart TV]
    H[🌍 Servidor Web<br/>skillsforall.srv]

    A --> B
    B --> C
    B --> G
    C --> D
    D --> E
    D --> F
    D --> H
```

---

# 🧪 Testes Realizados

Após a configuração, recomenda-se validar:

- ✅ Comunicação entre os Desktop PCs;
- ✅ Comunicação entre os Laptops;
- ✅ Conectividade da Smart TV;
- ✅ Recebimento automático de endereços IP via DHCP;
- ✅ Comunicação com o Gateway;
- ✅ Acesso ao website **https://skillsforall.srv**;
- ✅ Comunicação entre todos os dispositivos da LAN.

---

# 📚 Conceitos Abordados

- Redes Domésticas
- Topologias de Rede
- Cabo Coaxial
- Ethernet
- Wireless LAN (WLAN)
- DHCP
- Gateway Padrão
- NAT
- DNS
- HTTP
- IPv4
- Wireless Router
- Cisco Packet Tracer

---

# 📌 Pré-requisitos

- Cisco Packet Tracer instalado;
- Conhecimentos básicos de Redes de Computadores;
- Conceitos básicos de IPv4;
- Noções de redes Wireless.

---

# 🎓 Competências Desenvolvidas

Ao concluir este laboratório, o estudante desenvolverá competências em:

- Configuração de Roteadores Wireless;
- Administração de Redes Domésticas;
- Configuração de Clientes de Rede;
- Testes de conectividade;
- Acesso a serviços Web;
- Simulação de Redes Cisco;
- Diagnóstico de Problemas de Conectividade.

---

# ✅ Resultado Esperado

Ao final do laboratório, o **Cable Splitter** deverá distribuir corretamente o sinal coaxial para o **Cable Modem** e para a **Smart TV**. O **Cable Modem** fornecerá acesso à Internet ao **Wireless Router**, que distribuirá endereços IP automaticamente via DHCP para os dispositivos da rede local. Todos os clientes deverão comunicar-se corretamente entre si, acessar a Internet e conseguir abrir o website **https://skillsforall.srv** hospedado no servidor Web externo.

---

# 👨‍💻 Autor

**Jordão Paulo**

**Analista de Cibersegurança** • **Analista de Redes** • **Infraestrutura de TI**

Criador da série **Laboratórios Cisco NetAcad**, dedicada ao ensino prático de Redes de Computadores, Infraestrutura de TI e Cibersegurança utilizando o Cisco Packet Tracer.

---

© 2026 Jordão Paulo. Todos os direitos reservados.
