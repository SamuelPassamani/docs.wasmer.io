# AGENTS.md - Diretivas e Base de Conhecimento do Agente de IA

Este arquivo serve como as diretrizes personalizadas e base de conhecimento para o Agente de IA interagir com este repositório.

## 1. Diretivas de Comportamento Gerais

*   **Foco na Qualidade:** Priorize a criação de código limpo, legível, testável e eficiente.
*   **Segurança:** Sempre considere implicações de segurança em todas as ações e sugestões.
*   **Comunicação Clara:** Ao interagir, forneça informações concisas e bem estruturadas.
*   **Proatividade:** Antecipe problemas e sugira melhorias ou soluções preventivas.
*   **Consistência:** Mantenha a consistência com os padrões e estilos existentes no repositório.
*   **Modularidade:** Favoreça soluções modulares e desacopladas.

## 2. Instruções de Comportamento Específicas do Repositório

*   **Estilo de Código:**
    *   **TypeScript/JavaScript:** Siga as convenções do ESLint e Prettier configuradas no projeto.
    *   **React:** Utilize componentes funcionais com Hooks.
    *   **Tailwind CSS:** Use as classes de utilitário do Tailwind para estilização, mantendo a consistência com o `tailwind.config.js`.
*   **Processo de Contribuição:**
    *   Crie branches para novas funcionalidades a partir do `main`.
    *   Abra Pull Requests para revisão de código.
    *   As alterações na documentação devem ser feitas nos arquivos MDX correspondentes dentro do diretório `pages`.
*   **Testes:**
    *   Embora não haja um framework de teste formal configurado, verifique visualmente as alterações executando o servidor de desenvolvimento local (`pnpm run dev`).
    *   Garanta que as alterações não quebrem o processo de build (`pnpm run build`).
*   **Documentação:**
    *   Este repositório *é* a documentação. Atualize os arquivos `.mdx` relevantes para qualquer nova funcionalidade ou alteração.
    *   Para alterações na estrutura de navegação, edite os arquivos `_meta.json` apropriados.
    *   Adicione comentários claros em componentes React complexos.
*   **Convenções de Nomenclatura:**
    *   **Arquivos de Componente:** Use PascalCase (ex: `MyComponent.tsx`).
    *   **Arquivos de Página:** Use kebab-case (ex: `my-page.mdx`).
*   **Arquitetura:**
    *   Mantenha a estrutura de documentação do Nextra.
    *   Evite lógica complexa nos arquivos MDX; encapsule-a em componentes React no diretório `components/`.
    *   Respeite os redirecionamentos em `next.config.mjs` ao mover ou renomear páginas para garantir a retrocompatibilidade dos links.

## 3. Base de Conhecimento do Repositório

### 3.1. Visão Geral do Projeto
Este repositório contém o código-fonte do site de documentação oficial do Wasmer (docs.wasmer.io). O objetivo é fornecer uma referência completa, guias e tutoriais para os produtos da Wasmer, que incluem o **Wasmer Runtime** (para executar pacotes WebAssembly), o **Wasmer Registry** (para publicar e descobrir pacotes) e o **Wasmer Edge** (para implantar aplicativos na borda).

### 3.2. Tecnologias e Ferramentas Utilizadas
*   **Linguagens:** TypeScript, JavaScript (ES6+), MDX
*   **Frameworks/Bibliotecas Frontend:** Next.js, Nextra, React
*   **Estilização:** Tailwind CSS, PostCSS
*   **Ferramentas de Build/Empacotamento:** pnpm, Next.js CLI
*   **Outras:** ESLint, Prettier, Vercel (para implantação, inferido do uso do Next.js)

### 3.3. Estrutura e Componentes Chave
*   `/pages/`: Contém todo o conteúdo da documentação em formato MDX. A estrutura de diretórios aqui define a estrutura da URL do site.
    *   `_meta.json`: Arquivos que controlam a ordem e os títulos da navegação da barra lateral em cada seção.
*   `/components/`: Abriga componentes React reutilizáveis que são importados para os arquivos MDX para fornecer funcionalidade e UI interativas.
*   `/public/`: Contém ativos estáticos como imagens, favicons e fontes.
*   `/styles/`: Arquivos CSS globais.
*   `theme.config.tsx`: Arquivo de configuração central para o `nextra-theme-docs`, onde o layout, logotipo, rodapé, metadados e navegação do site são personalizados.
*   `next.config.mjs`: Arquivo de configuração do Next.js. É crucial para definir redirecionamentos de URL, o que é importante para manter a integridade dos links após reestruturações de conteúdo.
*   `package.json`: Define os scripts do projeto (`dev`, `build`) e gerencia todas as dependências do Node.js via `pnpm`.

### 3.4. Padrões e Convenções Observados
*   **Arquitetura:** O site segue o padrão de arquitetura do Nextra, que usa um sistema de roteamento baseado em arquivos e arquivos `_meta.json` para gerar a navegação.
*   **Content-Driven:** O site é orientado pelo conteúdo, com o conteúdo principal escrito em Markdown (MDX), tornando-o acessível para contribuidores técnicos e não técnicos.
*   **Componentização:** A funcionalidade complexa é abstraída em componentes React para reutilização e separação de preocupações.
*   **Configuração de Redirecionamento:** Há um uso extensivo de redirecionamentos em `next.config.mjs` para lidar com a evolução da estrutura da documentação e evitar links quebrados.

### 3.5. Outras Observações Relevantes
*   O projeto usa `pnpm` como gerenciador de pacotes. Certifique-se de usar os comandos `pnpm` (ex: `pnpm install`, `pnpm run dev`) em vez de `npm` ou `yarn`.
*   Ao adicionar ou modificar o conteúdo, é essencial executar o servidor de desenvolvimento local (`pnpm run dev`) para visualizar as alterações e garantir que a formatação e a funcionalidade estejam corretas.
*   Qualquer alteração significativa na estrutura de arquivos em `/pages` provavelmente exigirá a criação de novos redirecionamentos em `next.config.mjs` para evitar quebrar links existentes.

## 4. Agentes Específicos

### 4.1. Agente "Jules"
O Agente "Jules" é uma instância de IA especializada encarregada de tarefas de arquitetura de instruções, documentação e execução de missões específicas neste repositório.

*   **Diretriz Principal:** Operar exclusivamente em português.
*   **Documentação Detalhada:** Para mais informações sobre as capacidades, funcionalidades e o fluxo de trabalho do Agente Jules, consulte o documento [README do Projeto Jules](./docs.wasmer.io/.jules/README.md).