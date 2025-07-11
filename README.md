# NLW Agents

Este projeto foi desenvolvido durante o evento **NLW** promovido pela [Rocketseat](https://rocketseat.com.br/).

## Descrição

O **NLW Agents** é um servidor Node.js construído com Fastify, Drizzle ORM e Zod, seguindo boas práticas de organização de código e padrões modernos de desenvolvimento backend.

## Tecnologias e Bibliotecas Principais

- **[Fastify](https://www.fastify.io/):** Framework web rápido e eficiente para Node.js.
- **[Drizzle ORM](https://orm.drizzle.team/):** ORM para TypeScript focado em segurança e performance.
- **[Zod](https://zod.dev/):** Validação de schemas e tipagem.
- **[fastify-type-provider-zod](https://github.com/fastify/fastify-type-provider-zod):** Integração entre Fastify e Zod.
- **[@fastify/cors](https://github.com/fastify/fastify-cors):** Middleware para CORS.
- **[postgres](https://github.com/porsager/postgres):** Cliente PostgreSQL para Node.js.
- **[drizzle-kit](https://github.com/drizzle-team/drizzle-kit):** Ferramenta de migrations e geração de schemas.
- **[drizzle-seed](https://github.com/drizzle-team/drizzle-seed):** Seed de dados para Drizzle ORM.
- **[TypeScript](https://www.typescriptlang.org/):** Tipagem estática para JavaScript.
- **[@biomejs/biome](https://biomejs.dev/):** Linter e formatter.

## Padrões de Projeto e Organização

- **Organização em camadas:** Separação clara entre rotas HTTP (`src/http/routes`), lógica de banco de dados (`src/db`), configuração de ambiente (`src/env.ts`) e inicialização do servidor (`src/server.ts`).
- **Validação centralizada:** Uso de Zod para validação de dados de entrada e saída.
- **Migrations e Seeds:** Estrutura para versionamento e popular dados do banco via Drizzle.

## Setup e Configuração

1. **Clone o repositório:**

   ```bash
   git clone <url-do-repo>
   cd server
   ```

2. **Instale as dependências:**

   ```bash
   npm install
   ```

3. **Configure o ambiente:**

   - Copie o arquivo `.env.example` para `.env` e ajuste as variáveis conforme necessário.

4. **Rode as migrations e seeds (se necessário):**

   ```bash
   # Comando de migration e seed conforme Drizzle
   npm run db:seed
   ```

5. **Inicie o servidor em modo desenvolvimento:**

   ```bash
   npm run dev
   ```

6. **Acesse a rota de health check:**
   ```
   GET /health
   ```

---

Se precisar de mais detalhes ou exemplos de uso, consulte os arquivos na pasta `src/` ou a documentação das bibliotecas listadas acima.
