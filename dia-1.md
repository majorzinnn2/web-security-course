---
layout: default
title: Dia 1 - Introdução
nav_order: 2
---

# Dia 1: Introdução à Segurança Web

Neste primeiro dia, vamos cobrir os conceitos fundamentais que formam a base da segurança de aplicações web, desde os princípios teóricos até as ferramentas e metodologias práticas.

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

- **Estados Nacionais**: Governos que conduzem operações cibernéticas para espionagem, sabotagem ou guerra cibernética.   

![nacional]({{ '/assets/images/nacional.png' | relative_url }})

### CIA 

![CIA]({{ '/assets/images/cia.png' | relative_url }})

## (Confidencialidade, Integridade e Disponibilidade)
O modelo CIA é um dos pilares da segurança da informação. Ele se concentra em três princípios fundamentais:

![Ilustração da Tríade CIA]({{ '/assets/images/triade-cia.png' | relative_url }})

1. **Confidencialidade**: Garante que a informação seja acessível apenas por pessoas autorizadas. Isso pode ser alcançado através de criptografia, controle de acesso e autenticação.

2. **Integridade**: Assegura que a informação não seja alterada de forma não autorizada. Isso envolve o uso de hashes, assinaturas digitais e controles de versão.

3. **Disponibilidade**: Garante que a informação e os sistemas estejam disponíveis para os usuários autorizados quando necessário. Isso pode incluir redundância, backups e planos de recuperação de desastres.

## Ciclo de Desenvolvimento Seguro (SDLC - Secure Development Life Cycle)

O Ciclo de Desenvolvimento Seguro (ou Secure Development Lifecycle - SDLC) é uma abordagem para o desenvolvimento de software que integra a segurança em todas as fases do processo, desde o planejamento inicial até o descomissionamento do sistema. O objetivo é construir software mais seguro desde o início, em vez de tentar consertar vulnerabilidades depois que o produto já foi lançado, o que é muito mais caro e arriscado. Quanto mais cedo a segurança for considerada no ciclo de vida do desenvolvimento, menor será o custo e o impacto das vulnerabilidades.

1. **Requisitos de segurança**
    Identificação e definição dos requisitos de segurança que o sistema deve atender, com base nas necessidades do negócio e nas ameaças potenciais. O Framework OWASP ASVS ou Microsoft STRIDE podem ser utilizados para ajudar a definir esses requisitos. Sendo que o STRIDE é focado em ameaças e o ASVS em requisitos de segurança.
    A sigla **STRIDE** significa:
    - Spoofing (Falsificação de identidade)
    - Tampering (Violação de dados)
    - Repudiation (Repúdio)
    - Information Disclosure (Divulgação de informações)
    - Denial of Service (Negação de serviço)
    - Elevation of Privilege (Elevação de privilégio)
    A ideia é que cada uma dessas categorias representa um tipo diferente de ameaça que pode afetar a segurança de um sistema. E nós devemos criar um documento que aborde cada uma dessas categorias, identificando as ameaças específicas que podem afetar o sistema e definindo medidas para mitigá-las.

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

4. **Pentesting (Penetration Testing)**
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

2.  **OWASP (Open Web Application Security Project)**
    *   *Espaço para desenvolver o conteúdo...*

4.  **Metodologia de Pentesting (PTES, OSSTMM, etc.)**
    *   4.1. Preparação
    *   4.2. Reconhecimento
    *   4.3. Mapeamento
    *   4.4. Exploração e Análise
    *   4.5. Pós-exploração
    *   4.6. Reporte (Relatório)

5.  **Ferramentas: Burp Suite Community e PortSwigger Web Security Academy**
    *   *Espaço para desenvolver o conteúdo sobre a instalação e primeiros passos.*
