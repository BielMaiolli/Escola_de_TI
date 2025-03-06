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

---

## 8. Tomada de Decisões
Vocês devem **documentar** todas as decisões tomadas na definição do projeto. Essas decisões devem abranger:
- **Seleção de tecnologias e frameworks**
- **Definição de estruturas de dados**
- **Escolha de algoritmos**
- **Adoção de padrões de projeto**
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
