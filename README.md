# Escola_de_TI V.1
Repositório da Escola de TI

# Primeiro Projeto – Arquitetura MVC

## 1. Criação do Projeto
- Criar um **repositório** em uma ferramenta de versionamento, como **GitHub**. ✔
- Criar um **README** para documentar as **decisões do projeto**, incluindo justificativas e escolhas arquiteturais. ✔

---

## 2. Definição do Produto
Os participantes devem definir um produto de software a ser implementado. As opções podem incluir:
- **Aplicação web**
- **Aplicativo móvel**
- **Outro software relevante**

A definição do produto deve ser detalhada, incluindo **objetivo, público-alvo e contexto de uso**.

### 2.1 Objetivo

### 2.2 Público-alvo

### 2.3 Contexto de uso

---

## 3. Requisitos do Sistema
Os participantes devem listar os **requisitos funcionais e não funcionais**, descrevendo-os detalhadamente. Isso inclui:
- **Funcionalidades principais** do produto, como:
  - Criação de perfis de usuário
  - Visualização de conteúdo
  - Postagem de mensagens
  - Adição de amigos
- **Requisitos não funcionais**, como:
  - **Desempenho** (tempo de resposta, escalabilidade)
  - **Segurança** (mecanismos de autenticação e autorização)
  - **Usabilidade** (design intuitivo e acessibilidade)
  - **Manutenibilidade** (facilidade de atualização e suporte)

---

## 4. Restrições e Condições
- **Restrições Técnicas:** Escolha de plataformas, linguagens de programação e frameworks disponíveis.
- **Restrições Não Técnicas:** Orçamento, prazos de entrega, requisitos legais e regulatórios.

## 5. Necessidades dos Stakeholders
Considerar clientes, usuários finais, gerentes de projeto e desenvolvedores.

## 6. Tendências Tecnológicas
Exploração de novas linguagens, frameworks, plataformas em nuvem e metodologias ágeis.

## 7. Riscos do Projeto
Avaliação de riscos técnicos, operacionais e de negócios.

---

## 5. Tomada de Decisões
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

## 6. Organização da Arquitetura MVC
Com base nas funcionalidades identificadas, os participantes devem estruturar o código seguindo o padrão **Modelo-Visão-Controlador (MVC)**. Isso inclui:
- **Model:** Definir classes e regras de negócio.
- **View:** Criar interfaces gráficas para apresentação dos dados.
- **Controller:** Implementar a lógica de controle e interação entre a interface e os dados.

Os participantes devem **definir quais arquivos serão criados e como serão organizados**.

## Estrutura do Projeto (Backend + NestJS) | Utilizando um exemplo de pokemon.

```bash
projeto/
 frontend/
 backend/
    src/
        modules/
            pokemon/
                controllers/
                    pokemon.controller.ts
                services/
                    pokemon.service.ts
                repositories/
                    pokemon.repository.ts
                entities/
                    pokemon.entity.ts
                dtos/
                    create-pokemon.dto.ts
                    update-pokemon.dto.ts
                schemas/
                    pokemon.schema.ts
                pokemon.module.ts

            auth/
                controllers/
                    auth.controller.ts
                services/
                    auth.service.ts
                repositories/
                    auth.repository.ts
                entities/
                    auth.entity.ts
                dtos/
                    login-auth.dto.ts
                auth.module.ts

        common/  # Código compartilhado entre os módulos
            decorators/
                roles.decorator.ts
            guards/
                auth.guard.ts
                roles.guard.ts
            filters/
                exception.filter.ts
            interceptors/
                logging.interceptor.ts
            pipes/
                validation.pipe.ts

        config/
            databaseConfig/
                database.config.ts
            jwtConfig/
                jwt.config.ts
            swaggerConfig/
                swagger.config.ts

        main.ts
        app.module.ts
    
    test/
    .env
    package.json
    tsconfig.json
    README.md

---
```
## 7. Avaliação das Decisões
Ao finalizar o projeto, os participantes devem revisar suas escolhas com base nos seguintes critérios:
- **Compatibilidade com os requisitos funcionais e não funcionais**
- **Coerência entre arquitetura planejada e implementação**
- **Testes de desempenho, usabilidade e qualidade**
- **Feedback dos stakeholders e documentação das lições aprendidas**

---

## 8. Entrega da Atividade
Vocês devem enviar o link do git do projeto através do formulários: a atividade através do seguinte link:
📌 **[Formulário de Entrega](ainda não fiz o formulário)**

---

# RESUMO

- Criar o projeto
- Construir o esboço
- Utilizar a arquitetura MVC

---

# Próxima etapa

**Implementação de um entregável do projeto**
