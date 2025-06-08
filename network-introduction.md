# Componentes, Dispositivos e Diagramas de Rede

Este documento apresenta os principais conceitos, dispositivos e estruturas que compõem uma rede, com foco na comunicação entre dispositivos, tipos de redes e o papel dos diferentes equipamentos. Esta informação é essencial para analistas e profissionais de segurança de redes.

---

## Identificação e Comunicação entre Dispositivos

- Os dispositivos comunicam-se através de **endereços únicos**:
  - **Endereço IP** (identifica o dispositivo na rede)
  - **Endereço MAC** (identifica fisicamente a interface de rede)
- Estes identificadores asseguram que os dados são enviados ao **destinatário correcto**.

---

## Tipos de Rede

### LAN (Local Area Network)
- Rede localizada numa área pequena (ex.: casa, escritório, escola)
- Dispositivos como telemóveis e portáteis conectam-se à **WIFI doméstica**, formando uma LAN
- A LAN conecta-se à Internet através de um **router e modem**

### WAN (Wide Area Network)
- Abrange áreas geográficas amplas (ex.: cidades, países)
- A Internet é um exemplo de uma grande WAN
- Permite comunicação entre redes diferentes, como entre colaboradores de empresas em diferentes países

---

## Dispositivos de Rede

### Hub
- Dispositivo simples que **envia dados para todos os dispositivos** na rede
- Sem filtragem de destino, menos seguro
- Comparável a uma torre de rádio a emitir sinais para todos os receptores

### Switch
- Mais inteligente que um hub
- Envia dados **apenas para o dispositivo de destino**
- Mantém uma **tabela de endereços MAC**
- Melhora o desempenho e a segurança da rede

### Router
- Conecta **múltiplas redes** e direcciona o tráfego baseado no **endereço IP**
- Permite a comunicação entre redes diferentes (ex.: entre uma casa e a Internet)
- Pode incluir funcionalidades de **firewall**

### Modem
- Liga o router à Internet, através do **ISP (fornecedor de serviços de Internet)**
- Converte sinais digitais entre a Internet e a rede local
- É o ponto de entrada da Internet para uma LAN

### Ponto de Acesso Sem Fios (Wireless Access Point)
- Cria redes sem fios (Wi-Fi) usando ondas de rádio
- Permite que dispositivos com adaptadores sem fios se conectem à rede

---

## Outros Componentes de Rede

### Dispositivos do Utilizador
- Computadores, portáteis, smartphones e tablets
- Cada um com endereço IP e MAC únicos
- Ligam-se via **cabos Ethernet** ou **Wi-Fi**

### Firewalls
- Monitorizam e controlam o tráfego de rede, entrada e saída
- Aplicam **regras de segurança definidas pela organização**
- Ficam entre a rede interna e redes externas (ex.: Internet)

### Servidores
- Fornecem serviços e recursos a outros dispositivos (clientes)
- Exemplos:
  - Servidor de ficheiros
  - Servidor de email
  - Servidor DNS

---

## Virtualização de Dispositivos de Rede

- Ferramentas de **virtualização** executam funções de dispositivos físicos (ex.: routers, switches)
- São oferecidas por **fornecedores de serviços em nuvem**
- Permitem **redução de custos** e **escalabilidade**

---

## Diagramas de Rede

- Representam visualmente a **arquitectura e os dispositivos de rede**
- Utilizam **ícones e linhas** para mostrar ligações entre dispositivos
- Auxiliam analistas e administradores a:
  - Compreender a estrutura da rede
  - Identificar vulnerabilidades
  - Planejar defesas contra ameaças
