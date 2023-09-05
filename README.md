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

### Problema 4

Temos no TJDF alguns Storage Account, e, tanto estes recursos quanto outros recursos no 
Microsoft 365 somente devem ser acessados por equipamentos do TJDF e por conexões que 
são oriundas apenas do BRASIL. Que tipo de solução podemos oferecer e como posso ter 
esta solução em meu ambiente? É Gratuitamente?

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/0dbb390e-8f8a-4df1-94a0-0fe0a5e76a03)

O Acesso Condicional permite que você defina políticas de acesso com base em várias condições, como localização geográfica, estado do dispositivo e autenticação MFA multifator. Você pode configurar uma política para permitir o acesso apenas a partir de locais específicos, neste caso, o Brasil.

Na Autenticação Multifator (MFA), além de restringir o acesso por localização geográfica, você pode adicionar uma camada adicional de segurança exigindo autenticação multifator para garantir que apenas usuários autorizados possam acessar recursos críticos.

Não é Gratuito, mas Essencial: O Acesso Condicional é uma característica do Azure AD Premium, que é uma assinatura paga. Embora não seja gratuito, o investimento em segurança é essencial para proteger os recursos críticos do TJDF contra acessos não autorizados e ameaças cibernéticas.

Licenças Gratuitas: Com uma licença gratuita do Azure AD, você pode configurar políticas de Acesso Condicional simples, como bloquear o acesso de dispositivos não confiáveis ou exigir MFA para determinados usuários.

### Problema 5

Temos algumas aplicações no ambiente no qual precisamos proteger. Além disto, estamos 
em um ambiente muito crítico no qual qualquer vazamento de dados, pode comprometer 
o TJDF de uma maneira muito delicada, por isso precisamos controlar o tráfego de dados 
entre os computadores, monitorando tudo o que sai. O que ofertar nestes cenários? 

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/3e8736df-a2d4-4a1a-9c16-b7c581fdaf7f)

O Purview permite a descoberta e catalogação de todos os dados existentes no ambiente, incluindo dados sensíveis e informações confidenciais.

O Purview oferece controle granular sobre quem pode acessar e interagir com os dados. As permissões podem ser gerenciadas de forma centralizada.

A funcionalidade DLP oferecida pela Microsoft ajuda a evitar vazamentos acidentais ou intencionais de informações confidenciais. Ela monitora o tráfego de dados em tempo real e pode bloquear ou alertar sobre a transferência não autorizada de informações sensíveis.

A solução permite um monitoramento detalhado e abrangente de todas as atividades de dados no ambiente. Isso inclui a capacidade de rastrear e registrar quem acessou, modificou ou compartilhou dados, fornecendo uma trilha de auditoria completa. 

### Problema 6

Precisamos centralizar a coleta de dados de infraestrutura, software recursos, e termos a 
possibilidade de, com base nestes dados coletados, dispararmos processos automatizados 
para tratar alguns casos e/ou anomalias no ambiente. O que podemos utilizar aqui?

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/8cb4857a-d70e-4f98-8c8d-807a464bf2c1)

Azure Firewall e o Network Security Groups (NSG) será utilizado para centralizar a coleta de dados de infraestrutura, software e recursos, além de permitir a automação de processos para tratar casos e anomalias no ambiente de maneira eficaz.

O Azure Firewall pode ser configurado para registrar informações detalhadas sobre o tráfego de rede, incluindo fonte, destino, protocolo e portas. Isso centraliza a coleta de dados de infraestrutura e tráfego de rede em um local único e acessível.

Os registros de tráfego do Azure Firewall podem ser usados para análise posterior, permitindo a identificação de atividades suspeitas ou anomalias na rede.

Os NSGs são conjuntos de regras de segurança que podem ser aplicados a nível de rede e vão controlar o tráfego de entrada e saída para recursos específicos no Azure.

Os NSGs permitem centralizar a definição de regras de segurança que determinam quais tipos de tráfego são permitidos ou bloqueados.

Microsoft Sentinel é responsável pela coleta de dados de diversas fontes para uma visão abrangente da infraestrutura e ameaças. Dispara alertas automatizados e ações de resposta para mitigar ameaças em tempo real.

O Sentinel realiza o monitoramento contínuo e relatórios detalhados para melhor compreensão da postura de segurança.

### Problema 7

O TJDF tomou conhecimento de uma ferramenta da Microsoft chamada Purview, mas eles 
não fazem ideia de como esta ferramenta pode auxiliar em termos de segurança no 
ambiente deles, por isso é importante que você explique os principais recursos existentes e 
de que maneira ele pode ser adotado no ambiente.

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/c25faf95-77f4-4ed0-8bf8-541bb6335e6f)

O Microsoft Purview é uma plataforma de governança de dados que oferece uma série de recursos que podem ser altamente benéficos para melhorar a segurança do ambiente do TJDF (Tribunal de Justiça do Distrito Federal).

O Purview oferece recursos de classificação automatizada de dados com base em políticas predefinidas ou personalizadas. Permite o monitoramento detalhado de quem acessa, modifica ou compartilha dados, fornecendo uma trilha de auditoria completa.

A plataforma é capaz de identificar padrões de uso anômalos que podem indicar atividades suspeitas ou tentativas de violação de segurança.

O Purview permite a definição de políticas de retenção e descarte de dados, isso garante que informações não sejam mantidas indefinidamente e estejam em conformidade com regulamentações.

O Purview se integra perfeitamente com outras soluções Microsoft, como o Microsoft 365 e o Azure, facilitando a implementação e a gestão no ambiente do TJDF.

### Valores do projeto

![image](https://github.com/brunobonatini/Projeto-Seguranca-da-Informacao-EDN/assets/105396325/94f38382-db4d-48c2-ae8a-0026429ca719)








