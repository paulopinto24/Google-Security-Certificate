# Comunicação em Redes e Modelos de Protocolos

## Comunicação em Redes e Pacotes de Dados

As redes permitem a comunicação e o partilhamento de recursos entre dispositivos de uma organização. No entanto, essa comunicação expõe vulnerabilidades que podem ser exploradas por agentes maliciosos.

### Pacote de Dados

Um pacote de dados é a unidade básica de informação transmitida numa rede. Cada pacote é composto por:

- **Cabeçalho**: contém informações sobre a origem, o destino (endereços IP e MAC) e o número do protocolo.
- **Corpo**: contém a mensagem ou os dados transmitidos.
- **Rodapé**: indica o fim do pacote.

### Desempenho da Rede

- **Largura de banda**: quantidade de dados transmitidos por segundo.  
  Fórmula: `Largura de banda = Dados transferidos / Tempo (segundos)`
- **Velocidade**: taxa de envio ou receção de pacotes.

Anomalias na largura de banda ou velocidade podem indicar falhas ou ataques.

### Análise de Pacotes (Packet Sniffing)

Técnica usada para capturar e analisar pacotes de dados. Utilizada para:

- Monitorizar o tráfego
- Detetar anomalias
- Investigar incidentes de segurança

---

## Modelo TCP/IP e Portas de Rede

### TCP/IP

O modelo TCP/IP (Transmission Control Protocol / Internet Protocol) é o padrão utilizado para comunicações em redes, nomeadamente na Internet.

#### TCP (Transmission Control Protocol)

- Estabelece ligações entre dispositivos
- Segmenta os dados em pacotes
- Assegura entrega fiável e ordenada
- Gere controlo de erros

#### IP (Internet Protocol)

- Responsável pelo endereçamento e encaminhamento dos pacotes
- Define o IP de origem e destino
- Permite a comunicação entre redes distintas

### Portas de Rede

As portas são pontos lógicos que permitem aos sistemas operativos organizar o tráfego de rede. Cada serviço ou aplicação utiliza uma porta específica. Exemplos:

| Porta | Serviço                         |
|-------|----------------------------------|
| 20    | Transferência de ficheiros (FTP) |
| 25    | Correio eletrónico (SMTP)        |
| 443   | Comunicação segura (HTTPS)       |

---

## Camadas do Modelo TCP/IP

O modelo TCP/IP organiza a comunicação em quatro camadas principais.

### Camada de Acesso à Rede

- Responsável pela transmissão física dos pacotes
- Envolve hardware como cabos, NICs, hubs e switches
- Inclui o protocolo ARP (Address Resolution Protocol) para associar IPs a endereços MAC

### Camada de Internet

- Encaminha os pacotes através de diferentes redes
- Adiciona endereços IP de origem e destino
- Protocolos principais:
  - IP: endereçamento e encaminhamento
  - ICMP: mensagens de erro e diagnóstico (ex.: ping)

### Camada de Transporte

- Gere o envio de dados entre dispositivos
- Permite controlo de fluxo e deteção de erros
- Protocolos:
  - TCP: ligação fiável com controlo de entrega
  - UDP: ligação não fiável, usado para aplicações em tempo real

### Camada de Aplicação

- Responsável pela interação com aplicações e serviços
- Define como os dados devem ser tratados
- Protocolos comuns:
  - HTTP (web)
  - SMTP (email)
  - FTP (ficheiros)
  - DNS (resolução de nomes)
  - SSH (acesso remoto seguro)

---

## Comparação entre o Modelo TCP/IP e o Modelo OSI

O modelo OSI (Open Systems Interconnection) é uma referência teórica com sete camadas, usada frequentemente em contextos de ensino e análise técnica.

### Camadas do Modelo OSI

| Nº  | Nome                | Função Principal                                                  |
|-----|---------------------|-------------------------------------------------------------------|
| 7   | Aplicação           | Interface com o utilizador (ex.: HTTP, SMTP, FTP)                |
| 6   | Apresentação        | Tradução de dados, criptografia e formatação (ex.: SSL, TLS)     |
| 5   | Sessão              | Estabelecimento, gestão e terminação de sessões de comunicação   |
| 4   | Transporte           | Segmentação, controlo de fluxo, fiabilidade (TCP/UDP)           |
| 3   | Rede                | Endereçamento IP e encaminhamento entre redes                    |
| 2   | Enlace de Dados     | Comunicação dentro da mesma rede física, endereços MAC           |
| 1   | Física              | Transmissão física: cabos, sinais, modems, hubs                  |

### Comparação entre os Modelos

| OSI                     | TCP/IP                    |
|-------------------------|---------------------------|
| Camadas 7 a 5           | Camada de Aplicação       |
| Camada 4 (Transporte)   | Camada de Transporte       |
| Camada 3 (Rede)         | Camada de Internet         |
| Camadas 2 e 1           | Camada de Acesso à Rede    |

### Protocolos por Camada

#### Modelo OSI

| Camada           | Protocolos Exemplo                      |
|------------------|------------------------------------------|
| Aplicação (7)     | HTTP, SMTP, FTP, DNS                    |
| Apresentação (6)  | SSL/TLS, codificações                   |
| Sessão (5)        | NetBIOS, RPC                            |
| Transporte (4)    | TCP, UDP                                |
| Rede (3)          | IP, ICMP                                |
| Enlace (2)        | Ethernet, ARP                           |
| Física (1)        | Ethernet, DSL, rádio                    |

#### Modelo TCP/IP

| Camada            | Protocolos Exemplo                      |
|-------------------|------------------------------------------|
| Aplicação          | HTTP, SMTP, DNS, FTP                   |
| Transporte         | TCP, UDP                                |
| Internet           | IP, ICMP                                |
| Acesso à Rede      | Ethernet, ARP                           |

---

## Endereços IP e Endereços MAC

### Endereços IP

Existem dois tipos principais de endereços IP:

- **IPv4 (Internet Protocol version 4)**  
  - Composto por quatro números (1 a 3 dígitos), separados por pontos.  
    Exemplo: `192.168.0.1`
  - Devido à crescente utilização da Internet, o número de endereços IPv4 disponíveis tornou-se limitado.

- **IPv6 (Internet Protocol version 6)**  
  - Composto por 32 caracteres hexadecimais, separados por dois-pontos.  
    Exemplo: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
  - Suporta uma quantidade muito maior de endereços, ideal para a expansão da Internet.

### Endereços IP Públicos vs. Privados

- **Endereço IP Público**  
  - Atribuído pelo fornecedor de acesso à Internet (ISP).
  - Visível na Internet e associado à localização geográfica da rede.
  - Todos os dispositivos de uma rede doméstica ou empresarial partilham o mesmo IP público.

- **Endereço IP Privado**  
  - Usado apenas dentro de redes locais (LAN).
  - Não é acessível diretamente a partir da Internet.
  - Permite que os dispositivos comuniquem entre si de forma interna.

---

### Endereço MAC

O **endereço MAC** (Media Access Control) é um identificador único atribuído a cada interface de rede de um dispositivo. Trata-se de um endereço físico e fixo, usado a nível da camada de enlace de dados.

- Composto por um conjunto de caracteres alfanuméricos.
- Usado para identificar dispositivos numa mesma rede local.
- Exemplo: `00:1A:2B:3C:4D:5E`

#### Tabela de Endereços MAC

- Os **switches** usam tabelas de endereços MAC para encaminhar pacotes aos dispositivos correctos.
- Quando um switch recebe um pacote, lê o endereço MAC de destino e associa-o à porta correta.
- Esta associação é mantida numa **tabela de endereços MAC**, semelhante a uma lista de contactos internos.

