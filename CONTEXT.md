# IAG - Contexto do Projeto

## 1. Visão Geral
* **O que é o projeto?** O site institucional do Instituto Agro Genética (IAG).
* **Qual problema ele resolve?** Apresenta as especialidades do laboratório em biologia molecular e análise de solo, divulga a equipe e os valores da instituição, fornece um blog educativo para o produtor rural e viabiliza canais de contato.
* **Público-alvo / Casos de uso principais:**
  - Produtores rurais, agrônomos e empresas agrícolas buscando análises genéticas e de solo de alta precisão.
  - Leitores interessados em biotecnologia aplicada à agricultura (Blog).
  - Candidatos ou parceiros interessados em conhecer a equipe técnica.

## 2. Tecnologias e Stack
* **Framework Frontend:** Astro (Static Site Generator) - Escolhido por ser focado em conteúdo, leve, rápido e ter excelente SEO nativo.
* **Estilização:** Tailwind CSS (integrado ao Astro).
* **Gestão de Conteúdo (Blog):** Markdown nativo do Astro (Content Collections).
* **Formulário de Contato:** Integração com Web3Forms (envio de e-mail sem necessidade de backend próprio).
* **Suporte a Idiomas:** Sistema dinâmico de tradução (Português e Inglês) integrado aos layouts e componentes do Astro.
* **Integração Futura (Planejada):** Um portal de clientes em Django-Python será desenvolvido no futuro. O site institucional em Astro permanecerá focado no marketing, direcionando os clientes para o portal Django através de links de login/painel.

## 3. Estrutura de Diretórios
* `/src` - Código fonte do projeto Astro:
  - `/src/pages` - Rotas e páginas do site (Home, Solos, Serviços, Quem Somos, Blog).
  - `/src/components` - Componentes reutilizáveis (Navbar, Footer, formulários, cards).
  - `/src/layouts` - Layouts estruturais HTML (gerenciamento de idioma e metadados SEO).
  - `/src/content` - Coleções de conteúdo Markdown (posts do blog e dados dinâmicos).
* `/public` - Imagens, ícones e outros ativos estáticos públicos.
* `/suporte` - Pasta com dados brutos, biografias e notas de suporte (Ignorada pelo Git em `.gitignore`).

## 4. Diretrizes de Código e Padrões
* **Design e Estética:** Manter a paleta de cores institucional baseada em tons de verde-esmeralda (emerald) e azul/cinza escuro (slate/bg-iag-gradient), com visual moderno, degradês suaves e efeitos de vidro (glassmorphism).
* **SEO:** Garantir tags de título, descrições meta adequadas e hierarquia correta de headings `<h1>`-`<h6>` em todas as páginas para máxima relevância em buscas.
* **Multidioma:** Toda nova seção ou página deve suportar a exibição em Português e Inglês, respeitando o estado do idioma selecionado pelo usuário.

## 5. Status Atual (Junho 2026) e Próximos Passos
* **Migração Concluída:** O site foi 100% migrado para Astro, com Navbar, Footer, Página Inicial, Solos, Serviços e Quem Somos criados e compilando sem avisos.
* **Formulário de Contato:** Totalmente funcional com a chave Web3Forms configurada (`52255464-3f59-4cb4-8f21-d92c68fb59af`).
* **Blog:** Estruturado com coleções de conteúdo em Markdown. Há 4 posts de exemplo em `src/content/blog/`.
* **Pendências para Próxima Sessão:**
  - **Biografias:** Redigir e integrar as bios de **Matheus Hideki**, **Mariana** e **Juliano** em `src/pages/sobre.astro` assim que os dados brutos forem atualizados nos arquivos Markdown da pasta `suporte/`.
  - **Imagens da Equipe:** Upload e configuração das fotos reais da equipe na pasta `public/` para substituir os avatares circulares temporários.

