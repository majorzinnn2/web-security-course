---
layout: default
title: Dia 1 - Introdução
nav_order: 2
---

# Dia 1: Introdução à Segurança Web

Bem-vindo ao primeiro dia do nosso curso de segurança web! Hoje, construiremos a fundação do seu conhecimento, explorando os pilares essenciais da cibersegurança. Começaremos com a Tríade CIA (Confidencialidade, Integridade e Disponibilidade), entenderemos os diferentes tipos de atacantes e mergulharemos no Ciclo de Desenvolvimento Seguro (SDLC). Além disso, vamos desmistificar o que é a OWASP e seu famoso Top 10, e apresentar as metodologias e ferramentas, como o Burp Suite, que serão cruciais para sua jornada prática.

## Segurança cibernética

A segurança cibernética refere-se à prática de proteger sistemas, redes e programas contra ataques digitais. Esses ataques geralmente visam acessar, alterar ou destruir informações confidenciais, extorquir dinheiro dos usuários ou interromper processos comerciais normais. A segurança cibernética é crucial para proteger dados sensíveis, manter a privacidade dos usuários e garantir a integridade dos sistemas.

### Ataques e Atacantes
A maioria dos ataques começa pela exploração de uma falha de software ou erro de configuração que resultou dos esforços honestos de programadores e equipes de TI, que são humanos e, portanto, imperfeitos. 

Entretanto, nem todos os ataques são causados por erros de programação ou falhas de configuração. Alguns são utilizam técnicas de engenharia social para enganar os usuários a fim de obter acesso não autorizado a sistemas ou dados. De qualquer forma, o objetivo final dos atacantes é comprometer a segurança dos sistemas e obter acesso a informações ou recursos que não deveriam estar disponíveis para eles.

Os atacantes podem ser classificados em várias categorias, incluindo:  

- **Hackers Éticos (White Hat)**: Profissionais que usam suas habilidades para identificar e corrigir vulnerabilidades de segurança, ajudando a proteger sistemas contra ataques maliciosos.

![white hat]({{ '/assets/images/white-hat.png' | relative_url }})

- **Hackers Maliciosos (Black Hat)**: Indivíduos que exploram vulnerabilidades para ganho pessoal, causando danos ou roubando informações.

![black hat]({{ '/assets/images/black-hat.png' | relative_url }})

- **Hackers Cinzentos (Gray Hat)**: Pessoas que podem violar a segurança sem permissão, mas não têm intenções maliciosas. Eles podem divulgar vulnerabilidades publicamente ou vendê-las.

![gray hat]({{ '/assets/images/gray-hat.png' | relative_url }})

- **Hacktivistas**: Ativistas que usam suas habilidades de hacking para promover causas políticas ou sociais.

![hacktivista]({{ '/assets/images/hacktivista.png' | relative_url }})

- **Hackers de Estado**: Governos que conduzem operações cibernéticas para espionagem, sabotagem ou guerra cibernética.   

![nacional]({{ '/assets/images/nacional.png' | relative_url }})

### CIA 

![CIA]({{ '/assets/images/cia.png' | relative_url }})

### (Confidencialidade, Integridade e Disponibilidade)
O modelo CIA é um dos pilares da segurança da informação. Ele se concentra em três princípios fundamentais:

![Ilustração da Tríade CIA]({{ '/assets/images/triade-cia.png' | relative_url }})

1. **Confidencialidade**: Garante que a informação seja acessível apenas por pessoas autorizadas. Isso pode ser alcançado através de criptografia, controle de acesso e autenticação.

2. **Integridade**: Assegura que a informação não seja alterada de forma não autorizada. Isso envolve o uso de hashes, assinaturas digitais e controles de versão.

3. **Disponibilidade**: Garante que a informação e os sistemas estejam disponíveis para os usuários autorizados quando necessário. Isso pode incluir redundância, backups e planos de recuperação de desastres.

### OWASP (Open Web Application Security Project) 
Agora que já entendemos os conceitos básicos de segurança cibernética, podemos explorar o OWASP, uma organização sem fins lucrativos dedicada a melhorar a segurança de software. O OWASP é conhecido por seus projetos, ferramentas e recursos que ajudam desenvolvedores e profissionais de segurança a criar aplicações mais seguras.
Os projetos mais conhecidos do OWASP incluem:
- **OWASP Top Ten**: Uma lista das dez principais vulnerabilidades de segurança em aplicações web, atualizada periodicamente. A lista mais recente (2021) inclui:
    1. **Broken Access Control**: Falhas de Controle de Acesso que permitem que usuários não autorizados acessem recursos ou funcionalidades restritas.
    2. **Cryptographic Failures**: Falhas na implementação de criptografia que podem levar à exposição de dados sensíveis.
    3. **Injection**: Falhas que permitem a injeção de código malicioso em aplicações, como SQL Injection e Command Injection.
    4. **Insecure Design**: Falhas de design que comprometem a segurança da aplicação desde o início.
    5. **Security Misconfiguration**: Configurações inadequadas que podem expor a aplicação a riscos de segurança.
    6. **Vulnerable and Outdated Components**: Uso de bibliotecas ou componentes desatualizados com vulnerabilidades conhecidas.
    7. **Identification and Authentication Failures**: Falhas na identificação e autenticação de usuários, como senhas fracas ou falta de autenticação multifator.
    8. **Software and Data Integrity Failures**: Falhas que comprometem a integridade do software e dos dados, como a falta de verificação de integridade.
    9. **Security Logging and Monitoring Failures**: Falhas na implementação de logging e monitoramento de segurança, dificultando a detecção de atividades maliciosas.
    10. **Server-Side Request Forgery (SSRF)**: Vulnerabilidades que permitem que um atacante faça requisições não autorizadas a partir do servidor.

- **OWASP ASVS (Application Security Verification Standard)**: Um framework que fornece um conjunto de requisitos de segurança para aplicações web, ajudando desenvolvedores a garantir que suas aplicações atendam a padrões mínimos de segurança.
- **OWASP ZAP (Zed Attack Proxy)**: Uma ferramenta de teste de segurança de aplicações web que ajuda a identificar vulnerabilidades em aplicações web durante o desenvolvimento e testes.
- **OWASP Cheat Sheets**: Uma coleção de guias práticos que fornecem melhores práticas para desenvolver aplicações seguras.
- **OWASP Dependency-Check**: Uma ferramenta que identifica bibliotecas de terceiros com vulnerabilidades conhecidas em projetos de software.

Segue o site oficial do OWASP: [https://owasp.org/](https://owasp.org/)

### Ciclo de Desenvolvimento Seguro (SDLC - Secure Development Life Cycle)
O Ciclo de Desenvolvimento Seguro (ou Secure Development Lifecycle - SDLC) é uma abordagem para o desenvolvimento de software que integra a segurança em todas as fases do processo, desde o planejamento inicial até o descomissionamento do sistema. O objetivo é construir software mais seguro desde o início, em vez de tentar consertar vulnerabilidades depois que o produto já foi lançado, o que é muito mais caro e arriscado. Quanto mais cedo a segurança for considerada no ciclo de vida do desenvolvimento, menor será o custo e o impacto das vulnerabilidades.

1. **Requisitos de segurança**
    Nesta etapa é realizada a identificação e definição dos requisitos de segurança que o sistema deve atender, com base nas necessidades do negócio e nas ameaças potenciais. O Framework OWASP ASVS ou Microsoft STRIDE podem ser utilizados para ajudar a definir esses requisitos. Sendo que o STRIDE é focado em ameaças e o ASVS em requisitos de segurança.
    A sigla **STRIDE** significa:
    - Spoofing (Falsificação de identidade)
    - Tampering (Violação de dados)
    - Repudiation (Repúdio)
    - Information Disclosure (Divulgação de informações)
    - Denial of Service (Negação de serviço)
    - Elevation of Privilege (Elevação de privilégio)
    
    Cada uma dessas categorias representa um tipo diferente de ameaça que pode afetar a segurança de um sistema. E nós devemos criar um documento que aborde cada uma dessas categorias, identificando as ameaças específicas que podem afetar o sistema e definindo medidas para mitigá-las.

    A sigla **ASVS** significa:
    - Application Security Verification Standard (Padrão de Verificação de Segurança de Aplicações) é um framework desenvolvido pela OWASP que fornece um conjunto de requisitos de segurança para aplicações web. Ele é projetado para ajudar desenvolvedores, arquitetos e testadores a garantir que suas aplicações atendam a padrões mínimos de segurança.
    O ASVS é dividido em três níveis de verificação, cada um com um conjunto crescente de requisitos de segurança:
    - Nível 1: Requisitos básicos de segurança que todas as aplicações devem atender.
    - Nível 2: Requisitos adicionais para aplicações que lidam com dados sensíveis ou que exigem um nível mais alto de segurança.
    - Nível 3: Requisitos avançados para aplicações que lidam com dados altamente sensíveis ou que exigem o mais alto nível de segurança.
    Entretanto, acaba sendo utilizado em um nível mais alto, como um checklist para garantir que a aplicação atenda a todos os requisitos de segurança necessários.

2. **SAST (Static Application Security Testing)**
    As aplicações SAST analisam o código-fonte, bytecode ou binário para identificar vulnerabilidades de segurança sem executar o programa. Elas são eficazes na detecção de problemas como injeção de SQL, XSS (Cross-Site Scripting), buffer overflows e outras falhas comuns de segurança.
    São normalmente integradas ao processo de desenvolvimento, direto no ambiente de desenvolvimento integrado (IDE) ou no pipeline de integração contínua/entrega contínua (CI/CD).
    As ferramentas mais famosas são:
    - Snyk
    - Checkmarx
    - Veracode
    - Fortify
    - Semgrep
    - SonarQube

3. **DAST (Dynamic Application Security Testing)**
    Testes de segurança que são realizados no aplicativo em execução. No contexto de segurança web, o DAST envolve a simulação de ataques externos ao aplicativo para identificar vulnerabilidades que podem ser exploradas por invasores. Ferramentas DAST interagem com a aplicação da mesma forma que um usuário ou atacante faria, enviando solicitações HTTP e analisando as respostas para detectar falhas de segurança. Elas podem ser executadas periodicamente ou como parte do processo de desenvolvimento para garantir que novas vulnerabilidades não sejam introduzidas.
    As ferramentas mais famosas são:
    - OWASP ZAP (Zed Attack Proxy)
    - Burp Suite
    - Aqua security
    - Acunetix
    - Qualys Web Application Scanner

4. **Pentesting (Penetration Testing) ou teste de penetração**
    
    ![LGTV]({{ '/assets/images/lgtv.png' | relative_url }})

    Consiste em simular ataques reais a um sistema para identificar e explorar vulnerabilidades de segurança. O objetivo do pentesting é avaliar a segurança do sistema, identificar pontos fracos e fornecer recomendações para mitigá-los. O pentesting pode ser realizado manualmente por profissionais de segurança ou com o auxílio de ferramentas automatizadas. Existem diferentes tipos de pentesting, incluindo:
    - **Black Box**: O testador não tem conhecimento prévio do sistema.
    - **White Box**: O testador tem conhecimento completo do sistema, incluindo código-fonte e arquitetura.
    - **Gray Box**: O testador tem conhecimento parcial do sistema.

    Ferramentas comuns de pentesting incluem:
    - Burp Suite    
    - Kali Linux
    - Parrot Security OS
    - sqlmap
    - Metasploit
    - Nmap
    - Wireshark

    Testes de intrusão serão o foco principal do nosso curso, onde aprenderemos a identificar e explorar vulnerabilidades em aplicações web.

## Metodologia de Pentesting (PTES, OSSTMM, etc.)

Existem várias metodologias para conduzir testes de penetração, cada uma com seu próprio conjunto de etapas e processos. Algumas das metodologias mais conhecidas incluem:
*   **PTES (Penetration Testing Execution Standard)**: Uma metodologia que define um conjunto de etapas para conduzir testes de penetração, incluindo planejamento, coleta de informações, análise de vulnerabilidades, exploração, pós-exploração e relatório.
*   **OSSTMM (Open Source Security Testing Methodology Manual)**: Uma metodologia que fornece um framework para conduzir testes de segurança em sistemas, redes e aplicações. Ela inclui etapas como planejamento, coleta de informações, análise de vulnerabilidades, exploração e relatório.
*   **NIST SP 800-115**: Um guia publicado pelo Instituto Nacional de Padrões e Tecnologia dos EUA que fornece diretrizes para conduzir testes de penetração e avaliações de segurança.
*   **OWASP Testing Guide**: Um guia publicado pela OWASP que fornece um conjunto de testes para avaliar a segurança de aplicações web. Ele inclui etapas como planejamento, coleta de informações, análise de vulnerabilidades, exploração e relatório.
*  **PCI Penetration Testing Guidance**: Um guia publicado pelo Conselho de Padrões de Segurança da Indústria de Cartões de Pagamento (PCI SSC) que fornece diretrizes para conduzir testes de penetração em sistemas que processam, armazenam ou transmitem dados de cartões de pagamento. Ele inclui etapas como planejamento, coleta de informações, análise de vulnerabilidades, exploração e relatório.

Basicamente todos os seguem uma estrutura semelhante, neste curso seguiremos as seguintes etapas, entretanto, na sua vida profissional, você pode e deve adaptar a metodologia conforme a necessidade do cliente ou do projeto, e consultar as metodologias em questão para entender o melhor de cada uma delas:

* **Preparação**: Esta é uma das etapas mais importantes, pois é nela que é definido o escopo do teste, Regras de Engajamento, Acordos de Confidencialidade, getting out of jail card, cronograma, recursos necessários, stakeholders, etc. Sem uma boa preparação, o teste pode falhar ou não atender às expectativas.
* **Reconhecimento**: Nesta etapa, o testador coleta informações sobre o alvo, como endereços IP, nomes de domínio, tecnologias utilizadas, etc. Isso pode ser feito através de técnicas como varredura de rede, análise de DNS, pesquisa em bancos de dados públicos, etc.
* **Mapeamento**: Nesta etapa, o testador cria um mapa do sistema alvo, identificando os pontos de entrada, serviços em execução, portas abertas, etc. Isso pode ser feito através de técnicas como varredura de portas, análise de serviços, etc.
* **Exploração e Análise**: Nesta etapa, o testador tenta explorar as vulnerabilidades identificadas nas etapas anteriores. Isso pode ser feito através de técnicas como injeção de SQL, XSS, brute force, etc. O objetivo é identificar quais vulnerabilidades podem ser exploradas e quais são os impactos potenciais.
* **Pós-exploração**: Nesta etapa, o testador analisa o sistema após a exploração, buscando informações adicionais, escalando privilégios, etc.
* **Reporte (Relatório)**: Nesta etapa, o testador documenta suas descobertas, incluindo vulnerabilidades identificadas, métodos de exploração, impactos potenciais e recomendações para mitigação. O relatório deve ser claro, conciso e direcionado ao público-alvo, seja ele técnico ou executivo.

## Ferramentas: Burp Suite Community e PortSwigger Web Security Academy
![Burp Suite]({{ '/assets/images/burp.png' | relative_url }})

O Burp Suite é uma plataforma integrada para realizar testes de segurança em aplicações web. Ele oferece uma variedade de ferramentas que ajudam os testadores a identificar e explorar vulnerabilidades em aplicações web. A versão Community é gratuita e oferece funcionalidades básicas. Algumas das principais ferramentas do Burp Suite incluem:

- **Proxy**: Permite interceptar e modificar o tráfego HTTP/S entre o navegador e o servidor web.
- **Repeater**: Permite enviar requisições HTTP/S personalizadas para o servidor e analisar as respostas.
- **Intruder**: Permite automatizar ataques de força bruta e fuzzing para identificar vulnerabilidades.
- **Decoder**: Permite decodificar e codificar dados em vários formatos, como Base64, URL encoding, etc.   
- **Scanner**: Disponível apenas na versão Professional, realiza varreduras automatizadas para identificar vulnerabilidades comuns em aplicações web.

Além do Burp Suite, a PortSwigger oferece a Web Security Academy, uma plataforma de aprendizado online gratuita que oferece uma variedade de laboratórios práticos para aprender sobre segurança web e como usar o Burp Suite. A academia cobre uma ampla gama de tópicos, desde conceitos básicos de segurança web até técnicas avançadas de exploração. Você pode acessar a Web Security Academy em: [https://portswigger.net/web-security](https://portswigger.net/web-security)

Para o nosso curso utilizaremos os laboratórios da Web Security Academy para praticar as técnicas que aprenderemos. Vamos iniciar?

Primeiro vamos instalar o Burp Suite Community, você pode baixar ele no site oficial: [https://portswigger.net/burp/communitydownload](https://portswigger.net/burp/communitydownload)

Em seguida, siga os passos para instalar e configurar o Burp Suite Community no seu sistema operacional.

Neste curso utilizaremos o navegador do proprio Burp Suite, chamado de Burp Browser, que já vem configurado para trabalhar com o Burp Suite. Entretanto, você também pode configurar o seu navegador preferido (como Firefox ou Chrome) para trabalhar com o Burp Suite, caso queira. Você pode seguir os passos descritos na documentação oficial: [https://portswigger.net/burp/documentation/desktop/getting-started/proxy-setup](https://portswigger.net/burp/documentation/desktop/getting-started/proxy-setup) par realizar essa configuração no su browser favorito.