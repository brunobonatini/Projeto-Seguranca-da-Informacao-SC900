# Projeto - Segurança da Informacao EDN - Microsoft Azure SC900

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/0bfc469b-8328-439c-a705-6693ae1cc945)

## Problema

Sua consultoria está sendo contratada pelo Tribunal de Justiça do Distrito Federal, pois 
ao buscar a ISO 27001, eles perceberam alguns pontos de melhorias no tange Segurança da 
Informação, mas não possuem expertise no Azure e Microsoft 365 para aplicar estas melhorias.
Abaixo listaremos alguns destes pontos de melhorias, e sua função como consultor será 
prover a melhor solução com base em tudo o que você estudou e ainda estudará. O Objetivo é 
que você oferte produtos que atenderão as necessidades e principalmente, explique o motivo 
da escolha e como aquele produto funciona e atenderá as demandas do TJ do Distrito Federal. 

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/be5ef720-65fa-4b20-a7ee-700e7731afbf)

### Problema 1

O TJ possui 267 estações de trabalho em seu ambiente, e não existe uma solução padrão de 
antivírus instalada nestes equipamentos, pois antes do processo de auditoria para ISO, cada 
usuário tinha acesso Admin em seu computador e instalava o que queria. Pensando na 
proteção dos equipamentos e no avanço do processo de certificação ISO 27001, o que você 
sugere para melhorar a segurança neste ambiente?

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/199628be-7c97-40af-b247-a692d9c1bfc3)

O Microsoft Defender for Endpoint oferece detecção proativa e em tempo real de ameaças, identificando e bloqueando ataques de malware, ransomware, phishing e outras ameaças cibernéticas antes que possam causar danos. Isso garantirá uma camada eficaz de proteção para todas as estações de trabalho.

A solução permite o controle de dispositivos e aplicativos em todas as estações, ajudando a evitar a execução de software não autorizado ou perigoso. Isso é muito importante em um ambiente onde os usuários tinham acesso Admin e podiam instalar softwares sem restrições. 
O Defender for Endpoint pode ajudar a reduzir os privilégios administrativos concedidos aos usuários, seguindo as melhores práticas de segurança. A ferramenta realiza análises de vulnerabilidades nas estações para identificar e remediar potenciais pontos fracos no sistema.

O Microsoft Defender for Endpoint se integra perfeitamente com outros produtos Microsoft, como o Microsoft Intune (que pode ser usado para gerenciamento de dispositivos móveis), criando um ambiente de segurança bastante eficaz.

### Problema 2

Além das 267 estações de trabalho, o TJDF possui 29 iPads que são utilizados por Juízes
durante as audiências. Estes iPads não estão ingressados no intune, mas eles são utilizados 
para acessar o Sharepoint do TJDF, o OneDrive, Teams e Contas de E-mail do ambiente, sem 
mesmo ter algum recurso de segurança para isto. O que podemos sugerir para este cenário?

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/e1ea8a46-ef75-4660-b35a-7aeee610650f)

O Microsoft Intune é um serviço de gerenciamento de mobilidade empresarial (EMM) baseado na nuvem que faz parte do conjunto de soluções de produtividade e segurança da Microsoft. Ele foi projetado para ajudar as organizações a gerenciar dispositivos móveis, aplicativos e configurações de segurança de forma centralizada.

O Intune permite que você gerencie todos os dispositivos, incluindo iPads, de forma centralizada por meio de uma única interface baseada na nuvem.

Com o Intune, você pode aplicar políticas de segurança consistentes em todos os iPads. Isso inclui requisitos de senha, criptografia de dados, restrições de aplicativos e configurações de rede, garantindo que os dispositivos estejam em conformidade com os padrões de segurança da organização.

O Intune oferece recursos para rastrear e localizar dispositivos perdidos ou roubados e tomar medidas remotas, como bloquear ou apagar dados confidenciais, caso seja necessário.

O Azure AD faz a restrição do acesso aos recursos somente para dispositivos e conexões confiáveis.
Faz também a proteção contra acesso não autorizado e ameaças cibernéticas, minimizando riscos.

### Problema 3

O TJDF está no projeto de digitalização de todo os seus processos, com isto, será necessário 
pensar em uma solução que atenda aos seguintes requisitos:

A. Um tipo de armazenamento que onde possamos guardar aproximadamente 47TB de 
dados processuais com margem para um futuro crescimento.

B. Por compliance, os dados não podem sair do Brasil. 

C. Que os dados possuam criptografia, mesmo quando estão em repouso.

D. Que processos com mais de 180 dias pós julgados sejam arquivados automaticamente, 
qual camada de armazenamento utilizar?

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/67d4bbb5-1177-4c38-acc1-997e5557b30a)

O Armazenamento no Azure é altamente escalável, permitindo que você aumente ou diminua a capacidade de armazenamento conforme necessário. Isso é importante para acomodar os aproximadamente 47TB de dados processuais e para garantir espaço para futuros crescimentos.

O Armazenamento no Azure oferece criptografia automática em repouso, o que significa que seus dados processuais estarão protegidos mesmo quando estiverem armazenados. A criptografia é uma medida fundamental para a segurança dos dados.

A camada de Armazenamento de Blob "Archive" no Azure é adequada para armazenamento de longo prazo e é otimizada para dados raramente acessados. Ela oferece custos mais baixos em comparação com outras camadas, tornando-a ideal para arquivamento de processos judiciais.
