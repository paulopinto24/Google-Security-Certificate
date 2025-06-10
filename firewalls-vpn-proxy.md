# Firewalls

Uma firewall é um dispositivo ou aplicação de segurança de rede que monitoriza o tráfego que entra e sai de uma rede. A firewall decide se permite ou bloqueia esse tráfego com base num conjunto de regras de segurança previamente definidas.

## Port Filtering

Filtragem de portas (ou *port filtering*) é uma funcionalidade essencial das firewalls. Consiste em permitir ou bloquear comunicações com base nos números de porta utilizados nas ligações de rede.
Por exemplo, pode ser configurada para permitir apenas a comunicação nas portas:
- 443, usada para HTTPS (comunicação segura na web)
- 25, usada para envio de email

As regras aplicadas na firewall são definidas pela política de segurança da organização.

## Tipos de Firewall

### Firewall de Hardware
- Dispositivo físico que inspeciona todos os pacotes de dados antes de entrarem na rede.
- Considerada uma defesa básica contra ameaças externas.

### Firewall de Software
- Programa instalado num computador ou servidor.
- Analisa o tráfego recebido pelo sistema onde está instalado.
- Mais económica e sem necessidade de hardware dedicado, mas consome recursos do sistema.

### Firewall Baseada na Cloud (Firewall as a Service - FaaS)
- Firewall de software fornecida por um prestador de serviços na cloud.
- A configuração é feita através de uma interface online.
- Protege tanto o tráfego de entrada como recursos da organização armazenados na nuvem.

## Tipos de Operação

### Firewall com Estado (*Stateful*)
- Mantém o contexto das conexões e monitoriza o comportamento do tráfego.
- Consegue identificar padrões suspeitos e impedir ataques em tempo real.
- Mais segura que a firewall sem estado.

### Firewall sem Estado (*Stateless*)
- Opera com base em regras fixas definidas pelo administrador.
- Não guarda histórico nem reconhece padrões de comportamento.
- Menos eficaz contra ataques complexos.

### Next Generation Firewall (NGFW)
- Combina a inspeção com estado com funcionalidades avançadas.
- Realiza inspeção profunda de pacotes (*deep packet inspection*).
- Inclui prevenção de intrusões e integração com serviços de inteligência na cloud.
- Fornece proteção em tempo real contra ameaças emergentes.

# Virtual Private Network (VPN)

Uma VPN (Virtual Private Network) é um serviço de segurança de rede que altera o endereço IP público do utilizador e oculta a sua localização virtual. Isto permite proteger os dados pessoais quando se acede à internet através de redes públicas.

## Encriptação de Dados

A VPN encripta os dados durante a sua transmissão na internet. Esta encriptação assegura que a informação trocada se mantém confidencial e ilegível para terceiros não autorizados.

## Tipos de VPN

### Acesso Remoto
- Ligação segura entre um dispositivo pessoal e um servidor VPN.
- Encripta os dados transmitidos entre o utilizador e os recursos internos.

### Site-to-Site
- Conecta redes geograficamente distintas (ex: filiais).
- Cria túneis encriptados entre redes locais.
- Normalmente usa IPsec.

---

## Protocolos de VPN

| Protocolo     | Descrição                                                                 | Vantagens                                                                 | Limitações                                                                 |
|---------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| WireGuard | Protocolo moderno e open-source, com foco em simplicidade e desempenho.   | - Rápido e eficiente<br>- Código leve<br>- Fácil de configurar            | - Menor histórico de auditoria<br>- Nem todos os sistemas o suportam      |
| IPsec     | Protocolo mais antigo e amplamente suportado por sistemas operativos.     | - Muito testado<br>- Compatibilidade ampla<br>- Fiável                   | - Mais complexo<br>- Pode ter desempenho inferior em certas configurações |

---


## Encapsulamento

A VPN utiliza um processo chamado encapsulamento para proteger os dados sensíveis.

- O encapsulamento envolve os dados privados dentro de outros pacotes de dados.
- Isto permite ocultar informações como o endereço IP e o endereço MAC de origem.
- Ao encapsular, a VPN resolve o problema de encriptação pura: os routers de rede conseguem ler o pacote exterior para encaminhar corretamente os dados, mas o conteúdo interno continua protegido.
- Desta forma, os pedidos da rede podem alcançar os destinos corretos sem comprometer a privacidade.

## Túnel Encriptado

A VPN estabelece um túnel encriptado entre o dispositivo do utilizador e o servidor da VPN.

- Este túnel é protegido com encriptação forte que só pode ser decifrada com uma chave criptográfica.
- Garante que nenhum agente externo consiga aceder aos dados durante a transmissão.

# Security Zones

Zonas de segurança são segmentos de uma rede criados para proteger a rede interna contra acessos externos, como a internet. Fazem parte da técnica de segurança chamada segmentação de rede, que divide a rede em partes separadas, cada uma com permissões de acesso e regras de segurança específicas.

## Funções das Zonas de Segurança

- Controlam quem pode aceder a diferentes partes da rede.
- Servem de barreira para proteger redes internas.
- Mantêm a privacidade entre grupos dentro da organização.
- Ajudam a conter falhas e impedir a sua propagação para o resto da rede.

## Exemplos de Segmentação

- Hotel com Wi-Fi público: uma rede pública separada da rede interna usada pela equipa.
- Universidade: pode haver sub-redes distintas para docentes e estudantes, permitindo isolar problemas que surjam numa dessas sub-redes.

## Tipos de Zonas de Segurança

As redes de uma organização são divididas em dois grandes grupos:

### Zona Não Controlada

- Qualquer rede fora do controlo da organização.
- Exemplo: a internet.

### Zona Controlada

- Sub-redes internas protegidas da zona não controlada.
- Contém diferentes camadas de segurança.

#### Demilitarized Zone (DMZ)

- Camada externa da zona controlada.
- Contém serviços públicos com acesso à internet:
  - Servidores web
  - Servidores proxy
  - Servidores DNS
  - Servidores de email e ficheiros

- Atua como perímetro de segurança entre a internet e a rede interna.

#### Rede Interna

- Contém servidores e dados privados essenciais à organização.
- Acesso controlado e mais protegido do que a DMZ.

#### Zona Restrita

- Localizada dentro da rede interna.
- Contém informação altamente confidencial.
- Acesso apenas a utilizadores com privilégios especiais.

## Estrutura de Segurança

- Idealmente, a DMZ fica entre duas firewalls:
  - Uma filtra o tráfego vindo do exterior.
  - Outra filtra o tráfego que entra na rede interna.
- A zona restrita deve ser protegida por mais uma firewall adicional.
- Estas camadas sucessivas criam várias linhas de defesa contra ataques.

## Controlo de Acessos

- A configuração das firewalls define as políticas de controlo de acesso.
- As equipas de segurança controlam o tráfego que chega à DMZ e à rede interna.
- Exemplo: garantir que apenas tráfego HTTPS pode aceder a servidores web na DMZ.

# Subnetworks

A sub-rede (subnetwork ou subnet) é a subdivisão de uma rede de computadores em grupos lógicos chamados sub-redes. Funciona como uma rede dentro de outra rede, criada com base nos endereços IP e na máscara de sub-rede atribuída aos dispositivos.

Cada sub-rede permite:

- Organização lógica da rede.
- Redução de tráfego desnecessário.
- Melhoria de desempenho.
- Criação de zonas de segurança.

Quando dispositivos da mesma sub-rede comunicam entre si, a comutação local permite que os dados não saiam da sub-rede, o que aumenta a velocidade e eficiência da comunicação.

---

## CIDR (Classless Inter-Domain Routing)

O CIDR é um método moderno que substitui o antigo sistema de endereçamento IP baseado em classes. Ele permite criar sub-redes mais flexíveis e eficientes ao:

- Atribuir máscaras de sub-rede com maior precisão.
- Expandir a disponibilidade de endereços IPv4.
- Reduzir o tamanho das tabelas de roteamento.

### Notação CIDR

Um endereço IP com CIDR inclui um prefixo de rede, utilizando o formato:
```<endereço IPv4>/<prefixo>```
exemplo: 
```198.51.100.0/24```

Este exemplo abrange os endereços de `198.51.100.0` até `198.51.100.255`.

---

## Benefícios da Sub-rede para a Segurança

- Permite isolar segmentos da rede, dificultando a propagação de ameaças.
- Torna possível criar zonas separadas com firewalls, regras de roteamento e isolamento físico.
- Ajuda a usar a largura de banda de forma mais eficiente.
- Melhora o desempenho geral da rede.
- Evita a necessidade de novos blocos IP públicos, utilizando apenas o que já foi atribuído.

# Proxy Servers

Um proxy é um servidor intermediário que processa pedidos feitos por um cliente, reenviando-os para outros servidores. Atua como uma camada entre a internet e a rede interna da organização, ajudando a proteger os sistemas internos.

- O proxy tem um endereço IP público diferente da rede privada.
- Oculta o IP real da rede interna, dificultando ataques externos.
- Pode verificar se os pedidos de conexão são seguros antes de os reenviar.

---

## Funcionalidades de Segurança

- Ocultação de IP: o IP real da rede não é exposto ao exterior.
- Bloqueio de websites: pode impedir o acesso a páginas não permitidas numa organização.
- Filtragem de tráfego: regula o tráfego de entrada e saída com base em regras de segurança.
- Cache: armazena temporariamente dados frequentemente solicitados, o que reduz a necessidade de aceder constantemente aos servidores internos e melhora a segurança.

---

## Tipos de Servidores Proxy

### Proxy Directo (Forward Proxy)
- Atua entre os utilizadores internos e a internet.
- Oculta o IP do utilizador.
- Filtra pedidos de saída antes de permitir o acesso à internet.
- Exemplo: um colaborador envia um pedido para aceder a um site; o proxy verifica e aprova o pedido antes de o encaminhar.

### Proxy Reverso (Reverse Proxy)
- Atua entre a internet e os servidores internos.
- Oculta os IPs dos servidores internos de quem está fora da rede.
- Útil para proteger servidores web com dados sensíveis.
- Filtra e aprova os pedidos vindos do exterior antes de os encaminhar para os servidores da organização.

### Proxy de Email
- Filtra emails antes de estes entrarem nos servidores internos.
- Verifica se o endereço do remetente é legítimo.
- Reduz riscos de ataques de phishing e de spam.
- Permite aplicar múltiplas camadas de filtragem de mensagens sem afetar a infraestrutura principal de email.

---

## Papel na Segurança da Rede

Os proxies ajudam a:
- Filtrar e monitorizar o tráfego (entrada e saída).
- Reduzir a superfície de ataque ao esconder IPs internos.
- Detetar padrões de comportamento suspeito.
- Proteger servidores internos de acesso não autorizado.


