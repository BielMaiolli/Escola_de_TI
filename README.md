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


### 2.2 Público-alvo
- Cliente Tipo 1 (Pessoa que quer alugar um espaço de eventos; Locatário)
- Cliente Tipo 2 (Pessoa que tem um local para alugar; Locador)

### 2.3 Contexto de uso
Quando alguem quiser organizar um evento, festa ou churrasco em familia.

---

## 3. Requisitos do Sistema
Os **requisitos funcionais e não funcionais**, detalhadamente:
- **Funcionalidades principais** do produto, como:
  - Criação de perfis de usuário;
  - Cadastro de locais;
  - Ferramenta de pesquisa (utilização de barra de pesquisa com filtros);
  - Registro e Login;

    
- **Requisitos não funcionais**, como:
  - **Desempenho** (tempo de resposta, escalabilidade)
  - **Segurança** (mecanismos de autenticação e autorização)
  - **Usabilidade** (design intuitivo e acessibilidade)
  - **Manutenibilidade** (facilidade de atualização e suporte)

---

## 4. Restrições e Condições
- **Restrições Técnicas:**  linguagens de programação e frameworks disponíveis.
  
### Tecnologias
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
Com base nas funcionalidades identificadas, vamos estruturar o código seguindo o padrão **Modelo-Visão-Controlador (MVC)**. Isso inclui:
- **Model:** Definir classes e regras de negócio.
- **View:** Criar interfaces gráficas para apresentação dos dados.
- **Controller:** Implementar a lógica de controle e interação entre a interface e os dados.

Os **arquivos serão criados e serão organizados dessa forma**.

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

- Criar o projeto
- Construir o esboço
- Utilizar a arquitetura MVC

---

# Próxima etapa

**Implementação de um entregável do projeto**
