# Escola_de_TI V.1
Repositório da Escola de TI

# Primeiro Projeto – Arquitetura MVC

## 1. Criação do Projeto
- Criar um **repositório** em uma ferramenta de versionamento, como **GitHub**. ✔
- Criar um **README** para documentar as **decisões do projeto**, incluindo justificativas e escolhas arquiteturais. ✔

---

## 2. Definição do Produto

- **Aplicação web**
- Talvez **Aplicativo mobile**


### 2.1 Objetivo
Nosso objetivo é intermediar o processo entre o locador e o locatário, focando em uma experiência personalizada e além disso propor outros serviços, afim de facilitar a vida dos nossos usuários.

Queremos reunir esses espaços de eventos em uma aplicação Web, fornecendo filtros de busca para ajudar a encontrar o lugar perfeito para você. 

### 2.2 Público-alvo
- Cliente Tipo 1 (Pessoa que quer alugar um espaço de eventos; Locatário)
- Cliente Tipo 2 (Pessoa que tem um local para alugar; Locador)

### 2.3 Contexto de uso
Quando alguem quiser organizar um evento, festa ou churrasco em familia.

---

## 3. Requisitos do Sistema
Os **requisitos funcionais e não funcionais**, detalhadamente:
- **Funcionalidades principais** do produto, como:

**1. Requisitos Funcionais**
  
1.1 Gerenciamento de Usuários
- Criar perfis de usuário (Locador e Locatário)
- Cadastro e edição de informações do usuário
- Autenticação e login utilizando Firebase Authentication
- Recuperação de senha via Firebase (envio de e-mail de redefinição)
- Sistema de avaliação de usuários e locais (avaliação por estrelas e comentários)
- Logout seguro para encerrar a sessão do usuário

1.2 Tela de Login com Firebase
- Login via email e senha utilizando Firebase Authentication
- Opção de login social (Google e Facebook) via Firebase
- Validação de credenciais em tempo real
- Exibição de mensagens de erro em caso de falha na autenticação
- Redirecionamento automático após login bem-sucedido
- Botão de "Esqueci minha senha" com envio de e-mail de redefinição pelo Firebase

1.3 Gerenciamento de Locais
- Cadastro de locais para locação pelo Locador, incluindo:
- Nome do local
- Endereço com integração ao Google Maps
- Capacidade máxima de pessoas
- Regras e restrições do local
- Upload de imagens do espaço
- Valor por hora, diária ou evento
- Disponibilidade de datas e horários
- Edição e exclusão de locais cadastrados
- Visualização detalhada do local pelo Locatário

1.4 Pesquisa e Filtros
- Barra de pesquisa para encontrar locais por nome e região
Filtros por:
- Localização (cidade e bairro)
- Capacidade mínima e máxima
- Preço por período
- Tipo de evento suportado
- Exibição de resultados organizados em lista e mapa

1.5 Reserva de Espaços
- Solicitação de reserva por parte do Locatário
- Aprovação ou recusa da reserva pelo Locador
- Notificação sobre o status da reserva
- Consulta de histórico de reservas para ambos os usuários

1.6 Contato com o Locador
- Botão de contato que redireciona diretamente para o WhatsApp do dono do estabelecimento.

**2. Requisitos não funcionais**, como:
- **Desempenho** (tempo de resposta, escalabilidade)
- **Segurança** (mecanismos de autenticação e autorização)
- **Usabilidade** (design intuitivo e acessibilidade)
- **Manutenibilidade** (facilidade de atualização e suporte)

2.1 Desempenho e Escalabilidade
- O sistema deve ser capaz de suportar múltiplos acessos simultâneos
- Resposta rápida para pesquisa e carregamento de imagens. 

2.2 Segurança
- Autenticação segura via Firebase Authentication
- Controle de permissões para acesso a recursos
- Armazenamento seguro de dados

2.3 Usabilidade
- Interface intuitiva e responsiva
- Design adaptado para web e mobile
- Processo de reserva simples e eficiente

2.4 Manutenção e Evolução
- Utilização de Firebase para login, banco de dados e armazenamento de imagens

---

## 4. Restrições e Condições
  
### Tecnologias
- NestJs
- React
- Swagger
- Javascript
- React Native
- Docker
- Git
- MongoDB ou Postgres

### Ferramentas
- Github
- Trello
- Clockify
- Formulários do Google
- Google Drive
- Discord
- Inteligencias Artificiais

### Restrições Técnicas

Obs: **Restrições Técnicas:**  linguagens de programação e frameworks disponíveis.

### Restrições Não Técnicas
- Não temos total conhecimento em React
- Não temos total conhecimento em React Native
- Não temos total conhecimento em Docker

Obs: **Restrições Não Técnicas:** Orçamento, prazos de entrega, requisitos legais e regulatórios, nossa falta de conhecimento.

## 5. Necessidades dos Stakeholders
Considerar clientes, usuários finais, gerentes de projeto e desenvolvedores.

Necessidades do Locatário até o momento:
- Nenhuma

Necessidades do Locador até o momento:
- Manutenção do local

Necessidades do Gerente do projeto:
- Nenhuma

Necessidades dos Desenvolvedores:
- Nenhuma

## 6. Tendências Tecnológicas
Exploração de novas linguagens, frameworks, plataformas em nuvem e metodologias ágeis.

## 7. Riscos do Projeto
Avaliação de riscos técnicos, operacionais e de negócios.

### 7.1. Riscos Técnicos
- Desenvolvimento e Escalabilidade da Plataforma:
Há o risco de a aplicação apresentar bugs ou falhas que prejudiquem a experiência do usuário, especialmente em momentos de alta demanda.
Mitigação: Investir em testes contínuos, revisões de código e arquiteturas que suportem crescimento.

- Segurança e Proteção de Dados:
Sendo uma plataforma que lida com informações pessoais e transações financeiras (como pagamento de anúncios e taxas), há risco de ataques cibernéticos ou vazamentos de dados.
Mitigação: Implementar protocolos de segurança robustos, criptografia de dados e auditorias regulares.

- Integração com Sistemas Terceirizados:
A proposta envolve a conexão com serviços de validação de ambientes e possivelmente integrações com parceiros para serviços como limpeza, catering ou locação. Problemas na integração podem gerar falhas operacionais.
Mitigação: Realizar testes de integração rigorosos e estabelecer contratos claros com parceiros, definindo SLAs e pontos de controle.

- Manutenção e Atualizações:
A necessidade de atualizações frequentes para corrigir bugs, melhorar funcionalidades ou integrar novas tecnologias pode ocasionar períodos de instabilidade e interrupções no serviço.
Mitigação: Planejar janelas de manutenção e investir em processos de deploy contínuo que minimizem o impacto nos usuários.

- Integração com APIs e Terceiros:
A integração com APIs externas (para validações, pagamentos ou serviços complementares) pode apresentar problemas de compatibilidade, instabilidade ou alterações inesperadas nos endpoints.
Mitigação: Estabelecer contratos de nível de serviço (SLAs) e monitorar continuamente as integrações para agir rapidamente em caso de falhas.

- Dependência da Infraestrutura de Hospedagem:
Problemas com o provedor de serviços de nuvem ou infraestrutura podem causar lentidão ou indisponibilidade do sistema, afetando a experiência do usuário.
Mitigação: Utilizar estratégias de redundância, balanceamento de carga e monitoramento constante da infraestrutura.

### 7.2. Riscos Operacionais
- Gestão dos Parceiros e Qualidade dos Serviços:
O sucesso da plataforma depende da qualidade dos ambientes anunciados e dos serviços terceirizados (como limpeza e cozinha/churrasco). Caso esses parceiros não entreguem conforme o esperado, a reputação do aplicativo pode ser comprometida.
Mitigação: Desenvolver critérios rigorosos de validação (como mencionado na seção "6. Validações e Responsabilidades") e manter um sistema de avaliação e feedback dos clientes.

- Suporte ao Cliente e Logística:
Problemas na organização do atendimento, na gestão dos agendamentos e na resolução de imprevistos podem afetar a experiência do usuário e a eficiência operacional.
Mitigação: Implementar um sistema de atendimento eficiente e investir em treinamento da equipe de suporte, além de utilizar ferramentas de gestão operacional.

- Adoção e Engajamento dos Usuários:
Caso a plataforma não consiga atrair tanto anunciantes quanto clientes finais, pode haver baixa adesão e dificuldades para manter um fluxo constante de transações.
Mitigação: Planejar estratégias de marketing digital, promover uma boa experiência do usuário (UX/UI) e ajustar funcionalidades conforme o feedback do mercado.

- Problemas de Logística e Agendamento:
A coordenação entre disponibilidade de espaços, horários e serviços terceirizados pode gerar conflitos, cancelamentos ou sobreposições de agendamentos.
Mitigação: Investir em um sistema robusto de gestão de reservas e comunicação integrada entre todas as partes envolvidas.

- Capacitação e Retenção da Equipe:
A baixa qualificação ou alta rotatividade dos colaboradores pode impactar a eficiência do suporte, atendimento e validação dos ambientes e parceiros.
Mitigação: Promover treinamentos contínuos e criar políticas de retenção que valorizem a equipe.

- Comunicação Ineficiente:
Falhas na comunicação interna ou com parceiros podem levar a mal-entendidos, erros operacionais e experiências negativas para os usuários.
Mitigação: Estruturar processos claros de comunicação e utilizar ferramentas que centralizem informações e permitam um acompanhamento eficaz.

### 7.3. Riscos de Negócios
- Concorrência com Plataformas Consolidadas:
Dado que concorrentes como o Airbnb já têm presença significativa, o projeto pode enfrentar barreiras para ganhar visibilidade e confiança dos usuários.
Mitigação: Evidenciar os diferenciais competitivos, como a oferta de serviços complementares (ex.: limpeza pós-evento, suporte para planejamento) e focar em nichos de mercado que possam estar menos atendidos.

- Viabilidade Financeira:
Investimentos em tecnologia, marketing e parcerias podem exigir um fluxo de caixa robusto antes que a plataforma se torne rentável.
Mitigação: Elaborar um planejamento financeiro detalhado, com projeções de receitas e custos, e diversificar as fontes de monetização (como taxas, publicidade e parcerias).

- Mudanças no Comportamento do Consumidor e no Mercado de Eventos:
Tendências de mercado, sazonalidades e mudanças nas preferências dos consumidores podem impactar a demanda pelos serviços oferecidos.
Mitigação: Manter um monitoramento contínuo do mercado e adaptar o modelo de negócio conforme as mudanças, investindo também em pesquisas de satisfação dos clientes.

- Variações no Mercado e Sazonalidade:
A demanda por espaços e serviços para eventos pode ser bastante variável ao longo do ano, afetada por fatores sazonais, crises econômicas ou mudanças de comportamento do consumidor.
Mitigação: Diversificar as estratégias de receita e manter flexibilidade para ajustar o modelo de negócio conforme as tendências do mercado.

- Mudanças Regulatórias e Legais:
Alterações em leis e regulamentações relacionadas a eventos, locações e proteção de dados podem exigir adaptações rápidas no modelo de negócio e na operação da plataforma.
Mitigação: Monitorar o cenário regulatório e contar com assessoria jurídica para antecipar e ajustar as estratégias de acordo com as novas demandas.

- Riscos de Imagem e Reputação:
Problemas operacionais ou incidentes (como falhas de segurança ou avaliações negativas não gerenciadas) podem ser amplificados nas redes sociais, afetando a credibilidade do projeto.
Mitigação: Estabelecer um plano de gerenciamento de crises, monitorar constantemente as redes sociais e investir em ações de relacionamento com o cliente.

---

## 8. Tomada de Decisões
Estamos **documentando** todas as decisões tomadas na definição do projeto. Essas decisões devem abranger:

- **Seleção de tecnologias e frameworks:**
NestJs -> Facilidade em aprendizado, tecnologia recente, mais familiarizado com o grupo.

React -> Facilidade em aprendizado, tecnologia recente, causa interesse ao grupo.

Swagger -> Facilidade em testar e documentar o código.

Javascript -> Mais familiariazado com o grupo e opção para juntar o backend e frontend.

React Native -> Interesse ao grupo para produto mobile (talvez).

Docker -> Interesse ao grupo, tecnologia recente, muito vantajoso para o produto.

Git -> Importante ao grupo para organização das mudanças do código.

MongoDB ou Postgres -> Um é bem flexivel e o outro mais Rigido, melhores bancos para o nosso uso, podemos utilizar os dois (talvez).

Github -> Plataforma que o grupo é familiarizado, ótimo para guardar o nosso código ou algo relacionado ao projeto.

Trello -> Plataforma que o grupo é familiarizado, ótimo para organizar as tarefas, ideias e andamento do projeto.

Clockify -> Plataforma que o grupo é familiarizado, ótimo para cronometrar o tempo ao executar tarefas relacionado ao projeto.

Microsoft Forms -> Interessante ao grupo, ótimo para conseguir ter um bom uso e organização das perguntas.

Google Drive -> Plataforma que o grupo é familiarizado, ótimo para guardar a nossa documentação ou algo relacionado ao projeto.

Discord -> Plataforma que o grupo é familiarizado, ótimo para reuniões do grupo.

Inteligencias Artificiais -> Ótimo para todas as partes do nosso projeto e para não ficar atras das outras empresas.

- **Definição de estruturas de dados**

Programação Orientada a Objetos.

- **Escolha de algoritmos**


- **Adoção de padrões de projeto**

Está na documentação de Guia de Convenções de Codificação.

- **Definição de componentes do sistema**


- **Modelos de decisão utilizados**, como:
  - Análise comparativa de alternativas
  - Prototipagem e experimentação
  - Análise de risco

Todas as decisões devem ser **justificadas com base nos requisitos do projeto**.

---

## 9. Organização da Arquitetura MVC
Com base nas funcionalidades identificadas, vamos estruturar o código seguindo o padrão **Modelo-Visão-Controlador (MVC)**. Isso inclui:
- **Model:** Definir classes e regras de negócio.
- **View:** Criar interfaces gráficas para apresentação dos dados.
- **Controller:** Implementar a lógica de controle e interação entre a interface e os dados.

Os **arquivos serão criados e serão organizados dessa forma**.

## Estrutura do Projeto (Backend + NestJS)

    MVC - Model View Controller

    /nomaSolutions
        /src
            /entities
                /locador
                    locador.module.ts
                    locador.controller.ts
                    locador.service.ts
                    locador.schema.ts
                /locatario
                    locatario.module.ts
                    locatario.controller.ts
                    locatario.service.ts
                    locatario.schema.ts
                /prestador-de-servico
                    prestador-de-servico.module.ts
                    prestador-de-servico.controller.ts
                    prestador-de-servico.service.ts
                    prestador-de-servico.schema.ts
            /shared
                /config
                database.config.ts
            main.ts
            /frontend
    

---

## 10. Avaliação das Decisões
Ao finalizar o projeto, os participantes devem revisar suas escolhas com base nos seguintes critérios:
- **Compatibilidade com os requisitos funcionais e não funcionais**
- **Coerência entre arquitetura planejada e implementação**
- **Testes de desempenho, usabilidade e qualidade**
- **Feedback dos stakeholders e documentação das lições aprendidas**

---

- Criar o projeto
- Construir o esboço
- Utilizar a arquitetura MVC

---

# Próxima etapa

**Implementação de um entregável do projeto**
