# Computação em Nuvem e Redes Definidas por Software (SDN)

Este documento resume os principais conceitos sobre redes em nuvem, ambientes híbridos, redes definidas por software (SDN), tipos de serviços em nuvem (SaaS, PaaS, IaaS), e os benefícios operacionais, técnicos e económicos da migração para a nuvem. 

---

## O que é Computação em Nuvem?

- **Computação em nuvem** é o uso de **servidores, aplicações e serviços de rede remotos**, hospedados na internet, em vez de dispositivos físicos locais.
- As empresas acedem a recursos tecnológicos sob demanda, pagando apenas pelo que consomem.

### Rede em Nuvem
- É composta por **servidores e recursos remotos** localizados em datacenters e acessados pela internet.
- Permite que **serviços e aplicações web** sejam usados a partir de qualquer local geográfico.

---

## Comparação: Rede Tradicional vs. Rede em Nuvem

| Característica          | Rede Tradicional                    | Rede em Nuvem                         |
|-------------------------|--------------------------------------|---------------------------------------|
| Localização dos dados   | Em servidores físicos da empresa     | Em datacenters remotos (CSPs)         |
| Escalabilidade          | Limitada ao hardware físico          | Elástica e ajustável sob demanda      |
| Custos iniciais         | Elevados (infraestrutura própria)    | Reduzidos (modelo pay-as-you-go)      |
| Manutenção              | Equipa interna                      | Responsabilidade do fornecedor (CSP)  |

---

## Tipos de Serviço em Nuvem

### Software como Serviço (SaaS)
- O fornecedor gere tudo (infraestrutura, plataforma e aplicação).
- Exemplo: Gmail, Microsoft 365, Salesforce.

### Plataforma como Serviço (PaaS)
- O fornecedor fornece ferramentas e ambiente para **desenvolvimento de aplicações personalizadas**.
- Exemplo: Google App Engine, Heroku.

### Infraestrutura como Serviço (IaaS)
- A empresa configura e gere **servidores virtuais, redes e armazenamento**.
- Exemplo: AWS EC2, Microsoft Azure, Google Compute Engine.

---

## Nuvem Híbrida e Multi-Nuvem

- **Nuvem híbrida**: combinação de infraestrutura local e serviços de nuvem.
- **Multi-nuvem**: uso de múltiplos fornecedores de nuvem (ex.: AWS + Azure).
- Benefícios:
  - Redução de custos
  - Maior controlo sobre dados sensíveis
  - Flexibilidade operacional

---

## Redes Definidas por Software (SDN)

- As SDNs substituem dispositivos físicos por **componentes virtuais** (ex.: switches, routers, firewalls).
- As configurações são feitas **por software**, de forma programática e remota.
- Vantagens:
  - Facilidade de gestão e monitorização
  - Resposta rápida a ameaças
  - Alta eficiência e performance
  - Suporte a virtualização e automação de rede

---

## Benefícios da Computação em Nuvem e SDN

### Escalabilidade
- Recursos ajustáveis conforme a procura
- Permite crescer ou reduzir sem desperdício

### Redução de Custos
- Sem necessidade de grandes investimentos iniciais
- CSPs partilham custos de infraestrutura

### Fiabilidade e Segurança
- Alta disponibilidade e redundância
- Ferramentas de segurança como:
  - Firewalls de Aplicação Web (WAF)
  - Sistemas de Detecção/Prevenção de Intrusão (IDS/IPS)
  - Firewalls L3/L4

---

## Segurança em Redes de Nuvem

- Com o aumento da migração para a nuvem, a **segurança baseada em identidade** tornou-se crucial.
- É necessário verificar **a origem do tráfego e a identidade do utilizador**.
- Segurança na nuvem inclui:
  - Controlo de acessos
  - Monitorização de tráfego
  - Análise de dados e ameaças
  - Conformidade com normas e regulamentos
