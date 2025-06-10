# Protocolos de Rede

Os protocolos de rede são conjuntos de regras que definem como os dados são estruturados, transmitidos e tratados numa rede. Funcionam como uma linguagem comum entre dispositivos e são fundamentais para a comunicação digital.

---

## Tipos de Protocolos

Os protocolos podem ser agrupados em três categorias principais:

- **Protocolos de Comunicação**
- **Protocolos de Gestão**
- **Protocolos de Segurança**

Além disso, existem protocolos específicos para **email**, **acesso remoto** e **tradução de endereços**.

---

## Protocolos de Comunicação

Regulam a troca de dados entre dispositivos, definem o formato da informação e a forma como é enviada e recebida.

| Protocolo | Função | Porta(s) |
|----------|--------|----------|
| **TCP** | Comunicação fiável com verificação (handshake) | Varia conforme o serviço |
| **UDP** | Comunicação rápida sem garantia de entrega | Varia conforme o serviço |
| **HTTP** | Comunicação entre cliente e servidor web | TCP 80 |
| **HTTPS** | Versão segura do HTTP com SSL/TLS | TCP 443 |
| **DNS** | Tradução de nomes de domínio para IP | UDP 53 / TCP 53 |

---

## Protocolos de Gestão

Gerem e monitorizam dispositivos e tráfego na rede.

| Protocolo | Função | Porta(s) |
|----------|--------|----------|
| **SNMP** | Monitorização e gestão de dispositivos | UDP 161 (requis.) / UDP 162 (traps) |
| **ICMP** | Diagnóstico e relatórios de erro (ex.: ping) | Não usa portas |
| **DHCP** | Atribuição automática de IP e configuração | UDP 67 (servidor) / UDP 68 (cliente) |

---

## Protocolos de Segurança

Asseguram a confidencialidade e integridade da informação transmitida.

| Protocolo | Função | Porta(s) |
|----------|--------|----------|
| **HTTPS** | Comunicação segura via SSL/TLS | TCP 443 |
| **SFTP** | Transferência de ficheiros encriptada via SSH | TCP 22 |
| **SSH** | Acesso remoto seguro | TCP 22 |
| **Telnet** | Acesso remoto não encriptado | TCP 23 |

---

## Protocolos de Email

Responsáveis pela receção, envio e sincronização de mensagens eletrónicas.

| Protocolo | Função | Porta(s) |
|----------|--------|----------|
| **POP3** | Transferência de emails para armazenamento local | TCP 110 / TCP 995 (SSL/TLS) |
| **IMAP** | Acesso e sincronização de emails em vários dispositivos | TCP 143 / TCP 993 (TLS) |
| **SMTP** | Envio de emails | TCP 25 / TCP 587 (TLS) |

---

## Outros Protocolos

| Protocolo | Função | Porta(s) |
|----------|--------|----------|
| **ARP** | Mapeamento de IP para MAC | Não usa portas |
| **NAT** | Tradução de IP privado para público | Atua na camada de rede/transporte |
| **FTP/SFTP** | Transferência de ficheiros (SFTP é seguro) | FTP: TCP 20/21, SFTP: TCP 22 |

---

## Endereços IP

Dispositivos numa rede utilizam endereços IP para comunicar, que podem ser **privados** ou **públicos**.

### Endereços Privados

- Usados em redes internas
- Atribuídos por routers
- Intervalos:
  - `10.0.0.0 – 10.255.255.255`
  - `172.16.0.0 – 172.31.255.255`
  - `192.168.0.0 – 192.168.255.255`

### Endereços Públicos

- Atribuídos por ISPs ou IANA
- Visíveis na Internet
- Intervalos típicos:
  - `1.0.0.0 – 9.255.255.255`
  - `11.0.0.0 – 126.255.255.255`

### NAT

- Traduz IPs privados para um IP público comum
- Essencial para comunicação com a Internet
- Executado por routers/firewalls

---

# Tecnologias Wi-Fi e Protocolos de Segurança

## IEEE 802.11 (Wi-Fi)

- Conjunto de padrões que definem comunicações para LANs sem fios
- Criado pelo IEEE (Institute of Electrical and Electronics Engineers)
- O termo "Wi-Fi" é utilizado comercialmente

---

## Evolução dos Protocolos de Segurança Sem Fios

| Protocolo | Ano | Características |
|----------|-----|-----------------|
| **WEP** | 1999 | Primeira tentativa de segurança. Vulnerável e obsoleto |
| **WPA** | 2003 | Introduz TKIP e verificação de integridade da mensagem |
| **WPA2** | 2004 | Introduz AES e protocolo CCMP, padrão atual em muitas redes |
| **WPA3** | 2018 | Criptografia mais forte, proteção contra ataques KRACK, utiliza SAE |

---

## Modos WPA2 e WPA3

### Modo Pessoal

- Ideal para redes domésticas
- Usa uma frase secreta global
- Configuração simples

### Modo Empresarial

- Usado em ambientes organizacionais
- Gestão centralizada de acessos
- Maior controlo e segurança
