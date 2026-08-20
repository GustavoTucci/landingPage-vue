# ARCHVIZ

> Visualização arquitetônica para transformar projetos em experiências que podem ser compreendidas, apresentadas e lembradas.

[![Vue](https://img.shields.io/badge/Vue-3-42B883?logo=vuedotjs&logoColor=white)](https://vuejs.org/)
[![Vue CLI](https://img.shields.io/badge/Vue%20CLI-5-35495E?logo=vue.js&logoColor=white)](https://cli.vuejs.org/)
[![Status](https://img.shields.io/badge/status-em%20desenvolvimento-C9B79F)](#status-do-projeto)

## Sobre o projeto

ARCHVIZ é uma landing page institucional criada para um estúdio de visualização arquitetônica. A interface apresenta portfólio, serviços e formas de contato em uma experiência responsiva, com direção visual editorial e foco em clareza, atmosfera e apresentação de projetos.

O projeto foi desenvolvido em Vue 3 com componentes independentes e estilos organizados por seção. A identidade utiliza uma base escura, detalhes em bege e imagens arquitetônicas para reforçar o posicionamento premium da marca.

## O que a página apresenta

- Hero section com proposta de valor e chamadas para ação.
- Navegação responsiva com menu para dispositivos móveis.
- Diferenciais da empresa em componentes reutilizáveis.
- Portfólio com filtros por categoria: residencial, comercial, interiores e animação.
- Carrossel de depoimentos com controles de navegação.
- Planos de produção com cards responsivos e botões alinhados.
- Conteúdo editorial sobre visualização arquitetônica.
- Formulário de contato com validação dos campos.
- Microinterações, estados de hover e adaptação para desktop, tablet e mobile.

## Stack técnica

- Vue 3
- Vue CLI 5
- JavaScript
- CSS3, Flexbox e CSS Grid
- Variáveis CSS para cores, espaçamentos e bordas
- ESLint e `eslint-plugin-vue`

## Organização do código

```text
src/
├── assets/
│   ├── styles/
│   │   ├── animations.css
│   │   └── variables.css
│   └── imagens do projeto
├── components/
│   ├── blog/
│   ├── contact/
│   ├── features/
│   ├── footer/
│   ├── header/
│   ├── hero/
│   ├── portfolio/
│   ├── pricing/
│   └── testimonials/
├── App.vue
└── main.js
```

Cada seção possui seu próprio componente Vue e arquivo CSS. Essa separação facilita a manutenção da interface e permite evoluir cada parte sem concentrar toda a lógica em um único arquivo.

## Como executar

### Pré-requisitos

- Node.js 18 ou superior
- npm 9 ou superior

### Instalação

```bash
npm install
```

### Ambiente de desenvolvimento

```bash
npm run serve
```

Após iniciar o servidor, acesse a URL exibida no terminal. Por padrão, o projeto utiliza `http://localhost:8080`.

## Comandos disponíveis

| Comando | Descrição |
| --- | --- |
| `npm run serve` | Inicia o servidor de desenvolvimento. |
| `npm run build` | Gera os arquivos de produção em `dist/`. |
| `npm run lint` | Verifica problemas de sintaxe e estilo. |

## Build e publicação

Gere uma versão pronta para publicação com:

```bash
npm run build
```

Os arquivos finais serão criados em `dist/`. Essa pasta pode ser publicada em serviços de hospedagem estática, como Netlify, Vercel ou GitHub Pages.

## Demonstração

Uma versão publicada do projeto está disponível em:

<https://clever-starburst-2a2467.netlify.app/>

## Status do projeto

O projeto está em desenvolvimento. A interface e as interações principais estão implementadas, enquanto o formulário e os dados de conteúdo ainda utilizam informações demonstrativas.

## Próximos passos

- Integrar o formulário a um serviço de envio real.
- Criar modal com detalhes individuais dos projetos.
- Substituir os dados demonstrativos por conteúdo real da empresa.
- Converter imagens para WebP ou AVIF e aplicar carregamento lazy.
- Adicionar testes de interação para filtros, formulário e navegação.

