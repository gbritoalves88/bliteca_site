# BliTeca — Site Institucional

Site institucional do **BliTeca**, uma plataforma criada para leitores que desejam organizar suas bibliotecas, acompanhar o progresso de leitura, descobrir novos livros e compartilhar experiências com outros leitores.

O projeto consiste em uma landing page responsiva desenvolvida com Angular, apresentando o aplicativo, suas principais funcionalidades e os canais de contato.

**Repositório:** https://github.com/gbritoalves88/bliteca_site

**Site:** https://bliteca.com.br

**Aplicativo:** [BliTeca na Google Play](https://play.google.com/store/apps/details?id=com.bliteca.app)

---

## 🎯 Objetivo

O site foi desenvolvido para apresentar o BliTeca ao público, centralizando informações sobre o aplicativo e facilitando o acesso aos seus principais canais.

A página funciona como porta de entrada para novos usuários, comunicando a proposta do produto e direcionando os visitantes para a instalação do aplicativo Android.

## ✨ Seções e funcionalidades

### Início — Hero

Apresentação principal do BliTeca, com:

- Identidade visual do produto.
- Mensagem de apresentação.
- Descrição resumida da proposta do aplicativo.
- Imagem ilustrativa da tela inicial.

### O Aplicativo

Apresentação das principais funcionalidades:

- Organização da biblioteca pessoal.
- Acompanhamento do progresso de leitura.
- Conexão com outros leitores.
- Descoberta de novos livros e recomendações.

A seção utiliza imagens reais da interface do aplicativo para aproximar a apresentação do produto da experiência de uso.

### Sobre o BliTeca

Apresenta a origem e o propósito do projeto, destacando a relação entre tecnologia, leitura e comunidade.

Também disponibiliza um acesso direto à página do aplicativo na Google Play.

### Contato

Área destinada à comunicação com o projeto:

- Link para envio de e-mail.
- Endereço de contato.
- Localização institucional.

### Navegação

- Menu com links para as seções da página.
- Menu mobile com abertura e fechamento interativos.
- Rolagem suave entre seções.
- Links para redes sociais.
- Links institucionais no rodapé.

## 🖥️ Identidade visual

O site utiliza uma identidade visual inspirada no universo da leitura, com uma apresentação leve e acolhedora.

| Elemento | Definição |
|---|---|
| Fundo principal | `#FAF3E8` |
| Fundo de conteúdo | `#FFFFFF` |
| Fundo de cards | `#F5EFE6` |
| Texto principal | `#2A2522` |
| Texto secundário | `#6B6560` |
| Cor de destaque | `#DB7C00` |
| Destaque no hover | `#B86600` |

### Tipografia

- **Playfair Display:** títulos e elementos de destaque.
- **Inter:** textos, descrições e navegação.

As imagens do aplicativo são utilizadas para ilustrar a experiência oferecida pelo BliTeca.

## 🧰 Tecnologias

| Tecnologia | Utilização |
|---|---|
| Angular 21 | Framework frontend |
| TypeScript 5.9 | Linguagem principal |
| SCSS | Estilização |
| HTML5 | Estrutura das páginas |
| CSS3 | Layout e responsividade |
| RxJS 7.8 | Biblioteca reativa utilizada pelo Angular |
| Angular Signals | Estado reativo do menu mobile |
| Vitest 4 | Infraestrutura de testes |

O projeto utiliza componentes standalone do Angular, com organização modular por seções da página.

## 🏗️ Arquitetura e organização

A aplicação é uma SPA (Single Page Application), composta por uma página principal e componentes independentes.

Não possui backend próprio, banco de dados ou autenticação. O conteúdo institucional é definido diretamente nos templates e componentes Angular.

### Estrutura do projeto

```text
bliteca_site/
│
├── public/
│   ├── assets/
│   │   ├── app.png
│   │   └── inicio.png
│   │
│   ├── favicon.ico
│   ├── favicon.png
│   └── googlePlay.png
│
├── src/
│   ├── app/
│   │   ├── components/
│   │   │   ├── header/
│   │   │   ├── hero/
│   │   │   ├── features/
│   │   │   ├── sobre/
│   │   │   ├── contato/
│   │   │   └── footer/
│   │   │
│   │   ├── app.config.ts
│   │   ├── app.routes.ts
│   │   ├── app.ts
│   │   ├── app.html
│   │   └── app.scss
│   │
│   ├── index.html
│   ├── main.ts
│   └── styles.scss
│
├── angular.json
├── package.json
├── package-lock.json
├── tsconfig.json
└── README.md
```

### Responsabilidade dos componentes

| Componente | Responsabilidade |
|---|---|
| `Header` | Cabeçalho e navegação desktop/mobile |
| `Hero` | Apresentação principal do produto |
| `Features` | Funcionalidades do aplicativo |
| `Sobre` | História e propósito do BliTeca |
| `Contato` | Informações e canais de contato |
| `Footer` | Rodapé, redes sociais e links institucionais |

O componente principal (`App`) organiza as seções e define a composição da página.

### Navegação

A navegação principal utiliza âncoras HTML para direcionar o visitante às seções:

| Âncora | Destino |
|---|---|
| `#inicio` | Apresentação |
| `#app` | Funcionalidades |
| `#sobre` | Sobre o projeto |
| `#contato` | Contato |

O menu mobile utiliza Angular Signals para controlar seu estado de abertura e fechamento.

## 📱 Responsividade

O layout foi desenvolvido para se adaptar a diferentes tamanhos de tela.

- Navegação desktop substituída por menu mobile em telas menores.
- Conteúdo organizado em colunas no desktop.
- Seções reorganizadas verticalmente em dispositivos móveis.
- Imagens dimensionadas conforme o espaço disponível.
- Grade de funcionalidades adaptada para telas menores.
- Ajustes específicos para dispositivos com largura de até 480px.

O objetivo é manter a apresentação e a navegação consistentes em computadores, tablets e smartphones.

## 🚀 Executando localmente

### Pré-requisitos

- Node.js.
- npm 11.21.1 ou compatível.
- Git.

### 1. Clonar o repositório

```bash
git clone https://github.com/gbritoalves88/bliteca_site.git

cd bliteca_site
```

### 2. Instalar dependências

```bash
npm install
```

### 3. Iniciar o servidor de desenvolvimento

```bash
npm start
```

A aplicação estará disponível em:

```text
http://localhost:4200
```

O Angular CLI disponibiliza recarga automática durante o desenvolvimento.

## 🏗️ Build de produção

Para gerar a versão otimizada:

```bash
npm run build
```

O build utiliza a configuração de produção definida no `angular.json`, incluindo:

- Otimização dos arquivos.
- Hash nos nomes dos arquivos.
- Limites de tamanho para o bundle inicial.
- Limites de tamanho para estilos dos componentes.

Os arquivos compilados são gerados no diretório `dist/`.

## 🧪 Testes

O projeto utiliza Vitest como infraestrutura de testes.

Para executar:

```bash
npm test
```

Os testes unitários ficam próximos dos respectivos componentes, em arquivos `.spec.ts`.

## 🌐 Integrações externas

O site possui links para serviços externos:

| Serviço | Finalidade |
|---|---|
| Google Play | Download do aplicativo Android |
| Instagram | Presença social do BliTeca |
| LinkedIn | Página institucional |
| E-mail | Contato com o projeto |
| Google Fonts | Carregamento das fontes Inter e Playfair Display |
| Unsplash | Imagem ilustrativa da seção Sobre |

## 🔗 Relação com o ecossistema BliTeca

O site faz parte do ecossistema do BliTeca e atua como canal institucional e de divulgação do aplicativo.

Enquanto o aplicativo concentra a experiência dos leitores e a API gerencia as funcionalidades e os dados do sistema, o site apresenta o produto ao público.

| Projeto | Responsabilidade |
|---|---|
| `bliteca_site` | Site institucional e divulgação |
| `bio-tek` | Aplicativo frontend |
| `bio-tek-api` | Backend e API REST |

## 📌 Considerações

O BliTeca Site é uma aplicação frontend independente, com foco em apresentação institucional, comunicação e divulgação do aplicativo.

Sua estrutura baseada em componentes permite manter e evoluir cada seção de forma organizada, sem a complexidade de uma aplicação full stack.

---

Desenvolvido por [Gabriel Brito](https://github.com/gbritoalves88).
