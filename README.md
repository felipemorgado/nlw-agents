# NLW Agents - Projeto Fullstack

Projeto desenvolvido durante um evento da Rocketseat, composto por duas aplicações: uma **API back-end** com Node.js e uma **interface front-end** com React.

## 📁 Estrutura do Repositório

```
.
├── server/  # API com Node.js, Fastify, PostgreSQL
└── web/     # Front-end com React 19
```

## 📚 Índice

- [📦 server (API)](#-server-api)
- [🌐 web (Front-end)](#-web-front-end)

---

## 📦 server (API)

Projeto desenvolvido durante um evento da Rocketseat utilizando tecnologias modernas para criação de uma API robusta e eficiente.

### 🚀 Tecnologias

- Node.js com TypeScript nativo (experimental strip types)  
- Fastify - Framework web rápido e eficiente  
- PostgreSQL com extensão pgvector para vetores  
- Drizzle ORM - Type-safe database operations  
- Zod - Schema validation  
- Docker - Containerização do banco de dados  
- Biome - Linting e formatação de código  

### 🏗️ Arquitetura

O projeto segue uma arquitetura modular com:

- Separação de responsabilidades entre rotas, schemas e conexão com banco  
- Validação de schemas com Zod para type safety  
- ORM type-safe com Drizzle para operações de banco de dados  
- Validação de variáveis de ambiente centralizadas  

### ⚙️ Setup e Configuração

#### Pré-requisitos

- Node.js (versão com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

#### Passos:

1. Clone o repositório  
   ```bash
   git clone <url-do-repositorio>
   cd server
   ```

2. Configure o banco de dados  
   ```bash
   docker-compose up -d
   ```

3. Configure as variáveis de ambiente  
   Crie um arquivo `.env` na raiz do projeto:
   ```
   PORT=3333
   DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
   ```

4. Instale as dependências  
   ```bash
   npm install
   ```

5. Execute as migrações do banco  
   ```bash
   npx drizzle-kit migrate
   ```

6. (Opcional) Popule o banco com dados de exemplo  
   ```bash
   npm run db:seed
   ```

7. Execute o projeto  
   **Desenvolvimento:**
   ```bash
   npm run dev
   ```
   **Produção:**
   ```bash
   npm start
   ```

### 📚 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo de desenvolvimento com hot reload  
- `npm start` - Executa o servidor em modo de produção  
- `npm run db:seed` - Popula o banco de dados com dados de exemplo  

### 🌐 Endpoints

A API estará disponível em [http://localhost:3333](http://localhost:3333)

- `GET /health` - Health check da aplicação  
- `GET /rooms` - Lista as salas disponíveis  

Desenvolvido com ❤️ durante o NLW da Rocketseat

---

## 🌐 web (Front-end)

Projeto desenvolvido durante um evento da Rocketseat para demonstrar o uso de agentes inteligentes na web.

### 🚀 Tecnologias

- React 19.1 - Biblioteca para interfaces de usuário  
- TypeScript 5.8 - Superset JavaScript com tipagem estática  
- Vite 7.0 - Build tool e servidor de desenvolvimento  
- TailwindCSS 4.1 - Framework CSS utility-first  
- React Router Dom 7.6 - Biblioteca de roteamento  
- TanStack React Query 5.8 - Gerenciamento de estado servidor e cache  
- Radix UI - Componentes primitivos acessíveis  
- Shadcn/ui - Sistema de componentes  
- Lucide React - Biblioteca de ícones  

### 📂 Padrões de Projeto

- Component-based Architecture  
- File-based Routing com React Router  
- Server State Management com React Query  
- Variant-based Components com CVA  
- Composition Pattern com Radix Slot  
- Path Aliasing (`@/` aponta para `src/`)  

### ⚙️ Configuração do Projeto

#### Pré-requisitos

- Node.js (versão 18 ou superior)  
- npm ou yarn  

#### Instalação

1. Clone o repositório  
2. Instale as dependências:  
   ```bash
   npm install
   ```
3. Execute o servidor de desenvolvimento:  
   ```bash
   npm run dev
   ```

Acesse a aplicação em [http://localhost:5173](http://localhost:5173)

### 📚 Scripts Disponíveis

- `npm run dev` - Inicia o servidor de desenvolvimento  
- `npm run build` - Gera build de produção  
- `npm run preview` - Preview do build de produção  

### 🔗 Backend

O projeto consome uma API que deve estar rodando na porta `3333`. Certifique-se de que o backend esteja configurado e executando antes de iniciar o frontend.

### 🛠️ Estrutura do Projeto

```
src/
├── components/ui/    # Componentes de interface
├── pages/            # Páginas da aplicação
├── lib/              # Utilitários e configurações
└── app.tsx           # Componente raiz
```

---

> Repositórios Originais:
> - [Server](https://github.com/rocketseat-education/nlw-agents-aulas-server)
> - [Web](https://github.com/rocketseat-education/nlw-agents-aulas-web)
